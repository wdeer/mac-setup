## Install xcode

Download xcode from the mac app store and open to start installing the necessary command line tools.

## Install .yadr

YADR (Yet Another Dotfile Repo) installs homebrew, zsh, and all sorts of cool bells and whistles


## Check Homebrew
run `brew doctor` to see if there are any issues, if there are follow the provided instructions.

Cant chown /usr/local ? [click here](https://github.com/Homebrew/brew/issues/3228#issuecomment-332679274)

If you have already migrated your ssh key you can feel free to continue, if not let's create one.


## SSH Keys
In order to connect to any of our LiquidWeb, Eleven2, or DigitalOcean servers over SSH/SFTP or commit to our Think Patented Github you must first have an SSH Key installed in your **~/.ssh/** directory.

To generate a key, paste the following in a terminal session:

	cd ~/.ssh && ssh-keygen -t rsa -b 4096 -C "youremailaddress@thinkpatented.com"

You will be asked to name the key, don't and just hit `enter` to leave as default **id_rsa** this will insure that any provided config files are pointing to the appropriate key. You will also be asked to provide a passphrase for the key, this is optional but recommended for an additional layer of security.

When the key has been created there will be two files (**id_rsa** and **id_rsa.pub**) The .pub file is your public key and can be shared freely. The non .pub file is your **private** key and should **NEVER NEVER NEVER** be shared. Send the **id_rsa.pub** file to the Lead Development Coordinator (Wes Deer) for inclusion as an authorized key on any appropriate servers.

note: If you are encountering any issues connecting to a server, re-run the ssh command and include the "-v" flag to get verbose output which will provide more details on what is causing the issue. If you are unable to diagnose the issue yourself send the verbose output to the Lead Development Coordinator (Wes Deer) for further diagnosis and to insure your SSH key has been added as an authorized key on the server.
