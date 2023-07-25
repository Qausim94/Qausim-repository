---
title: Git Style Guide
permalink: /styleguide/git
---

# Git Styleguide for Commit Messages and Branch Practices

This styleguide provides guidelines for writing consistent and meaningful commit messages and suggests best practices for managing Git branches.

## Commit Message Guidelines

Commit messages should follow a clear and descriptive format. A good commit message should provide enough information to understand the purpose of the commit at a glance. Here are some examples of good and bad commit messages:

### Good Commit Messages

- **feat: Add login functionality**

  - Adds a new feature to enable user login.

- **fix: Fix validation error in signup form**

  - Resolves a bug that was causing validation errors in the signup form.

- **docs: Update README with installation instructions**
  - Updates the project documentation to include clear installation instructions in the README file.

### Bad Commit Messages

- **Fixed bug**

  - Provides no context or details about the bug fix.

- **Updated code**

  - Lacks specific information about the code changes made.

- **Work in progress**
  - Indicates an incomplete or unfinished commit.

## Allowed Commit Types

The following commit types are allowed in this project:

- **build**: Changes that affect the build system or external dependencies. Use this when making changes to build tools, package managers, or other build-related configurations.

- **chore**: Routine tasks, maintenance, or general code changes that are not related to a specific feature or bug. Use this for tasks like updating dependencies, refactoring code, or improving project infrastructure.

- **ci**: Changes to the continuous integration (CI) configuration files and scripts. Use this when modifying the CI pipeline, adding new test cases, or updating the testing environment.

- **docs**: Changes or additions to project documentation. Use this when updating README files, adding or modifying documentation files, or providing inline code comments.

- **feat**: A new feature or enhancement added to the project. Use this when introducing new functionality or significant improvements to existing features.

- **fix**: A bug fix or resolution of an issue. Use this when addressing specific bugs, errors, or unexpected behavior in the code.

- **perf**: A code change that improves performance. Use this when optimizing algorithms, improving runtime efficiency, or enhancing overall system performance.

- **refactor**: A code change that neither fixes a bug nor adds a feature, but improves the code structure or readability. Use this when restructuring code, extracting reusable components, or improving naming conventions.

- **revert**: Reverting a previous commit. Use this when undoing the changes made in a previous commit, typically to address issues or revert unwanted modifications.

- **style**: Changes that do not affect the meaning of the code. Use this for whitespace modifications, formatting updates, or other cosmetic changes.

- **test**: Adding missing tests or correcting existing tests. Use this when adding new test cases, updating test suites, or fixing broken tests.

- **translation**: Changes related to translation or localization. Use this when modifying language files, adding new translations, or improving language support.

- **security**: Changes related to security enhancements or fixes. Use this when addressing vulnerabilities, implementing security measures, or resolving security-related issues.

- **changeset**: A specific type used in some project workflows or version control systems to track changesets or groups of related changes. Use this when following specific guidelines or workflows that utilize changesets.

It is important to choose the appropriate commit type that best describes the nature of the changes made in the commit. Following these guidelines will help maintain a clean commit history, improve collaboration, and ensure consistency throughout the development process.
