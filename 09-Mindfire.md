# Mindfire Marketing Studio

In order to get up and running with Mindfire's Marketing Studio you must first install silverlight `brew cask install silverlight`

After Silverlight has successfully installed head over to [http://mindfireinc.com/install](http://mindfireinc.com/install) to grab the installer package and run it.

*note: When the app installs it will likely drop it onto your Desktop, It is recommended that you move this somewhere in your user's home Folder. (ie /Users/YOURUSERNAME/Applications/)*

Once installed, just open up the app and you should be prompted for your mindfire username and password, enter it and you should be good to go.

## Not working?

If you only see a white screen then there is likely a permissions issue with Silverlight.

**To fix it, go to:**

Library > Application Support > Microsite

If there is no folder called **Silverlight** then it is not installed so run `brew cask install silverlight` 

If there is a folder called **Silverlight**, right click on it and select **Get Info**, go down to permissions and assign everyone and staff to have "read & write" permissions. Then try to reopen Marketing Studio.