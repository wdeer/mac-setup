#Environment Management tools

## RBENV

First, go to [ruby-lang.org](https://www.ruby-lang.org/en/downloads/) to find out the latest stable version of ruby (2.4.2 at the time of writing)

make sure the following has been added to your **~./zshrc** `export PATH="$HOME/.rbenv/bin:$PATH"` and `eval "$(rbenv init -)"`


	rbenv install 2.4.2
	rbenv global 2.4.2
	
For more information on using rbenv, **run** `rbenv --help` or go to [github.com/rbenv/rbenv](https://github.com/rbenv/rbenv) for further documentation

## NODENV

First, go to [nodejs.org](https://nodejs.org/en/) to find out the latest stable LTS(Long Term Support) version of node (6.11.4 at the time of writing)

make sure the following has been added to your **~./zshrc** `export PATH="$HOME/.nodenv/bin:$PATH"` and `eval "$(nodenv init -)"`

	nodenv install 6.11.4
	nodenv global 6.11.4
	
For more information on using nodenv, **run** `nodenv --help` or go to [github.com/nodenv/nodenv](https://github.com/nodenv/nodenv) for further documentation

## PYENV

First, go to [python.org](https://www.python.org/downloads/) to find out the latest stable version of **Python 2.\*\*** (2.7.14 at the time of writing)

make sure the following has been added to your **~./zshrc** `export PATH="$HOME/.pyenv/bin:$PATH"` and `eval "$(pyenv init -)"`

	nodenv install 2.7.14
	nodenv global 2.7.14
	
For more information on using nodenv, **run** `nodenv --help` or go to [github.com/nodenv/nodenv](https://github.com/nodenv/nodenv) for further documentation


## PHPBREW

First, go to [php.net](http://php.net/downloads.php) to find out the current stable version of PHP.

	phpbrew lookup-prefix homebrew
	phpbrew self-update
	phpbrew install next as php-7.1.10 +default+mysql+mcrypt+openssl+debug+sqlite	phpbrew use php-7.1.10
	
For more information about using phpbrew, **run** `phpbrew --help` or go to [github.com/phpbrew/phpbrew](https://github.com/phpbrew/phpbrew) for further documentation

### Composer

make sure the following has been added to your **~./zshrc** `export PATH="$PATH:$HOME/.composer/vendor/bin"`

	phpbrew app get composer
	composer global require laravel/valet

## Profile
By this point in time you should have a **~/.zshrc** file that looks similar to this:

	export PATH="$HOME/.rbenv/bin:$PATH"
	export PATH="$HOME/.nodenv/bin:$PATH"
	export PATH="$HOME/.pyenv/bin:$PATH"
	
	eval "$(rbenv init -)"
	eval "$(nodenv init -)"
	eval "$(pyenv init -)"
		
	export PATH="$PATH:$HOME/.composer/vendor/bin"
	
	