# Labeling Github repositories with actions
I couldn't find any great examples of using Actions to declarate and automate Github labeling, so I made one myself.

## Creating / modifying / deleting labels
- Labels are declaritively defined in [`labels.yml`](./.github/labels.yml)
- Labels are modified in the Github respoitory [`push-labels-to-github.yml`](.github/workflows/push-labels-to-github.yml) on push. [See the labels](https://github.com/scowalt/actions-labeler-example/labels) that get created for the repository!
- PR Changes to `labels.yml` are validated with [`sync-labels-PR-validation.yml`](.github/workflows/sync-labels-PR-validation.yml). [This pull request](https://github.com/scowalt/actions-labeler-example/pull/1) demonstrates this in action.
- [`import-labels-from-github.yml`](.github/workflows/import-labels-from-github.yml) will open a PR on the repository if any changes are made.

## Automatically labeling PRs
- [`labeler.yml`](.github/labeler.yml) defines the rules for labeling PRs.
- [`pr-labeler.yml`](.github/workflows/pr-labeler.yml) is the action that labels PRs.
