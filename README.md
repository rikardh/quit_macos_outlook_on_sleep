Assembled by Rikard Hjelm, 2018

This will make the Outlook application on a MAC quit when the MAC goes to sleep.

The main intelligence here is the "sleep watcher" app from Mr Tyler Hoffman. His nice tool allows something to be executed on Sleep and/or Wake of the Mac. Please see here for more info:
http://tyhoffman.com/blog/2013/09/sleepwatcher-power-event-driven-automation/ 

To install sleep watcher, run the install script. You mau want to check Tylers site above for any updates.
***The installer script WILL REMOVE any existing "sleep watcher" installation.***

Now edit the /etc/rc.sleep file and add:
<path>/quit_outlook.app
My rc.sleep contains the following, plain and simple:
/Users/rhjelm/sleepwatcher/quit_outlook.app

You're done!

If Outlook doesn't quit for some reason, try putting the same in /etc/rc.wake. Maybe that helps. The rc.sleep works for me on MacOS Sierra.


Why?
Well, I have issues with my VPN connection and Outlook. When I wake my MAC and Outlook is running, Outlook tries to go online before the VPN is up. This makes Outlook go into Offline mode which I don't always realize. So, better to have to start Outlook at every wake. At least this works for me!
