# Setup Python [![Tests][badge]][link]
This is a composite action which installs python and poetry,
installs your dependencies, and manages caching for them.
It also handles caching of pre-commit if you happen to be using that.

## Usage
### Example
You can use this action as follows:
```yaml
- name: Install Python Dependencies
  uses: HassanAbouelela/actions/setup-python@setup-python_v1.6.0
  with:
    install_args: "--without dev"
    python_version: '3.10'
```

### Inputs
The following inputs can be used to configure the action:

| Name             | Type   | Default | Description                                                                                                                                          |
|------------------|--------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| python_version   | string |         | Specify the python version passed to the `actions/setup-python` action.                                                                              |
| poetry_version   | string | poetry  | The version of poetry to install and use. This is passed directly to pip, so you can specify any pattern, such as `poetry~=1.2` or `poetry==1.1.15`. |
| working_dir      | path   | `.`     | The directory to run the `poetry install` command in. By default, this will just be the root directory.                                              |
| use_cache        | bool   | true    | Enable or disable the usage of cache, even if it is available.                                                                                       |
| cache_pre-commit | bool   | true    | Enable caching and restoring pre-commit installs. Only a pre-commit config at the root workspace will be cached properly.                            |
| install_args     | string |         | A string placed after the `poetry install` command, which can contain extra options.                                                                 |
| checkout         | bool   | true    | Perform a checkout of the repository in the action. If this is false, this must be done manually before running the action.                          |
| python_cmd       | string | python  | The python command to be used. This is incompatible with `python_version`.                                                                           |
| dev (deprecated) | bool   | true    | This argument is deprecated. Please use `install_args` with the appropriate options. This option will be removed in the next major release.          |

### Outputs
The following outputs are produced by the action:

| Name           | Type   | Description                                       |
|----------------|--------|---------------------------------------------------|
| cache-hit      | bool   | True if a cache was used to restore dependencies. |
| python-version | string | The full Python semver version used.              |


[badge]: https://img.shields.io/github/actions/workflow/status/HassanAbouelela/actions/test_setup_python.yaml?label=Tests&branch=main
[link]: https://github.com/HassanAbouelela/actions/actions/workflows/test_setup_python.yaml?query=branch%3Amain
