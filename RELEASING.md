## Release Process

This project uses [semantic-release](https://github.com/semantic-release/semantic-release) for automated versioning and CHANGELOG generation. The release process is triggered automatically when commits are pushed to the main branch.

### Commit Message Format

This project follows the [Conventional Commits](https://www.conventionalcommits.org/) specification. Commit messages should be structured as follows:

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

#### Types
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, etc)
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `build`: Changes that affect the build system or external dependencies
- `ci`: Changes to our CI configuration files and scripts
- `chore`: Other changes that don't modify src or test files

#### Examples

```
feat(api): add endpoint for sending messages
```

```
fix(web): resolve issue with message display
```

```
docs: update README with setup instructions
```

The commit type (feat, fix, etc.) determines how the version will be incremented:
- `feat`: Minor version bump (1.0.0 -> 1.1.0)
- `fix`, `perf`, `refactor`: Patch version bump (1.0.0 -> 1.0.1)
- `BREAKING CHANGE` in commit body: Major version bump (1.0.0 -> 2.0.0)