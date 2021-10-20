# Labeling Github repositories with actions
I couldn't find any great examples of using Actions to declarate and automate Github labeling, so I made one myself.

## Adding labels to Github
1. Labels are declaritively defined in [`labels.yml`](./.github/labels.yml)
2. Labels are modified in the Github respoitory [`sync-labels.yml`](./.github/workflows/sync-labels.yml) on push
3. [See the labels](https://github.com/scowalt/actions-labeler-example/labels) that get created for the repository!
4. Changes to `labels.yml` are validated with [`dryrun-sync-labels.yml`](./.github/workflows/dryrun-sync-labels.yml). https://github.com/scowalt/actions-labeler-example/pull/1 demonstrates this in action.
