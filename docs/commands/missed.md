# **missed**: rules without matching plugins

Show keys from `[tool.flakeheaven.plugins]` that has no matched installed plugins. Exitcode of this command is equal to the number of missed plugins. For example:

```toml
[tool.flakeheaven.plugins]
pycodestyle = ["+*"]
"flake8-*" = ["+*"]
```

If you have installed only `pyflakes` and `pycodestyle`, command `flakeheaven missed` will show `flake8-*`. If you have also installed `flake8-commas`, the command will have the empty output.
