# Overview

# Prerequisite

* Docker
* Docker compose
* [bbb_sunflower_1080p_60fps_normal.mp4](http://bbb3d.renderfarming.net/download.html)


# How to use it

before start the server, download the above video file and copy to `./assets/videos` directory

## Start server

```
docker-compose up -d
```

## Stop server

```
docker-compose down
```

## Play video (Pseudo streaming)

1. Open web browser like chrome, firefox.

2. Type `http://localhost:8080/video/<your_video_file>`

3. The video will shows in web browser.

## Play live stream (HLS)

1. Open VLC or Pot player

2. Open with `http://localhost:8080/hls/hello.m3u8`

3. The live stream will shows.

## Play live stream (DASH)

1. Open VLC or Pot player

2. Open with `http://localhost:8080/dash/hello.mpd`

3. The live stream will shows.


## Streaming your custom live stream

### OBS

1. Launch the OBS

2. Setup the live streaming configuration

* server address: `rtmp:localhost:1993`
* key: `<stream_key>`

3. Start streaming

### Player

1. Open VLC or Pot player

2. Open with `http://localhost:8080/dash/<stream_key>.mpd`
