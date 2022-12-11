# Contribution Guide
## Installation
TODO write guide

## Commits and Pull Requests
{{ cookiecutter.project_slug }} uses [semantic versioning](https://semver.org/) for releases on the {{ cookiecutter.default_branch }} branch. This means each release as an incremented version number of the form MAJOR.MINOR.PATCH, where:
- MAJOR increments after backwards incompatible (breaking) changes
- MINOR increments after adding functionality that is backwards compatible
- PATCH increments when backwards compatible bug fixes are added

To automate the semantic versioning and generating release notes, {{ cookiecutter.project_slug }} uses the [semantic-release](https://github.com/semantic-release/semantic-release) github package in [Github Actions](https://github.com/features/actions). This requires using [conventional commit](https://www.conventionalcommits.org/) format for all commit messages. Any pull requests that are submitted will not pass the Github Actions CI tool checks until all commits satisfy this format.
> type(optional scope): description
> 
> [optional body]
> 
> [optional footer(s)]

In this format, the type describes the type of change being made:
- fix: a bug patch, corresponding to the PATCH increment in semantic versioning
- feat: introducing new functionality, which on its own corresponds to the MINOR increment in semantic versioning
- Other types are allowed, but will not increment the semantic version number. Some recommended options are build, chore, ci, docs, style, refactor, perf, or test.
The exception to this versioning is when a commit has a footer BREAKING CHANGE, or has a ! after the type/scope (immediately before the :). This corresponds to the MAJOR increment in semantic versioning.

The description briefly describes the changes made in the commit. The optional body can be used to provide additional information on the changes.
