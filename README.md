# venvwrapper

These are a few scripts for managing virtual environments. I know good solutions exist, and previously used `virtualenvwrapper`, but the scripts would take to be sourced was annoying enough that I decided to quickly try out something myself. Of course, the functionality is much more limited, implementing exactly what I used `virtualenvwrapper` for and nothing more.

## Usage

To create a new virtual environment:

```
mkvenv VENV_NAME [-p PYTHON_VERSION]
```

In practice I only used the `-p` option, so that's all this has.

To activate an existing (in `$HOME/.virtualenvs`) virtual environment:
```
workon VENV_NAME
```

To delete a virtual environment
```
rmvenv VENV_NAME
```

Of course, these are only useful when sourced/in the path. `mkvenv` is python script, so that can be placed in `/usr/local/bin` or added to `$PATH`. `workon` and `rmenv` should be sourced in a `.bashrc` or `.zshrc`. Perhaps I'll rewrite `mkvenv` as a bash script for consistency, at some later point.
