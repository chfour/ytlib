# ytlib

this is a collection of bash scripts to manage a local, offline library of
youtube videos. features include:

* automated downloading of videos from a list
* a search engine (using fzf)
* automatically saving channel info ('about' tab, avatar, banner)
* utilities to manage your database, get information about videos
* other utilities (export, getall \[videos, channels\], get random video)

## how to use

### dependencies

first of all, install the dependencies:

* [youtube-dl](https://github.com/ytdl-org/youtube-dl) (required, duh)
* [jq](https://stedolan.github.io/jq/) (required)
* curl & wget (required, both used by the channel info downloader)
* [fzf](https://github.com/junegunn/fzf) (recommended, used by `utils/search`)
* mpv (recommended, used by `utils/search`, could also set the `PLAYER` environment variable before running search)
* 7z (optional, used by `utils/export`)

### usage

then, just run `./dl` + any parameters you'd like, see [youtube-dl/README.md#options](https://github.com/ytdl-org/youtube-dl/blob/master/README.md#options) for more info.

the recommended way to use this thing is to create a `list.txt` file in the root of this repo (already added to the .gitignore) and then use `./dl -l list.txt` (see [here](https://gist.github.com/chfour/46019d153b693ab84b1a76af817b8a40) for an example - my own `list.txt`)

## TODO

* global config file
