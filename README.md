# How we work 💼🔌

The following is a brief explanation on how we expect our internal repositories to be setup. We have a ruleset and a couple of workflows that are planned to be used across the entire organization.

## Rulesets 🔒

In the `ruleset-templates` directory, you will find a `default.json` file, it contains the base rules we use across all our repositories. We essentialy disable commits/pushes to the main branch and forces PRs to be squashed as well as have at least 1 reviewer approval.

These rules are applied to a repository in the `Settings -> Rules -> Rulesets -> New ruleset -> Import` section and should be applied immediately on creation of any new internal repository.

## Workflows 🚧

In the `workflow-templates` directory, you will find a `merge.yaml` file and a `release.yaml` file. These are both reusable action workflows that are expected to also be present in most of our repositories.

- The `merge.yaml` workflow ensures that pull request titles follow the [Conventional Commit](https://www.conventionalcommits.org) specification. Combined with the ruleset to block pushes to the main branch and the forcing of PR squashing, this setup allows contributors to create pull requests with commit messages written however they please while keeping the commit messages clean in the main branch through the pre-squash workflow validation.

- The `release.yaml` workflow integrates seamlessly with the `merge.yaml` workflow. It generates a changelog, tagged github releases and a bump in language specific version files based on the Conventional Commits specification messages. This allows for quick and low complexity releases where developers only have to worry about setting a good PR title before the PR is merged to ensure maintainable release notes and a clean commit message history.

These workflow templates can be added to internal repositories in the `Actions -> New workflow` section. Depending on the organization plan you may not be able to see the templates in private repositories, if that is the case you will have to manually copy from the ones here.

## Credits 💡

The `AUTHORS` file is also recommended to be present in every repository. This file lists the names of those who have contributed to the project in any way, whether through code, documentation, design, testing, or other forms of support. It serves to acknowledge the work of both internal team members and external contributors who have provided value to the project.

In most cases, the `AUTHORS` file is updated as contributions are made, with each contributor adding their name during the pull request process. Regular maintenance of this file is encouraged to ensure that all contributors receive proper credit.

## Notes 📝

Files present in this repository, other than the ones mentioned above, are used by github to generate defaults in some of our repositories that do not have custom configurations. See this [thread](https://stackoverflow.com/questions/60507097) for more information.

Repositories can be exempt from some of the above configurations on a per case basis, such as this one, where it makes little sense to verify commit messages, block pushes on the main branch, or generate releases, seeing as only admins should edit this informational repository.
