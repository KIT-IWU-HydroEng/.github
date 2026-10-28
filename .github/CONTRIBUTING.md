# Contributing

Thank you for your interest in contributing to the software of the **Hydraulic Engineering and Water Resources Management** group at the [Institute for Water and Environment (IWU)](https://www.iwu.kit.edu/wb/index.php), [Karlsruhe Institute of Technology (KIT)](https://www.kit.edu).

These guidelines apply to all repositories of this organization. Individual repositories may have their own `CONTRIBUTING.md` with additional or more specific rules; where they exist, those take precedence.

## Ways to contribute

- **Report bugs**: open an issue describing the problem, the steps to reproduce it, the expected and the actual behaviour, and your environment (operating system, software versions).
- **Suggest improvements**: open an issue explaining the idea and the use case behind it.
- **Improve documentation**: corrections and clarifications are always welcome.
- **Contribute code**: fix bugs, add features or tests via pull requests.

Before starting larger changes, please open an issue first so the scope can be discussed with the maintainers.

## Workflow

1. Fork the repository (external contributors) or create a branch (group members).
2. Create a descriptively named branch from the default branch, e.g. `fix/sediment-input-parsing` or `feature/wood-transport-export`.
3. Make your changes in small, focused commits whose messages follow the [commit message convention](#commit-messages).
4. Make sure existing tests pass and add tests for new functionality where applicable. Many repositories run automated checks on every pull request (e.g. pull request title, citation file, links, license, tests); these must pass before merging.
5. Update the documentation if your change affects usage.
6. Open a pull request against the default branch, describing what was changed and why, and referencing related issues (e.g. `Closes #12`). The pull request title must also follow the commit message convention, as it is used as the commit message when pull requests are squash-merged.
7. A maintainer will review the pull request. Please be responsive to feedback; changes may be requested before merging.

## Commit messages

All commit messages must follow the [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) specification:

```text
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

- **type** describes the kind of change. Use one of:

  | Type       | Use for                                                          |
  | ---------- | ---------------------------------------------------------------- |
  | `feat`     | a new feature                                                    |
  | `fix`      | a bug fix                                                        |
  | `docs`     | documentation only                                               |
  | `style`    | formatting that does not change the code's meaning               |
  | `refactor` | code changes that neither fix a bug nor add a feature            |
  | `perf`     | performance improvements                                         |
  | `test`     | adding or correcting tests                                       |
  | `build`    | the build system or dependencies                                 |
  | `ci`       | continuous integration configuration                             |
  | `chore`    | other maintenance that does not touch source code or tests       |
  | `revert`   | reverting an earlier commit                                      |

- **scope** (optional) names the part of the code affected, in parentheses, e.g. `fix(sediment): ...`.
- **description** is a short summary in the imperative mood ("add", not "added" or "adds"), starting in lowercase and without a full stop at the end.
- **body** (optional) explains what changed and why, separated from the description by a blank line.
- **footer** (optional) references issues (e.g. `Refs: #12`) or other metadata.
- **Breaking changes**, i.e. changes that break existing usage such as input formats, interfaces or default parameters, are marked with `!` after the type or scope and/or a `BREAKING CHANGE:` footer.

Examples:

```text
feat(wood): add export of wood transport rates to CSV
```

```text
fix(hydraulics): correct unit conversion of discharge from l/s to m³/s

The discharge was divided by 100 instead of 1000, which overestimated
flow velocities in the compound channel cases.

Refs: #42
```

```text
feat(io)!: change default output format to NetCDF

BREAKING CHANGE: results are no longer written as plain text files by default.
Use `--format txt` to keep the previous behaviour.
```

## Code guidelines

- Follow the style and conventions already used in the repository.
- Write readable code and comment non-obvious steps, especially physical assumptions, units and numerical choices.
- Do not commit large raw datasets, model outputs, credentials or personal data. Use the data-sharing approach described in the respective repository instead.
- Keep dependencies to a minimum and declare any new ones in the repository's dependency files.

## Research data and scientific integrity

Many repositories accompany scientific publications. When contributing:

- Do not change results-relevant code silently; document changes that may affect published results.
- Cite sources for methods, equations or code adapted from other work.
- If you use our software in your research, please cite it as indicated in the respective repository (e.g. a `CITATION.cff` file or the README).

## Licensing

By contributing, you agree that your contributions are licensed under the license of the respective repository. See [LICENSING.md](https://github.com/KIT-IWU-HydroEng/.github/blob/main/.github/LICENSING.md) for more information.

## Code of conduct

Everyone participating in our repositories is expected to follow our [Code of Conduct](https://github.com/KIT-IWU-HydroEng/.github/blob/main/.github/CODE_OF_CONDUCT.md).

