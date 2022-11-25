# Setup Python [![Tests][badge]][link]
This is a composite action which installs python and poetry,
installs your dependencies, and manages caching for them.
It also handles caching of pre-commit if you happen to be using that.

## Usage
### Example
You can use this action as follows:
```yaml
- name: Install Python Dependencies
  uses: HassanAbouelela/actions/setup-python@setup-python_v1.3.3
  with:
    dev: false
    python_version: '3.10'
```

### Inputs
The following inputs are required to use this action.

| Name             | Type   | Default | Description                                                                                                                                                                   |
|------------------|--------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dev              | bool   | false   | Indicate whether dev dependencies should be installed. If false, the `--no-dev` flag is passed to poetry. Despite having a default, it's good practice to explicitly set one. |
| python_version   | string |         | Specify the python version passed to the `actions/setup-python` action.                                                                                                       |
| poetry_version   | string | poetry  | The version of poetry to install and use. This is passed directly to pip, so you can specify any pattern, such as `poetry~=1.2` or `poetry==1.1.15`.                          |
| working_dir      | path   | `.`     | The directory to run the `poetry install` command in. By default, this will just be the root directory.                                                                       |
| use_cache        | bool   | true    | Enable or disable the usage of cache, even if it is available.                                                                                                                |
| cache_pre-commit | bool   | true    | Enable caching and restoring pre-commit installs. Only a pre-commit config at the root workspace will be cached properly.                                                     |
| install_args     | string |         | A string placed after the `poetry install` command, which can contain extra options.                                                                                          |

### Outputs
The following outputs are produced by the action:

| Name           | Type   | Description                                       |
|----------------|--------|---------------------------------------------------|
| cache-hit      | bool   | True if a cache was used to restore dependencies. |
| python-version | string | The full Python semver version used.              |


[badge]: https://img.shields.io/github/workflow/status/HassanAbouelela/actions/Test%20Setup-Python/main?label=Tests
[link]: https://github.com/HassanAbouelela/actions/actions/workflows/test_setup_python.yaml?query=branch%3Amain
