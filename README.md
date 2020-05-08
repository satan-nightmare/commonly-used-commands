# commonly-used-commands

# Installations

## Jupyterlab
```
sudo apt install python-pip python3-pip
pip install jupyterlab
pip3 install jupyterlab
```
To start: `jupyter lab --no-browser`

Note: It requries log off then log on to get jupyterlab in path. If you want to use it immediatly, use `~/.local/bin/jupyter lab`

### Issues

1. `Failed validating schema (@jupyterlab/apputils-extension:package`

Rebuilding jupyterlab will fix it
`jupyter lab clean; and jupyter lab build`
Ref: https://stackoverflow.com/questions/57260338/what-is-a-failed-validating-schema-jupyterlab-apputils-extensionpackage-in

2. Wrong python interpreter is being used by jupyterlab

Fix python interpreter path in `/home/<user>/.local/share/jupyter/kernels/python<2/3>/kernel.json`

3. In windows's WSL, permission error is thrown when running from user directories e.g. Dowcuments, Music, etc.

To fix, either run jupyter from a linux directory e.g. `/home/<user>/<some path>` or from some manully made directory in windows drive
Ref: https://github.com/Microsoft/WSL/issues/3608

## Virtual environment related issues

1. When using fish shell, `source <env>/bin/activate` throws error

Use following command instead `. <env>/bin/activate.fish`
Ref: https://stackoverflow.com/questions/10956335/how-to-get-virtualenv-to-work-with-fish-shell
