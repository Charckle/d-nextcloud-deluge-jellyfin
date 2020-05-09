# Premis

A set of Docker container to host a NAS/cloud and a torrent client.

# Resources

For this project the resources used are nextcloud and deluge, both from the image of linuxserver repository on the Docker webpage.

# Configuration

## Nextcloud

The nexcloud data folder is ment to be a mount for an external drive, preferably in a RAID with mdadm.

For this project we are using SQLite, as it was intended for a household ammount of users.

In Nextcloud we have to add a plugin, External storage support, that allows us to mount a folder, in our case ./nextcloud_data/Torrents, as a folder accessible to all users. We enter the External mounts configuration and set the mount point to "../../../data/Torrents"

## Deluge

The default credentials of Deluge are "admin" and "deluge". Please, give it a strong password.

After that we must select the download location in Deluge. In the Preferences menu we ad the download path to "/downloads"

## Jellyfin

The volume is shared with the torrent location, but you can add multiple sources.
