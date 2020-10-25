`ffmpeg -y -f x11grab -s 1280x800 -i :0.0 -f alsa -i default out.mkv`

`ffmpeg -y -i /dev/video0 out.mkv`
