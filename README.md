# docker-mediaelch

Container for MediaElch (http://www.kvibes.de/mediaelch/)

Run MediaElch with HTTP GUI (port 5800) or RDM (port 5900).

Exported Volumes

Builds and pushes two docker images for Ubuntu 20.04/latest and Ubuntu 18.04

## Usage
Containerised MediaElch and allow remote accesss through HTTP GUI. Connect to `http://<docker_ip>:5800` to access mediaelch GUI

## Parameters
* `-p 5800:5800 -p 5900:5900` - the port(s)
* `-v /home/mediaelch/.config/kvibes` - where MediaElch should store config files.
* `-v /media/movies` - your movies folder
* `-v /media/tv` - your tv-shows folder
* `-e PGID` for GroupID - see below for explanation
* `-e PUID` for UserID - see below for explanation

### User / Group Identifiers
You can specify the user `PUID` and group `PGID`. Ensure the data volume directory on the host is owned by the same user to avoid permission issues.
