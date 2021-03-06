## Install xcode

Download xcode from the mac app store and open it to start installing the necessary command line tools.

## Install .yadr

There are a wealth of dotfile repos out there, YADR (Yet Another Dotfile Repo) being a tremendously popular option. YADR installs homebrew, zsh, and all sorts of cool bells and whistles. 
It is recommended that you first fork https://github.com/skwp/dotfiles into your own github account then run the following in your terminal(replacing "skwp" with your own github username):

	sh -c "`curl -fsSL https://raw.githubusercontent.com/skwp/dotfiles/master/install.sh `"

For mor information on yadr and cutomizations see [https://github.com/skwp/dotfiles](https://github.com/skwp/dotfiles)

## Check Homebrew
Once yadr has installed, run `brew doctor` to see if there are any issues with homebrew, if there are follow the provided instructions to correct them.

Cant chown /usr/local ? [click here](https://github.com/Homebrew/brew/issues/3228#issuecomment-332679274)

If you have already migrated your ssh key you can feel free to continue, if not let's create one.


## SSH Keys
In order to connect to any of our LiquidWeb, Eleven2, or DigitalOcean servers over SSH/SFTP or commit to our Think Patented Github you must first have an SSH Key installed in your **~/.ssh/** directory.

To generate a key, paste the following in a terminal session:

	cd ~/.ssh && ssh-keygen -t rsa -b 4096 -C "youremailaddress@thinkpatented.com"

You will be asked to name the key, don't and just hit `enter` to leave as default **id_rsa** this will insure that any provided config files are pointing to the appropriate key. You will also be asked to provide a passphrase for the key, this is optional but recommended for an additional layer of security.

When the key has been created there will be two files (**id_rsa** and **id_rsa.pub**) The .pub file is your public key and can be shared freely. The non .pub file is your **private** key and should **NEVER NEVER NEVER** be shared. Send the **id_rsa.pub** file to the Lead Development Coordinator (Wes Deer) for inclusion as an authorized key on any appropriate servers.

note: If you are encountering any issues connecting to a server, re-run the ssh command and include the "-v" flag to get verbose output which will provide more details on what is causing the issue. If you are unable to diagnose the issue yourself send the verbose output to the Lead Development Coordinator (Wes Deer) for further diagnosis and to insure your SSH key has been added as an authorized key on the server.

## Git
You'll need to set your git username globally so that all repo configs default to your username:

run:

	git config --global user.name "YOUR.USERNAME"
	git config --global user.email "youremail@address.com"

Also, under your github's account settings you should add in your SSH key (id_rsa.pub) after which you can test your connection / add github to your "known\_hosts" by running:

	ssh -T git@github.com

If this is the first time you've tried connecting to Github over SSH you'll be prompted to add it to your known\_hosts, select **yes**.

## MacOS Defaults

There are a number of things you can do to fine tune your Mac.. Some adjustments can be handled by digging through preferences, but many must be ran as a terminal command. Here is a pretty well maintained and currated list of such tweaks: [https://github.com/kevinSuttle/macOS-Defaults](https://github.com/kevinSuttle/macOS-Defaults/blob/master/.macos) 

**note**: Instead of simply executing the .macos file, it is recommended that you go through the file and manually run commands only for the changes that you want.

## TP Stuff

### Forticlient
In order to VPN into thinkpatented you must use forticlient to do so. First try to run `brew cask search forti` (assumming you've already installed .yadr which installed homebrew) if nothing is found then just head on over to [http://www.forticlient.com/downloads](http://www.forticlient.com/downloads) to grab the installer.

Once installed enter the following settings:

* **VPN Type:** SSL VPN
* **Remote Gateway:** 66.148.163.130
* **Cusomized Port:**	65443
* **Username:** yourthinkpatentedusername

After that you should be good to go. If you are trying to get to Monarch Web visit the following url [http://10.20.32.12/scripts/cgiip.exe/WService=wsgams1/sfws/sflogin.w](http://10.20.32.12/scripts/cgiip.exe/WService=wsgams1/sfws/sflogin.w)

### Printers
At the moment, see Louie (IT) for this.. more detailed instructions to come
