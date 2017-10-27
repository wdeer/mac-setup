## SSH Keys
In order to connect to any of our LiquidWeb, Eleven2, or DigitalOcean servers over SSH/SFTP or commit to our Think Patented Github you must first have an SSH Key installed in your **~/.ssh/** directory.

To generate a key, paste the following in a terminal session:

	cd ~/.ssh && ssh-keygen -t rsa -b 4096 -C "youremailaddress@thinkpatented.com"

You will be asked to name the key, don't and just hit `enter` to leave as default **id_rsa** this will insure that any provided config files are pointing to the appropriate key. You will also be asked to provide a passphrase for the key, this is optional but recommended for an additional layer of security.

When the key has been created there will be two files (**id_rsa** and **id_rsa.pub**) The .pub file is your public key and can be shared freely. The non .pub file is your **private** key and should **NEVER NEVER NEVER** be shared. Send the **id_rsa.pub** file to the Lead Development Coordinator (Wes Deer) for inclusion as an authorized key on any appropriate servers.

note: If you are encountering any issues connecting to a server, re-run the ssh command and include the "-v" flag to get verbose output which will provide more details on what is causing the issue. If you are unable to diagnose the issue yourself send the verbose output to the Lead Development Coordinator (Wes Deer) for further diagnosis and to insure your SSH key has been added as an authorized key on the server.

## SSH Config
An SSH config file (~/.ssh/config) is a huge timesaver so make sure you have one:

Bare minimum:

	Host *
     ForwardAgent no
     ForwardX11 no
     ForwardX11Trusted yes
     Protocol 2
     ServerAliveInterval 60
     ServerAliveCountMax 30
     Port 22
     PubKeyAuthentication yes
     IdentityFile ~/.ssh/id_rsa
    
    ##Example Hosts
    Host examplewebsite.com examplewebsite example
    	HostName 111.111.11.11
    	User example
    
    Host examplewebsite2.com examplewebsite2 example2
    	HostName 111.111.11.11
    	User example2

Benefits are:

 * instead of typing `ssh example@111.111.11.11` everytime you want to SSH, you can simply type `ssh [hostname]`, for example:
  * `ssh examplewebsite.com`
  * `ssh examplewebsite`
  * `ssh example`
 * Apps like **Transmit** or the **Alfred's SSH Workflow** will automatically look at this file and use it's configs.

## Git
You'll need to set your git username globally so that all repo configs default to your username:

run:

	git config --global user.name "YOUR.USERNAME"
	git config --global user.email "youremail@address.com"

Also, under your github's account settings you should add in your SSH key (id_rsa.pub) after which you can test your connection / add github to your "known\_hosts" by running:

	ssh -T git@github.com

If this is the first time you've tried connecting to Github over SSH you'll be prompted to add it to your known\_hosts, select **yes**.

## AWS Credentials

In order to use the **awscli** or deploy any static sites to Amazon S3 you must first make sure your own AWS credentials are added to the **~/.aws/credentials** file.

**example:**

	[default]
	aws_access_key_id = ATOTALLYFAKEAWSKEYID
	aws_secret_access_key = thisisnotarealaccesskeysodownloadyourown

note: If you do not have a login for TP's AWS account see Lead Development Coordinator (Wes Deer)