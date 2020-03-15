# commonly-used-commands

Installing jupyterlab in ubuntu
```
sudo apt install python-pip python3-pip
pip install jupyterlab
pip3 install jupyterlab
```

It requries log off then log on to get jupyterlab in path. If you want to use it immediatly, use `~/.local/bin/jupyter lab`

Sometimes following error comes `Failed validating schema (@jupyterlab/apputils-extension:package`

Rebuilding jupyterlab will fix it
`jupyter lab clean; and jupyter lab build`
Ref: https://stackoverflow.com/questions/57260338/what-is-a-failed-validating-schema-jupyterlab-apputils-extensionpackage-in

To start: `jupyter lab --no-browser`

To fix issue when wrong pyrhon interpreter is being used by jupyterlab
Fix python interpreter path in `/home/<user>/.local/share/jupyter/kernels/python<2/3>/kernel.json`
