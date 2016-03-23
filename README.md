Bittorrent sync is awesome. End of story. 

I am syncing different directories between my work computer, home computer, raspberry pi, and cell phone. Mostly the pi is the "source" of my files, and external backup in case one of my drives dies. 

One problem I ran into was that for some reason, if I ran btsync at startup of the pi it would "forget" all the directories I had shared. I don't know why. I decided instead to run with a config file containing all the directories I was syncing since that wouldn't change from shutdown to startup and such. However, I couldn't find any good examples online! So once I got mine working I posted it to my github.

I left the fields secret and dir, under shared folders blank. To generate a read-write secret, run ./btsync --generate-secret within the folder that the btsync executable is in. In the dir field, enter the directory you'd like to sync. Keep in mind that btsync cannot merge non-empty directories.

Go check it out for a decent example or starting point to bittorrent sync config files.