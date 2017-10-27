# Web Stack

The following are the tools to get up and code wordpress sites.

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
	* **Password:** (empty)
3. Create a new database for your site
4. 