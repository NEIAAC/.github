# Guidelines

This document outlines the guidelines that any work performed as a contributor must adhere to. Read it before making any contributions.

## Code of Conduct

Please review our [Code of Conduct](CODE_OF_CONDUCT.md). It is in effect at all times. We expect it to be honored by everyone.

## Security

Review our [Security Policy](https://github.com/dy0gu/.github/blob/main/SECURITY.md).

## Issues

Before creating an issue, check if you are using the latest version of the project. If you are not up-to-date, see if updating fixes your issue first.

When opening an issue make sure you use the correct template. Fill in as much information as possible.
Use a **clear, short and descriptive title**.

If creating a bug report, include as many details as possible: version, environment, etc. Also include steps to reproduce the bug if you can.

## Pull Requests

Before forking and creating a pull request for non-trivial changes you should open an **issue** to discuss the changes, or discuss your intended approach for solving the problem in the comments of an existing issue, depending on if one exists already or not.

When opening a pull request make sure you use the correct template.
Fill in as much information as possible.
Use a **clear, short and descriptive title** that resembles the issue title it refers to.

All contributions will be licensed under the project's license.

## Commit Messages

Repositories follow the [Conventional Commits](https://www.conventionalcommits.org) standard, this is usually enforced/verified with the use of git hooks and CI.

Some individual repositories may not follow the above convention, in that case you should adere to the existing one. When in doubt, you may **simply ask**.

## Code Reviews

- **Review the code, not the author.** Look for and suggest improvements without disparaging or insulting the author. Provide actionable feedback and explain your reasoning.
- **You are not your code.** When your code is critiqued, questioned, or constructively criticized, remember that you are not your code. Do not take code review personally.
- Kindly note violations to the guidelines specified in this document, if any are found during a review.

## Coding Style

Consistency is the most important. Following the existing style, formatting, identation, and naming conventions of the file you are modifying and of the overall project. Failure to do so will result in a prolonged review process that has to focus on updating the superficial aspects of your code, rather than improving its functionality and performance.

For example, if all private properties are prefixed with an underscore `_`, then new ones added should be prefixed in the same way. Or, if methods are named using camelcase, like `thisIsMyNewMethod`, then do not diverge from that by writing `this_is_my_new_method`. You get the idea. If in doubt, please ask or search the codebase for something similar.

When possible, style and format will be enforced with an automated formatter/linter tool, either using git hooks or CI, to avoid contributors having to worry about it.

## Miscellaneous

We expect all contributions, be it code, design, or documentation, to present themselves in the English language. Any discussion or public facing development activities are also expected to be first and foremost in this language.
