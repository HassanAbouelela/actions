# Contributing Guidelines
Thanks for your interest in helping open source projects!

To start contributing to this project, find an issue you'd like to tackle.
If there is no issue for what you want to contribute to, feel free to make one!

Once you've found an issue, leave a comment specifying that you'd like to work on it,
as well as any additional details you think are relevant.
Once you're assigned, you're free to work on it.

See [here](#project-information) for information about the general project structure.
See [here](#process) for the process to get your changes merged.


## Process
Once you're assigned to an issue, your contribution will follow a
standard [fork and pull][fork-pull] model:
1. [Fork][fork] this repository using the button at the top of the GitHub UI.
2. Push changes to a branch on your fork.
3. Open a [pull request][pr] to this repository with your changes.
4. Your code will be reviewed.
    1. If changes are requested, push the requested changes to your branch, and ask for another review.
    2. If no changes are requested, and your work is approved, congrats! It should hopefully be merged in soon.


## Project Information
This section covers some basics about the general structure of the project.

This project uses pre-commit to maintain style. Use `python -m pip install pre-commit`,
followed by `pre-commit install` to set it up.  It'll run whenever you try to commit.


Each action in this project is split into its own folder.
The name of the folder is the name of the action.
At the bare minimum, the folder will contain an `action.yaml` file, and a `README.md` file.
The `action.yml` defines the actual instructions that'll be run from this script,
while the README serves as documentation for the script.


Each action should have a test suite defined for it in the [workflows](./workflows) folder,
where applicable. These tests will automatically run when you open a PR.

This project follows [semver][semver] for versioning.
Please make sure to follow it if you try to bump a version.



[fork-pull]: https://docs.github.com/en/github/collaborating-with-pull-requests/getting-started/about-collaborative-development-models#fork-and-pull-model
[fork]: https://docs.github.com/en/get-started/quickstart/fork-a-repo
[pr]: https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork
[semver]: https://semver.org/
