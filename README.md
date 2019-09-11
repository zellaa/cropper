# What it does
Cropper is a simple shell script (tested to work on both bash and zsh) which finds all video files within the current directory, and presents them to you in an ncurses TUI to then select, along with timestamps for you to input. It then creates a video file of the selected range, leaving the contents of the original file intact.

## Notes:
* Cropper renames all files within the current directory which have spaces in them, such as `file name.mkv` to replace the spaces with underlines, as `file_name.mkv`

## Customising:
As this is a shell script, simply add video/audio extensions which you want cropper to pick up within the code. I.e. instead of having `|opus\|mp4\|m4a\` `|opus\|mp4\|mov\|m4a\`

The ffmpeg options are also customisable as you see fit, in particular for the 'accurate' option you may wish to change the `-preset veryslow` to some other value. See [here](https://trac.ffmpeg.org/wiki/Encode/H.264) for more details.
