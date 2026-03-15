FROM g.nas.loc:4567/okoteka/internal-images/go/1.25.7:4f7ea6d2

RUN apk add --no-cache python3 py3-pip ffmpeg

RUN pip3 install --no-cache-dir --break-system-packages yt-dlp

CMD ["yt-dlp", "--version"]
