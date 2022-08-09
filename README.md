# Actions ![License] [![Semver-Logo]][Semver]
A repository to house all generic workflows used for my projects.

[Jump to action reference](#index).

### Usage
If you'd like to use these script in your own projects, the release name pattern is described below.
The inputs, outputs, and examples of each script are documented in the relevant script's directory
linked in the index below.

#### Release Name Pattern
> {name}_v{version}

Example:
> setup-python_v1.2.0


### Support Policy
This is just a hobby project, so I don't intend on providing any support promises.
I will contribute to this when I can. As this is an open source project
anyone is welcome to contribute directly, or fork and modify the project.


### Issues & Contributing
If you find a bug, have a feature request, or would like to contribute to the project,
open an issue here using one of the available templates.

Read more about contributing in the [contributing guidelines](.github/contributing.md).


### Index
An index of all the currently maintained scripts, their description, and the latest version.

| Name                           | Version | Status                        | Description                                          |
|--------------------------------|---------|-------------------------------|------------------------------------------------------|
| [Setup Python](./setup-python) | 1.2.0   | [![tests][sp_badge]][sp_link] | Setup a [poetry][Poetry]-managed python environment. |


[License]: https://shields.io/github/license/HassanAbouelela/actions
[Semver-Logo]: https://img.shields.io/badge/versioning-semver-informational
[Semver]: https://semver.org/
[Poetry]: https://python-poetry.org/

[sp_badge]: https://img.shields.io/github/workflow/status/HassanAbouelela/actions/Test%20Setup-Python/main?label=Tests
[sp_link]: https://github.com/HassanAbouelela/actions/actions/workflows/test_setup_python.yaml?query=branch%3Amain
