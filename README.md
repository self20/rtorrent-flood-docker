## romancin/rtorrent-flood

![](https://camo.githubusercontent.com/d8f5cb502f06e0ea1cc171550c2bed035293c1a9/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6a6f686e667572726f772e636f6d2f73686172652f666c6f6f642d73637265656e73686f742d612d303630362e706e67)

#### Main features
- Based on Alpine Linux.
- rTorrent and libtorrent are compiled from source.
- Provides by default a solid configuration.
- [Filebot](http://www.filebot.net/) is included, and creates symlinks in `/downloads/Media`.
- [Flood](https://github.com/jfurrow/flood), a modern web UI for rTorrent with a Node.js backend and React frontend.

#### Build-time variables
- **RTORRENT_VER** : rtorrent version
- **LIBTORRENT_VER** : libtorrent version
- **MEDIAINFO_VER** : libmediainfo version
- **FILEBOT_VER** : filebot version
- **BUILD_CORES** : number of cores used during build

#### Environment variables
- **UID** : user id (default : 0)
- **GID** : group id (defaut : 0)
- **FLOOD_SECRET** : flood secret key (defaut : supersecretkey) (CHANGE IT)
- **CONTEXT_PATH** : context path (base_URI) (default : /)
- **RTORRENT_SCGI** : SCGI port (default : 0 for use local socket)
- **PKG_CONFIG_PATH** : `/usr/local/lib/pkgconfig` (don't touch)

#### Ports
- **51415** (bind it).
- **3000** [(reverse proxy!)](https://github.com/hardware/mailserver/wiki/Reverse-proxy-configuration)

#### Tags
- **latest** : latest versions of rTorrent/libtorrent.
- Use **$RTORRENT_VER-$LIBTORRENT_VER** to get specific versions of rTorrent/libtorrent.

#### Volumes
- **/downloads** : your downloaded torrents, session files, symlinks...
- **/config/flood-db** : Flood databases.
