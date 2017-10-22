#Environment Management tools

## RBENV

First, go to [ruby-lang.org](https://www.ruby-lang.org/en/downloads/) to find out the latest stable version of ruby (2.4.2 at the time of writing)

`brew install rbenv` if you haven't already, then make sure the following has been added to your **~./zshrc** `export PATH="$HOME/.rbenv/bin:$PATH"` and `eval "$(rbenv init -)"`

	rbenv install 2.4.2
	rbenv global 2.4.2
	
For more information on using rbenv, **run** `rbenv --help` or go to [github.com/rbenv/rbenv](https://github.com/rbenv/rbenv) for further documentation

## NODENV

First, go to [nodejs.org](https://nodejs.org/en/) to find out the latest stable LTS(Long Term Support) version of node (6.11.4 at the time of writing)

`brew install nodenv` if you haven't already, then make sure the following has been added to your **~./zshrc** `export PATH="$HOME/.nodenv/bin:$PATH"` and `eval "$(nodenv init -)"`

	nodenv install 6.11.4
	nodenv global 6.11.4
	
For more information on using nodenv, **run** `nodenv --help` or go to [github.com/nodenv/nodenv](https://github.com/nodenv/nodenv) for further documentation

## PYENV

First, go to [python.org](https://www.python.org/downloads/) to find out the latest stable version of **Python 2.\*\*** (2.7.14 at the time of writing)

`brew install pyenv` if you haven't already, then make sure the following has been added to your **~./zshrc** `export PATH="$HOME/.pyenv/bin:$PATH"` and `eval "$(pyenv init -)"`

	nodenv install 2.7.14
	nodenv global 2.7.14
	
For more information on using nodenv, **run** `nodenv --help` or go to [github.com/nodenv/nodenv](https://github.com/nodenv/nodenv) for further documentation

**NOTE:** On High Sierra you may run into an issue with OpenSSL not being found.. Adding the following alias somewhere in your $PATH (ie: **~/.zshrc**) will tell pyenv where to find the homebrew installed OpenSSL lib.

`alias pyenv='CFLAGS="-I$(brew --prefix openssl)/include" LDFLAGS="-L$(brew --prefix openssl)/lib" pyenv'`

## Composer

make sure the following has been added to your **~./zshrc** `export PATH="$PATH:$HOME/.composer/vendor/bin"`

	brew install homebrew/php/composer

## Profile (~/.zshrc)
By this point in time you should have a **~/.zshrc** file that looks similar to this:

	export PATH="$HOME/.rbenv/bin:$PATH"
	export PATH="$HOME/.nodenv/bin:$PATH"
	export PATH="$HOME/.pyenv/bin:$PATH"
	export PATH="$PATH:$HOME/.composer/vendor/bin"
	
	eval "$(rbenv init -)"
	eval "$(nodenv init -)"
	eval "$(pyenv init -)"
	
This will insure that your installed versions of ruby (via rbenv), node (via nodenv), python (via pyenv), and composer are all initialized and available every time you open a terminal session and avoid the dreaded "Command not Found"