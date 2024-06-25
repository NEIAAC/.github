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

Please write a great commit message.

1. Capitalize the subject line
2. Do not end the subject line with punctuation.
3. Use the imperative in the subject line ("Fix networking issue")
4. Limit the subject line to 50 characters
5. Separate subject from body with a blank line, the body is optional
6. Wrap the body at about 72 characters
7. Use the body to explain **why**, *not what and how* (the code shows that!)

## Code Reviews

- **Review the code, not the author.** Look for and suggest improvements without disparaging or insulting the author. Provide actionable feedback and explain your reasoning.
- **You are not your code.** When your code is critiqued, questioned, or constructively criticized, remember that you are not your code. Do not take code review personally.
- Kindly note any violations to the guidelines specified in this document.

## Coding Style

Consistency is the most important. Following the existing style, formatting, identation, and naming conventions of the file you are modifying and of the overall project. Failure to do so will result in a prolonged review process that has to focus on updating the superficial aspects of your code, rather than improving its functionality and performance.

For example, if all private properties are prefixed with an underscore `_`, then new ones added should be prefixed in the same way. Or, if methods are named using camelcase, like `thisIsMyNewMethod`, then do not diverge from that by writing `this_is_my_new_method`. You get the idea. If in doubt, please ask or search the codebase for something similar.

When possible, style and format will be enforced with an automated formatter/linter tool to avoid contributors having to worry about it.
