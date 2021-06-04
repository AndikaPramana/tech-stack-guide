## Install python on mac and configure which version to use
1. Install brew 
	- `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
2. Remove old python instalation first for clean install 
	- `sudo rm /usr/local/bin/python*`	==> for removing python 
	- `sudo rm /usr/local/bin/pip*`		==> for removing pip
	- `sudo rm -Rf /Library/Frameworks/Python.framework/Versions/*` ==> for removing python frameworks
3. Because we are going to use multiple different version of python, then using pyenv is recommended
	- `brew install pyenv`
4. See the list of python version 
	- `pyenv install --list | grep " 3\.[678]"`
5. Install the version of python using pyenv
	- `pyenv install -v 3.6.5`
6. then we can see which version of python is installed
	- `which python`
7. python has 2 version: python 2.7 and python 3, and we can make alias to refer python as python3
	- `alias python=python3`
8. Choose global version of python through pyenv
	- `pyenv global 3.6.5` 
9. Choose local version of python through pyenv
	- `pyenv local 3.6.5`
10. UPDATE from may 2021
	- add these to bash profile (.zshrc or .bashrc)
	- `export PYENV_ROOT="$HOME/.pyenv"
	   export PATH="$PYENV_ROOT/bin:$PATH"
	   if command -v pyenv 1>/dev/null 2>&1; then
	   	eval "$(pyenv init --path)"
	   fi`	
