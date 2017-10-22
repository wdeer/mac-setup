# TROUBLESHOOTING
## Issues typically occuring after a fresh install:
### I keep getting "command not found" when trying to run any of the following: node, bower, npm, yarn, composer, cap, python, ruby.

If this is occurring on your local machine it could be that rbenv, nodenv, pyenv, and/or composer are not initializing when you start a new terminal session.

First determine which shell you have installed by running `which ${SHELL}`
**Bash** is the default installed by MacOS, but you should be using **Zsh**. If you installed .yadr this should have been installed and set automatically. If not, insure that zsh is installed and your shell has been changed to use it by default.

If that doesn't immediately address the issue you should also insure that you have followed the instructions in **Environment Management tools** and a **.zshrc** file in your home directory that contains the following:

	export PATH="$HOME/.rbenv/bin:$PATH"
	export PATH="$HOME/.nodenv/bin:$PATH"
	export PATH="$HOME/.pyenv/bin:$PATH"
	export PATH="$PATH:$HOME/.composer/vendor/bin"
	
	eval "$(rbenv init -)"
	eval "$(nodenv init -)"
	eval "$(pyenv init -)"

## Getting a weird "[process completed]" or "Broken Pipe" error after I tried to get too fancy and borked up my dotfiles?

Well you've really went and done it.. it appears the order in which yadr tells zsh to source files is out of whack.. Fear not, the easiest fix is as follows:

1. back up your current ~/.yadr directory to yadr.bak (since you borked your terminal you'll probably have to do this via Finder)
2. Set Terminal or iTerm to open Bash:
	* In iTerm: Go to "Preferences > Profile > General" Then select "Command" under **Command** and enter `/bin/bash -l` Then open a new iTerm window that will automatically open with Bash.
	* In Terminal: Go to "Shell (In Menu Bar) > New Command" Then enter `/bin/bash -l` which will spawn a new window using Bash
3. Open Xcode.app and you will likely be prompted to reinstall command line tools, do it.
4. Once command line tools have reinstalled, run the .yadr install script 

	**sh -c "\`curl -fsSL https://raw.githubusercontent.com/wdeer/dotfiles/master/install.sh \`"**

5. Then you should be up and running again.. carefully migrate any yadr settings from your backup (you'll bare minimum have to copy the contents of your ~/.zshrc)

**note:** if you ran the above steps in **iTerm** then you'll need to reset the Command setting under "Preferences > Profile > General" back to "Login Shell"