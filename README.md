# Data-file-merge Working Examples
This repo contains a set of working examples for merging JSON files via the DFM CLI/Python library.

## Usage

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