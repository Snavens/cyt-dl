# introduction

cyt-dl is an all-in-one tool to download/play youtube video/audio files.

works on cygwin-like terminals and/or GNUlinux

## SET UP by downloading ffmpeg, yt-dlp & mpv

IF YOU ARE USING WINDOWS

 1. ffmpeg

     link: <https://www.gyan.dev/ffmpeg/builds/ffmpeg-git-essentials.7z>

->extract [1] using 7zip. Get it here: <https://www.7-zip.org>

->copy extracted folder to C:\

 2. yt-dlp

     link: <https://github.com/yt-dlp/yt-dlp/releases>

-> copy [2] to [1] C:\ffmpeg\bin folder.

-> edit the system environment variables in environment variables, add C:\ffmpeg\bin folder to path.

If you have python installed then install with pip install yt-dlp and skip downloading [2]

 3. mpv

     link: <https://www.microsoft.com/store/productId/9P3JFR0CLLL6>
     
 IF YOU ARE USING LINUX
 
  1. ffmpeg (download the normal way you install other packages dependind on your distribution eg apt-get install ffmpeg ie debian/kali)
  
  2. yt-dlp (same thing as in [1] / pip install yt-dlp)
  
  3. mpv (same thing as in [1])
  
  FOR ANDROID USE:
  
  1. Download termux 
  
       link: <https://f-droid.org/repo/com.termux_118.apk>
       
Execute the commands (on your installed termux):

    apt-get update ; apt-get upgrade \
    apt install mpv ffmpeg python python-pip \
    pip install yt-dlp
    
  

## how to use

LINUX/CYGWIN

clone with:

    git clone https://github.com/Snavens/cyt-dl.git
    
    mv -vf cyt/<folder>/cyt-dl /usr/local/bin
    
    chmod 777 /usr/local/bin/cyt-dl
    
ANDROID

    git clone https://github.com/Snavens/cyt-dl.git && mkdir ~/bin && cp -vrf cyt/Android/termux-url-opener ~/bin
    
    termux-setup-storage && chmod 755 ~/bin/termux-url-opener
    
go to app settings and give termux permission to appear on top and you are done now all you have to do is share videos directly to termux app 

FOR WINDOWS USERS AGAIN

Make sure the folder is in path
If everything is set up, now you may start using it.

General usage examples:

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
