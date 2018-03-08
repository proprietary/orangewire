# orangewire

Downloads music from YouTube with ID3 tags and cover art provided by discogs.com. You can download single tracks or even entire albums, EPs, etc. at relatively high bitrate (>200kbps) and MP3 compression.

# Examples

## Download a track

```bash
python orangewire --user-token ********** --track-name "music is math" --artist-name "boards of canada"
```

!(example of result of track downloading in Windows)[https://i.imgur.com/l8cykHy.png]

## Download a whole album

```bash
./bin/python3 __main__.py --album-name "damn" --artist-name "kendrick lamar" --output-directory "../Kendrick Lamar - DAMN"
```

!(example of result of downloading an album in Windows)[https://i.imgur.com/kzlrsiA.png]

# Usage

## 1. Register an account with discogs.com

## 2. Get a "user token"

https://www.discogs.com/settings/developers

# License

GPL v3
