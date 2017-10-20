# Brew Packages

## Install Homebrew
The following requires homebrew already be installed, if you have not yet done so paste the following script in terminal and then you can get to brewing!

	/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	
## Brew install these packages

	brew install rbenv pyenv nodenv the_silver_searcher ack z zsh awscli wget wpcli-completion dnsmasq git-town tree sqlite mariadb mcrypt nginx shellcheck pngquant mozjpeg tmux reattach-to-user-namespace wpcli-completion
	
	brew install homebrew/php/composer homebrew/php/phpbrew homebrew/php/wp-cli

and install ffmpeg separately with some additional tools:

	brew install ffmpeg --with-faac --with-libssh --with-libvorbis --with-libvpx --with-openssl --with-opus --with-theora --with-webp --with-x265
	
and install yarn without node so we can use the version of node that we'll install with nodenv
	
	brew install yarn --without-node


## What did you just install!!!??

### Environment Management
* **[rbenv](https://github.com/rbenv/rbenv):** allows for managing multiple ruby versions and environments, command: `rbenv`
* **[pyenv](https://github.com/pyenv/pyenv):** allows for managing multiple python versions and environments, command: `pyenv`
* **[nodenv](https://github.com/nodenv/nodenv):** allows for managing multiple node versions and environments, command: `nodenv`
* **[phpbrew](https://github.com/phpbrew/phpbrew):** allows for managing multiple php versions and environments, command: `phpbrew`


### Helpful Tools
* **[zsh](https://www.zsh.org/):** Zsh is just a more awesome bash without having to learn anything new. Automatic spell correction for your commands, syntax highlighting, and more
* **[the\_silver\_searcher](https://github.com/ggreer/the_silver_searcher):** Fast cli code searching, command: `ag`
* **[ack](https://beyondgrep.com/):** More complex but fast cli code searching, command: `ack`
* **[wget](https://www.gnu.org/software/wget/):** Alternative to `curl`, command: `wget`
* **[wp-cli](https://wp-cli.org/):** Wordpress command line, command: `wp`
* **[wpcli-completion](https://github.com/wp-cli/wp-cli):** Auto-complete wp-cli
* **[z](https://github.com/rupa/z):** 1000000x faster cli navigation than `cd`, command: `z`
* **[awscli](https://aws.amazon.com/cli/):** Command line access to aws services, command: `aws`
* **[yarn](https://yarnpkg.com/):** Better than `npm`, command: `yarn`
* **[tree](http://mama.indstate.edu/users/ice/tree/):** Quickly see the current directory's structure including children, command: `tree`
* **[git-town](http://www.git-town.com/):** Many many many helpful git commands, see: https://github.com/Originate/git-town#commands
* **[shellcheck](https://www.shellcheck.net/):** Shell script linter/tester, command: `shellcheck`
* **[pngquant](https://pngquant.org/):** Shrink PNGs, command: `pngquant`
* **[mozjpeg](https://github.com/mozilla/mozjpeg):** Shrink JPGs, command: `jpegtran`
* **[tmux](https://github.com/tmux/tmux/wiki):** Allows for terminal multiplexing
* **[reattach-to-user-namespace](https://github.com/ChrisJohnsen/tmux-MacOSX-pasteboard):** fixes issue with using mac clipboard in tmux sessions


### Web Stack
* **[dnsmasq](http://www.thekelleys.org.uk/dnsmasq/doc.html):** Allows for ".dev" TLDs for local dev testing
* **[nginx](https://nginx.org/):** Nginx webserver
* **[sqlite](https://sqlite.org/):** SQLite DB
* **[mariadb](https://mariadb.org/):** MySQL DB
* **[mcrypt](http://mcrypt.sourceforge.net/):** Encryption functions used by php and webserver