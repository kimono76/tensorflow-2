# Jupyter Notebooks in the terminal

```sh 
pip install ipykernel 
pip install nbterm 

``` 
### Add nbterm to PATH
edit ~/.zshrc

```sh
export PYTHONPATH="${PYTHONPATH}:/$HOME/.local/bin/nbterm"

alias ll="ls -la"
alias nb="nbterm"

```
