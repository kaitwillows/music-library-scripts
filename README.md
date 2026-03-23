> [!WARNING]
> this repository is in development. do not use it, and do not trust me.

> [!NOTE]
> i have and will not use ai for any part of this repository

## motivation
- i love music, i don't like streaming services, and i'm willing to waste time on this
- [beets](https://beets.io/) is cool in concept, but i don't like the way it works (at least by default)


## directory tree
- `root/`
  - `scripts/`
  - `sources/`
    - `bandcamp/` - zips of flac albums, or flac files for singles
    - `soulseek/`
    - `rips/`
      - `vinyl/`
    - `patreon/` - patreon postst that are fine to be shared
    - `xpatreon/` - patreon posts that shouldn't be shared
    - `original/`
  - `libraries/`
    - `flac/` - flac OR highest quality compressed file
    - `mp3v2/`
    - `snowsky/` - for my mp3 player (i basically just need smaller covers)
  - `.cache/` - for unzipped bandcamp albums
 

## importing process
on any changed directories in `sources/`, a script will add each found audio file to the flac library in the following structure:
```
root/flac/[ARTIST ALIAS]/[ALBUM NAME] [(4-digit year)] [[SOURCE]]/
  [2-digit track number] [track name].flac
```
  - `bandcamp/`
    - metadata will **not** be altered from here.
    - file names will be changed though.
  - `soulseek/`

## soulseek downloads
genuinely dont know if this is possible, but i want a script that takes an album string query, and searches for that using slskd prioritizing:
- flac release (try to double check it's not fake)
- tagged `[bandcamp]`
- has ALL songs in the album (double check with bandcamp if possible, if not, musicbrainz)

then:
- strip all tags but title, artist(s), album artist(s), track number, and disk number
- ensure they match preferably something other than musicbrainz because musicbrainz kinda fucks things up sometimes uaghh and idk



