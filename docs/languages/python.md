---
id: python
title: Python
---

## About
> Python is an interpreted, high-level and general-purpose programming language. Python's design philosophy emphasizes code readability with its notable use of significant whitespace. Its language constructs and object-oriented approach aim to help programmers write clear, logical code for small and large-scale projects.
> [(Wikipedia, 2020)](https://en.wikipedia.org/wiki/Python_(programming_language))

- [https://www.python.org/](https://www.python.org/)

## Getting Started
- [https://www.python.org/about/gettingstarted/](https://www.python.org/about/gettingstarted/)
- We highly recommend you to install and get familiar with the following tools before starting to work with python productively, they will save you a lot of time and problems.

### Pyenv (Python Version Management)
Manage multiple python versions comfortably
#### Installation
1. Install via [Homebrew](https://brew.sh)
```shell 
brew update
brew install pyenv
```
2.   **Add `pyenv init` to your shell** to enable shims and autocompletion.
   Please make sure `eval "$(pyenv init -)"` is placed toward the end of the shell
   configuration file since it manipulates `PATH` during the initialization.
```shell
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc
```
    
- **Bash note**: Modify your `~/.bash_profile` file instead of `~/.zshrc`.

3. Restart shell
```shell 
source ~/.zshrc
```

#### Download specific python version
```shell 
pyenv install 3.7.0
```

#### List available python versions
```shell 
pyenv versions
```

#### Activate a specific version locally
*This sets the Python version for the current folder and all subfolders.*
```shell 
pyenv local 3.7.0
```
#### Activate a specific version globally
```shell 
pyenv global 3.7.0
```


### Virtual environments
Don't clutter your global pip installation, use one virtual environment per project instead. \
**Important:** Create virtual environment in project folder
#### Create a virtual environment & activate it
```shell 
python3 -m venv venv 
source venv/bin/activate
```

#### Deactivate virtual environment
```shell 
deactivate
```

#### Create a  requirements file
```shell 
pip freeze > requirements.txt 
```

#### Install dependencies from a requirements file
```shell 
pip install -r requirements.txt 
```
    
#### Uninstall virtual environment
1. *(Optionally)* Deactivate venv
```shell 
deactivate
```
2. Remove venv folder
```shell 
rm -rf venv 
```
