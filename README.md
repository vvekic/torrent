## wonderfall/rutorrent
Originally forked from [Wonderfall/rutorrent](https://github.com/Wonderfall/dockerfiles/tree/master/rutorrent).

#### What is this?
This container contains both rtorrent (whis is a BitTorrent client) and rutorrent (which is a front-end for rtorrent). Filebolt is also included, the default behavior is set to create clean symlinks, so media players like Emby/Plex can easily detect your TV shows and movies.

![](https://pix.schrodinger.io/KDVxwnJA/nEMCzJEd.jpg)

#### Main features
- Lightweight, since it's based on Alpine Linux.
- Everything is almost compiled from source.
- Filebot is included, and creates symlinks in `/data/Media`.
- rutorrent : Material theme by phlo set by default.
- rutorrent : nginx + PHP7.

#### configuration

- The default .rtorrent.rc file is in the /home/torrent Volumes

- Default port: **49184** (bind it).
- Default rutorrent port: **80** [(reverse proxy!)](https://github.com/hardware/mailserver/wiki/Reverse-proxy-configuration)

#### Volumes
- **/home/torrent** : the .rtorrent.rc config file.
- **/data** : your files, symlinks, and so on.
- **/var/www/torrent/share/users** : rutorrent settings.