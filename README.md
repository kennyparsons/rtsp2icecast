# rtsp2rsas

A simple Docker container to stream audio from an RTSP stream (eg. from an IP camera) to Rocket Streaming Audio Server using FFmpeg. 

### Environment Variables

Below are the environmental variables available and their default value. Override them as needed. The FFmpeg options are already set to auto-detect the audio stream in realtime and transcode it to MP3 at 128 kbps using LAME. 

| Variables            | Required |
|----------------------|:--------:|
| `RTSP_URL`           | Yes      |
| `ICECAST_URL`        | Yes      |
| `ICECAST_PORT`       | Yes      |
| `ICECAST_USERNAME`   | Yes      |
| `ICECAST_PASSWORD`   | Yes      |
| `ICECAST_MOUNTPOINT` | Yes      |
| `FFMPEG_INPUT_OPTS`  |          |
| `FFMPEG_OUTPUT_OPTS` |          |


### Docker Compose

1. Clone the repo
2. Edit docker-compose.yaml (particularly the required variables)
3. Launch the containers using `docker-compose up -d`
