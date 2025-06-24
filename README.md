# How we work 💼🔌

The following is a brief explanation on how we expect our work here to be setup and organized. We have settings, a ruleset and a couple of workflows that should be used across the entire organization.

## Repositories 📦

Internal repositories are expected to have a list of settings configured and follow consistent naming conventions.

In the repository home page:

- Title (repository name) should be in kebab-case, and avoid using numbers.
- Description should start capitalized and end with a period.
- The deployments section, packages section and any other section that is not being used should be disabled in the settings _(cog icon)_ next to the description.
- If the project has a website deployed, make sure it's linked under the description in its respective section.

Every project should include a `README.md` file that lists the minimal steps needed to get it running on a new machine, along with any other relevant information. This file should be in the root of the repository. Other valid alternatives are making use of the **GitHub Wiki** section of the repository or having a dedicated deployed documentation web page/site (like [this](https://github.com/NEIAAC/typescript-template) or [this](https://github.com/NEIAAC/python-template) repository).

In the `Settings -> General` section:

- The default branch should always be named `main`, this aligns with GitHub standards so usually there is no need to change it manually.
- The sponsorships tab should **_always_** be disabled, we do not accept donations here.
- Wikis, Discussions, Projects and other tabs should be disabled, if they are not being used in the repository.
- Pull requests should **only** allow squash merging, with the default commit message being **just** the PR title. When prompted, the   default message created by this setting is expected to be accepted without any changes, the reason for this will be explained further down in this document.
- Branches should always show the suggestion to update if they are behind their base branch.
- Head branches should be configured to always get automatically deleted after a pull requested from them has been merged.

Note that these settings must be configured even when starting a repository from one of our templates, as GitHub currently does not copy settings when creating repositories from templates.

This also applies to the rulesets that will be explained below, you will have to set them again manually too. Other files, such as workflows, will still be copied as they are actual contents of the template repository.

## Rulesets 🔒

In the `ruleset-templates` directory, you will find a `default.json` file, it contains the base rules we use across all our repositories. We essentialy disable commits/pushes to the main branch and forces PRs to be squashed as well as have at least 1 reviewer approval.

These rules are applied to a repository in the `Settings -> Rules -> Rulesets -> New ruleset -> Import` section and should be applied immediately on creation of any new internal repository.

## Workflows 🚧

In the `workflow-templates` directory, you will find a `merge.yaml` file and a `release.yaml` file. These are both reusable action workflows that are expected to also be present in most of our repositories.

- The `convention.yaml` workflow ensures that pull request titles follow the [Conventional Commit](https://www.conventionalcommits.org) specification. Combined with the ruleset to block pushes to the main branch and the forcing of PR squashing, this setup allows contributors to create pull requests with commit messages written however they please while keeping the commit messages clean in the main branch through the pre-squash workflow validation.

- The `release.yaml` workflow integrates seamlessly with the `convention.yaml` workflow. It generates a changelog, tagged github releases and a bump in language specific version files based on the Conventional Commits specification messages. This allows for quick and low complexity releases where developers only have to worry about setting a good PR title before the PR is merged to ensure maintainable release notes and a clean commit message history. Sometimes this workflow may fail with an error related to `release-please` not being able to create the PR labels. If this happens you must create the `2` labels manually, with the names `autorelease: pending` and `autorelease: tagged`, to fix it.

## Credits 💡

The `AUTHORS` file is also recommended to be present in every repository. This file lists the names of those who have contributed to the project in any way, whether through code, documentation, design, testing, or other forms of support. It serves to acknowledge the work of both internal team members and external contributors who have provided value to the project.

In most cases, the `AUTHORS` file is updated as contributions are made, with each contributor adding their name during the pull request process. Regular maintenance of this file is encouraged to ensure that all contributors receive proper credit.

## Notes 📝

Files present in this repository, other than the ones mentioned above, are used by github to generate defaults in some of our repositories that do not have custom configurations. See this [thread](https://stackoverflow.com/questions/60507097) for more information.

Repositories can be exempt from some of the above configurations on a per case basis, such as this one, where it makes little sense to verify commit messages, block pushes on the main branch, or generate releases, seeing as only admins should edit this informational repository.
