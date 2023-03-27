# introduction

cyt-dl is an all-in-one tool to download/play youtube video/audio files.

works on cygwin-like terminals

## SET UP by downloading ffmpeg, yt-dlp & mpv

 1. ffmpeg

     link: <https://www.gyan.dev/ffmpeg/builds/ffmpeg-git-essentials.7z>

->extract [1] using 7zip. Get it here: <https://www.7-zip.org>

->copy extracted folder to C:\

 2. yt-dlp

     link: <https://github.com/yt-dlp/yt-dlp/releases>

-> copy [2] to [1] C:\ffmpeg\bin folder.

![Screenshot (46)](https://user-images.githubusercontent.com/35012707/227935537-ff14bec2-9fb4-48de-9f28-4875a8585b21.png)

-> edit the system environment variables in environment variables, add C:\ffmpeg\bin folder to path.

If you have python installed then install with pip install yt-dlp and skip downloading [2]

 3. mpv

     link: <https://www.microsoft.com/store/productId/9P3JFR0CLLL6>

## how to use

Download the binary file by using link:

    wget https://github.com/Snavens/cyt-dl/releases/download/cyt-dl_v0.8.0/cyt-dl
    mv -vf cyt-dl /usr/local/bin # or ~/bin
  
Or simply clone with:

    git clone https://github.com/Snavens/cyt-dl.git
    mv -vf cyt/cyt-dl /usr/local/bin # or ~/bin
  
Copy it to your local path and set permissions to 777

     chmod 777 /usr/local/bin/cyt-dl
  
Make sure the folder is in path
If everything is set up, now you may start using it.

Example of how to use:

stream (file)s

    cyt-dl -s https://www.youtube.com/watch?v=SMT9Yzvw9w0 https://www.youtube.com/watch?v=XWynXenqp4c

download file as audio and store it in downloads folder

    cyt-dl d https://www.youtube.com/watch?v=5hX-qHLIRe8

download as video and play then keep it in music folder (you can store in any directory you want)

    cyt-dl ap https://www.youtube.com/watch?v=5hX-qHLIRe8 /cygdrive/c/Users/$(whoami)/Music

does the same as above and loop file.

    cyt-dl dp -l https://www.youtube.com/watch?v=5hX-qHLIRe8 /cygdrive/c/Users/$(whoami)/Music

More help is readily available in the script itself, use --help as option.

enjoy !
