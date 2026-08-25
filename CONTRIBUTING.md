# Contributing to Kiloloop Projects

Thank you for your interest in contributing!

Please read and follow our [Code of Conduct](CODE_OF_CONDUCT.md).

## How to Contribute

### Reporting Issues

- Use GitHub Issues on the relevant repository to report bugs or request features.
- Search existing issues before creating a new one.
- Include steps to reproduce for bug reports.

### Pull Requests

1. Fork the repository and create a feature branch from `main`.
2. Make your changes with clear, focused commits.
3. Run the project's quality checks before submitting (see the project README).
4. Open a PR against `main` with a clear description of what and why.
5. Check the repository's branch protections and contribution notes for any review or merge requirements before requesting merge.

### What We're Looking For

- Bug fixes with clear reproduction steps
- Documentation improvements
- Test coverage additions
- Feature proposals (open an issue first to discuss)

## Commit Messages

- Use imperative mood: "Add feature" not "Added feature"
- Keep the first line under 72 characters
- Reference issue numbers where applicable: "Fix validation bug (#42)"

## Changelog Entries

Repositories that keep a `CHANGELOG.md` follow [Common Changelog](https://common-changelog.org) discipline: a changelog answers "does this affect me, and how", not "how does it work".

- One line, one change — split a multi-facet feature into two or three scoped bullets rather than one long bullet.
- State the user-visible delta, not the implementation path.
- Do not inline flag enums or sub-mechanism walkthroughs — link the spec or doc section that carries the detail.
- One link per bullet, pointing at the best entry point.
- Each bullet must read as self-describing without its `### Added`/`### Changed` heading.

## License

By contributing, you agree that your contributions will be licensed under the project's license (typically Apache 2.0 — see the project's LICENSE file).
