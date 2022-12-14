# Data-file-merge Working Examples
This repo contains a set of working examples for merging JSON files via the [dfm CLI/Python library](https://github.com/ServerlessSam/data-file-merge).

## Usage

A current limitation in **dfm** is that you need to pass full local paths to files in the config files, excluding the leading `/`. This will be addressed in the project shortly. You will see placeholders `<REPLACE WITH YOUR LOCAL PATH TO THIS REPO EXCLUDING LEADING SLASH>` in each config file to replace before running.

### CLI
See [dfm install instructions](https://github.com/ServerlessSam/data-file-merge/wiki/Installation) for getting the CLI installed.

The CLI can be called using `dfm merge <path to config file>`. Note for some examples you may need to pass parameters using `-p key1=value1,key2=value2...`.

### Python
You can checkout the Python project [from GitHub](https://github.com/ServerlessSam/data-file-merge).

In a python shell (project supports Poetry) with the projects root directory in `PYTHONPATH` run the following:
```
from src.config import BuildConfig
cfg = BuildConfig.load_config_from_file("<path to config file>")
cfg.build()
```
Note for some examples you may need to pass parameter by adding a second argument to `load_config_from_file` of the form `{"ParameterKey1":"Value1", "ParamterKey2":"Value2"...}`.
