## Description
To trim a video.

## Commands

### Cut using a specific time
```bat
ffmpeg -i input.mp4 -ss 00:10:00 -to 01:10:00 -c:v copy -c:a copy output.mp4
```

## Source: 
https://shotstack.io/learn/use-ffmpeg-to-trim-video/

## Tags
- ffmpeg
- trim-video
