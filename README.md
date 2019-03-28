# venvwrapper

I use these to create and manage small one-off environments when I don't want something heavy-handed like Pipenv.

These are a few scripts for managing virtual environments. I know good solutions exist, and previously used `virtualenvwrapper`, but the time scripts would take to be sourced was annoying enough that I decided to quickly try out something myself. Of course, the functionality is much more limited, implementing exactly what I used `virtualenvwrapper` for and nothing more.

## Usage

To create a new virtual environment and activate it:

```
mkvenv VENV_NAME [-p PYTHON_VERSION]
```

In practice I only used the `-p` option (to select python version), so that's all this has.

To activate an existing (in `$HOME/.virtualenvs`) virtual environment:
```
workon VENV_NAME
```

To delete a virtual environment:
```
rmvenv VENV_NAME
```

Of course, these are only useful when sourced. For example, I have the lines

```zsh
source /usr/local/bin/mkvenv
source /usr/local/bin/workon
source /usr/local/bin/rmvenv
source /usr/local/bin/venv-completions
```

in my `.zshrc`. For `zsh`, it might also be necessary to include

```zsh
autoload bashcompinit
bashcompinit
```

to make the completions work.
