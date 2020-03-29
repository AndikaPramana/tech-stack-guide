## Install go on mac 
1. Install brew 
	- `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
2. Install go
	- `brew install golang`
3. Adding $GOPATH in bash_profile
	- `vim ~/.bash_profile`
	- `export GOPATH=$HOME/go`
4. Set the path where go will compiles and install tools
	- `export PATH=$PATH:$GOPATH/bin`

## Install go on Manjaro 
1. Update package manager database
	- `sudo pacman -Syu`
2. Install go 
	- `sudo pacman -S go`
3. Add go path (same as mac)