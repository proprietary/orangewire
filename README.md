# orangewire

Downloads music from YouTube with ID3 tags and cover art provided by discogs.com. You can download single tracks or even entire albums, EPs, etc. at relatively high bitrate (>200kbps) and MP3 compression.

# Examples

## Download a track

```bash
$ python3 orangewire --user-token ********** --track-name "music is math" --artist-name "boards of canada"
```

![example of result of track downloading in Windows](https://i.imgur.com/l8cykHy.png)

## Download a whole album

```bash
$ python3 orangewire --album-name "damn" --artist-name "kendrick lamar" --output-directory "../Kendrick Lamar - DAMN"
```

![example of result of downloading an album in Windows](https://i.imgur.com/kzlrsiA.png)

# Usage

## 1. Register an account with discogs.com

## 2. Get a "user token"

https://www.discogs.com/settings/developers

## 3. Install dependencies

## 4. Install orangewire

```bash
$ git clone https://github.com/zebradeltasavage/orangewire
$ cd orangewire
$ pip3 install -r requirements.txt
```

# License

GPL v3
