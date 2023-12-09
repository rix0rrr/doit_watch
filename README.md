# doit_watch

A watch plugin for the Python task manager [doit](https://pydoit.org).

## How to use

Run `doit watch`, or `doit watch <TASK>`, to run the tasks once if
necessary, and then run them again when any of the input files change.

```sh
$ doit watch
.  MyTask
-> Watching 324 files for changes...
```

## How to install

To install, add the following to your config files:

```conf
# requirements.txt
doit-watch>=0.1.0
```

```conf
# pyproject.toml (if using)
[tool.doit.plugins.command]
watch = "doit_watch:Watch"
```

```conf
# doit.cfg (if using)
[COMMAND]
watch = "doit_watch:Watch"
```

## Credits

I didn't write this plugin myself. I took the source code of the
[doit-auto1](https://github.com/pydoit/doit-auto1) plugin, and
combined the [PR](https://github.com/pydoit/doit-auto1/pull/1) of
@bollwyvl and the [PR](https://github.com/pydoit/doit-auto1/pull/2) of
@jguillon into a new package, with the name that we all agree the
command should have.
