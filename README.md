# orangewire

- Searches for and fetches MP3s (via youtue-dl), adding correct ID3 tags and cover art (via discogs's open database).

- Download single tracks or even entire albums, EPs, etc. at relatively high bitrate (200-300kbps) with just one command.


# Installation

via PyPI:

```bash
$ sudo -H pip3 install orangewire
```

# Examples

## Download a track

```bash
$ orangewire --user-token ********** --track-name "music is math" --artist-name "boards of canada"
```

![example of result of track downloading in Windows](https://i.imgur.com/l8cykHy.png)

N.B.: By default, this command produces no output if there are no errors or no further input required from you. To view progress, pass ``--verbose``. Otherwise, it will take up to 2 minutes on an average laptop before it exits (the bottleneck is youtube-dl which drives a lot of network requests and calls to ffmpeg).

## Download a whole album

```bash
$ orangewire --user-token ********** --album-name "damn" --artist-name "kendrick lamar"
```

You could also specify a directory to place the finished audio files with ``--output-directory``:

```bash
$ orangewire --user-token ********** --album-name "damn" --artist-name "kendrick lamar" --output-directory "../Kendrick Lamar - DAMN"
```

# Usage

## Tutorial

### 1. Register an account with discogs.com

### 2. Get a "user token"

https://www.discogs.com/settings/developers

### 3. Install orangewire

## Advanced

### Put your user token in ~/.orangewire to omit the command line flag

``$HOME/.orangewire`` should contain one line with only the user token obtained from discogs.com.

# How does it work?

1. Searches discogs.com's open music database for your query. This requires you to set up a free account and retrieve a "user token" in order for orangewire to work.
2. You manually select which one you meant from a few candidates (e.g., of tracks or albums). (Ideally this could be automated.)
3. Scrapes YouTube's search results to find the matching song (or songs in the case of albums, EPs, etc.).
4. Runs youtube-dl to convert the song(s) to MP3s.
5. Adds ID3 tags for artist, track name, album/cover art, etc. using the metadata from discogs.com.

# TODO

## Add a way to cross reference Wikipedia for more authoritative song information, where possible

## Train some classifier network to find the correct song metadata out of search results

## Implement the reverse operation: Find song metadata from YouTube video

# Legal

orangewire is a thin convenience wrapper around youtube-dl—without youtube-dl—a completely separate project—, this program wouldn't run. In itself, orangewire does not download, transfer, host, or share any media files. It only intends to use content from a site based on user submissions (YouTube) that is considered to be compliant with IP laws. Thus this program isn't subject to DMCA or other IP laws.

The author has no liability for any copyright infringement you commit with this program.

# License

GPL v3
