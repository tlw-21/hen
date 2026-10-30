# hen
My Books and Notes


Extracting M4A to MP3 into a usb

%HOMEPATH%\hen\dev_setup\windows

Using windows
```
for %n in (*.m4a) do (ffmpeg -i "%n" -codec:v copy -codec:a libmp3lame -q:a 2 "D:\%n.mp3")
```

using Bash (has issues with some names)
```bash
for f in *.m4a; do ffmpeg -i "$f" -codec:v copy -codec:a libmp3lame -q:a 2 /D/"${f%.m4a}.mp3"; done
```
