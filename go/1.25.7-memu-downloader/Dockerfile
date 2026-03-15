FROM g.nas.loc/okoteka/internal-images/go/1.25.7:latest

RUN wget -q https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp \
    -O /usr/local/bin/yt-dlp \
 && chmod +x /usr/local/bin/yt-dlp

RUN apk add --no-cache ffmpeg
