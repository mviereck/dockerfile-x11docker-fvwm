# x11docker/fvwm
FVWM desktop on alpine. Petite image size.
 - Run FVWM desktop in docker.
 - Use x11docker to run GUI applications and desktop environments in docker images. 
 - Get [x11docker from github](https://github.com/mviereck/x11docker)

# Command examples: 
 - Single application: `x11docker x11docker/fvwm xterm`
 - Full desktop: `x11docker --desktop x11docker/fvwm`
 - Full desktop with init system openrc: `x11docker --desktop --init=openrc x11docker/fvwm`

# Options:
 - Persistent home folder stored on host with   `--home`
 - Shared host folder with                      `--sharedir DIR`
 - Clipboard sharing with option                `--clipboard`
 - Sound support with option                    `--alsa`

Look at `x11docker --help` for further options.

# Extend base image
To add your desired applications, create your own Dockerfile with this image as a base. Example:
```
FROM x11docker/fvwm
RUN apk-add --no-cache midori
```
 # Screenshot
 FVWM desktop in a Xephyr window running with x11docker:
 
 ![screenshot](https://raw.githubusercontent.com/mviereck/x11docker/screenshots/screenshot-fvwm.png "FVWM desktop running in Xephyr window using x11docker")
 

