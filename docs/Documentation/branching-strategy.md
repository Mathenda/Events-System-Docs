# Branching Strategy

 GitFlow provides a structured approach to managing branches within a Git
 repository, facilitating parallel development, release management, and collaboration among developers.

## GitFlow Branching Strategy

We use the GitFlow branching strategy in this project. GitFlow is a branching model for Git, created by Vincent Driessen. It has attracted a lot of attention because it is very well suited to collaboration and scaling the development team.

### Main Branches

The main branches in GitFlow are `main` and `develop`:

- `main`: This branch contains the official release history. An update in this branch represents a new production release.
- `develop`: This branch is a pre-production branch where features are integrated.

### Supporting Branches

The supporting branches in GitFlow are Feature, Release, and Hotfix branches:

- `feature/*`: These are branches where new features are developed and merged into `develop`.
- `bug/*`: These are branches where non-critical bugs are fixed and merged into `develop`.
- `hotfix/*`: These are branches that act as an immediate production fix.
- `update/*`: These are branches where updates are made to the project structure or dependencies.

### Workflow

1. A `develop` branch is created from `main`.
2. A `feature/bug/hotfix/update` branch is created from `develop`.
3. When a feature/bug/hotfix/update is complete, it is merged into the `develop` branch.
4. When the `develop` branch has acquired enough features for a release, you can create a pull request from `develop` into `main`.
5. If an issue in `main` is detected, a `hotfix` branch is created from `main`.
6. Once the `main` is complete, it should be merged to both `main` and `develop`.

## Contributing

To contribute to this project, you can create a new branch based on the type of change you're making. The branch should be named `feature/<feature-name>`, `bug/<bug-name>`,`update/<update-name>` or `hotfix/<hotfix-name>`. After making your changes, open a pull request to merge your branch into the appropriate base branch (`develop` for features and hotfixes, `master` for releases).