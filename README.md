# Labelling Github repositories with actions

## Adding labels to Github
1. Labels are declaritively defined in [`labels.yml`](./.github/labels.yml)
2. Labels are created in [`sync-labels.yml`](./.github/workflows/sync-labels.yml)
3. [See the labels](https://github.com/scowalt/actions-labeler-example/labels) that get created for the repository!
4. Changes to `labels.yml` are validated with [`dryrun-sync-labels.yml`](./.github/workflows/dryrun-sync-labels.yml)
