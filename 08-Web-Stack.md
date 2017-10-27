# Web Stack

The following are the tools to get up and coding wordpress sites locally.

## Valet

First, assuming that composer has been installed correctly, run:

	composer global require laravel/valet
	
Once installed, run:

	valet install
	
This will install valet and start `dnsmasq` at which point you should be run `ping foobar.dev` and get a return of 127.0.0.1 which indicates valet is installed properly.

With valet installed you can now `cd` into a project's intended webroot and run `valet link domainname` for example:

	cd ~/Sites/foobar.com/public_html
	valet link foobar
	
	A [foobar] symbolic link has been created in [~/.valet/Sites/foobar].
	
At which point you should be able to visit http://foobar.dev in your browser and see *something*.

## MySQL

If you are developing a site that utilizes a mysql database and you've already **A)** installed **mariadb** or **mysql** via homebrew and **B)** installed the **Sequal Pro** app.

1. Open up Sequal Pro
2. Enter your primary database information, which is likely:
	* **Host:** 127.0.0.1
	* **Username:** root
	* **Password:** (empty by default)
3. Create a new database for your local dev site
4. Create a new user called **localdev** under the "Users" menu 
5. While keeping the **localdev** user selected, under "Schema Privileges" move all "Available Privileges" to "Granted Privileges"

## Bedrock

More to come on this, but bedrock is hands down the best setup for wordpress. It keeps your database credentials secure, separates vendor code from custom code, and allows you to use composer to manage your wordpress plugins *with ease*

For more info see [https://github.com/roots/bedrock](https://github.com/roots/bedrock)

## Capistrano
More to come on this.. Capistrano is a ruby server management tool that we use for deploying websites. Can be configured to work with any server that you have SSH access to.

For more info see: [https://github.com/capistrano/capistrano](https://github.com/capistrano/capistrano) and [https://github.com/roots/bedrock-capistrano](https://github.com/roots/bedrock-capistrano) (note: bedrock's default capistrano configs must be tweaked to work with most hosts)