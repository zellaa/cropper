# What it does
Cropper is a simple shell script (tested to work on both bash and zsh) which finds all video files within the current directory, and presents them to you in an ncurses TUI to then select, along with timestamps for you to input. It then creates a video file of the selected range, leaving the contents of the original file intact.

## Usage:
Run cropper normally by entering `cropper` within a terminal, or pass any optional flags alongside it. Currently supported flags are:
* `-h` to show help within the terminal
* `-l` to list file extensions which cropper is looking for

Time stamps should be entered in the format HH:MM:SS (e.g 02:00:21 would be a time stamp at 2 hours and 21 seconds). 

## Notes:
* Cropper renames all files within the current directory which have spaces by replacing the spaces with underlines. For example, `file name.mkv` becomes `file_name.mkv`.

## Customising:
As this is a shell script, simply add video/audio extensions which you want cropper to pick up within the code. This is done by appending a quoted file extension in the space seperated list `filetypes_list` within the source file.

The ffmpeg options are also customisable as you see fit, in particular for the 'accurate' option you may wish to change the `-preset veryslow` to some other value. See [here](https://trac.ffmpeg.org/wiki/Encode/H.264) for more details.
