# lyrics

**find** music files that **need** lyrics and **get** them as sidecars.

## Deployment

Get the source from this repository.

	git clone https://github.com/rtyle/lyrics.git
	(cd lyrics; git submodule update --init --recursive)

This implementation scrapes lyrics from **genius.com** using their API which requires an access token.
Acquiring such is documented here:

https://docs.genius.com/

Cache your Genius API token in a file (python module) named **geniusapi.py** like this:

	token = "your genius API token goes here"

Install python dependencies

	pip install mutagen

## Usage

**find** music files that **need** lyrics and **get** them as sidecars.

	find . \( -name \*.flac -o -name \*.mp3 \) | need | get

**find** music files that might have **txt** (lyrics) sidecars that **no** longer **match** ...

	find . \( -name \*.flac -o -name \*.mp3 \) | nomatchtxt

... and **rename** them

	find . \( -name \*.flac -o -name \*.mp3 \) | nomatchtxt --rename

## See also

	find
	need -h
	get -h
	nomatchtxt -h
