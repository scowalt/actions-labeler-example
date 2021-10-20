# Labeling Github repositories with actions
I couldn't find any great examples of using Actions to declarate and automate Github labeling, so I made one myself.

## Creating / modifying / deleting labels
- [`labels.yml`](./.github/labels.yml) is where labels are declaritively defined
- [`push-labels-to-github.yml`](.github/workflows/push-labels-to-github.yml) modifies the repo labels on push. [See the labels](https://github.com/scowalt/actions-labeler-example/labels) that get created for the repository!
- [`sync-labels-PR-validation.yml`](.github/workflows/sync-labels-PR-validation.yml) validates PR Changes to `labels.yml`. [This pull request](https://github.com/scowalt/actions-labeler-example/pull/1) demonstrates this in action.
- [`import-labels-from-github.yml`](.github/workflows/import-labels-from-github.yml) will open a PR on the repository if any changes are made to labels through the UI. See [this action run](https://github.com/scowalt/actions-labeler-example/actions/runs/1364342155) and [the resulting PR](https://github.com/scowalt/actions-labeler-example/pull/5)

## Automatically labeling PRs
- [`labeler.yml`](.github/labeler.yml) defines the rules for labeling PRs.
- [`pr-labeler.yml`](.github/workflows/pr-labeler.yml) is the action that labels PRs. See [this pull request](https://github.com/scowalt/actions-labeler-example/pull/3) for an example
