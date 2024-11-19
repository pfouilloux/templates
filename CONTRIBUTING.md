# Contributing to Development Templates

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues as you might find out that you don't need to create one.

When you are creating a bug report, please include as many details as possible:

- Use a clear and descriptive title
- Describe the exact steps to reproduce the problem
- Provide specific examples to demonstrate the steps
- Describe the behavior you observed after following the steps
- Explain which behavior you expected to see instead and why
- Include details about your configuration and environment

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When you are creating an enhancement suggestion, please include:

- A clear and descriptive title
- A detailed description of the proposed functionality
- Any possible drawbacks
- Impact on existing features

### Pull Requests

- Fill in the required template

- Follow our coding standards
- Update documentation as needed
- Include tests when adding features
- End all files with a newline

## Development Process

1. Fork the repo
2. Create a new branch
3. Make your changes
4. Submit a pull request

## Testing

Please run the test suite before submitting a pull request.

## Documentation

- Keep README.md updated

- Document new features
- Update examples if needed

## Questions?

Feel free to open an issue for any questions about contributing.

## Development Environment

We strongly recommend using our base development container as it comes with all necessary tools preconfigured:

- Conventional Commits tooling
- Linting and formatting tools
- Git hooks for commit validation
- Changelog generation tools

## Pull Request Guidelines

### Scope and Size

- Keep pull requests focused and small
- One logical change per pull request
- Changes should typically affect only one module

For changes affecting multiple modules:

1. **Single Logical Change**: If the change is inherently cross-module (e.g., removing a deprecated tool), submit as one PR
2. **Multiple Changes**: If changes are independent (e.g., updating dependencies due to base image change), submit separate PRs

### Commit Messages

- Pull request titles MUST follow [Conventional Commits](https://www.conventionalcommits.org/) format
- Individual commits within PRs SHOULD follow Conventional Commits format
- We use squash merging, so the PR title will become the commit message

### Changelog

Every pull request MUST include a changelog entry following the [Keep a Changelog](https://keepachangelog.com/) specification:

- Group changes under Added, Changed, Deprecated, Removed, Fixed, or Security
- Use present tense ("Add feature" not "Added feature")
- Reference relevant issues or PRs

Example:

```markdown
## Changelog
### Added
- New Python template with poetry support (#123)

### Changed
- Update base Debian image to 12.2 (#124)

### Security
- Remove deprecated SSL configuration (#125)
```
