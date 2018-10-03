# blur-videos
Blur a section of your video using manual tracking of frames.

This is script is based on the `manual_tracking` module in [MoviePy](https://zulko.github.io/moviepy/) and requires MoviePy and [PyGame](https://www.pygame.org/news) installed. 

The original module is edited to allow for non-consecutive blurring (i.e. skipping frames in which blurring should not be added to the video). Size and intensity of the blurring are set to defaults and need to be changed inside the code if needed (this is indicated with an in-line comment). The default setting requires the user to manually track each frame of the video. A mouse-click on the pop-up screen stores a blur coordinate for that location; any key stroke on the keyboard (except `Esc` and `\` will move to the next frame _without_ blurring the frame.

In the below example, the Swedish Sign Language sign BJÖRN ('bear') has been tracked to blur out the mouth for frames when the hand is not articulating in front of the mouth (cf. the non-blurred sign below).

### Blurred video (converted to `.gif`):
![bjorn_blurred](https://github.com/borstell/blur-videos/blob/master/bjorn_blurred.gif)

### Original video (converted to `.gif`):
![bjorn](https://github.com/borstell/blur-videos/blob/master/bjorn.gif)

The script runs over any video file (formats `.mp4`, `.mpg`, `.mpeg`, `.wmv`, `.avi`) inside a directory. The manual tracking is stored as a `.txt` file for each tracked video.

The script can be called from the command line with the command:
```
python3 blur-videos.py
```
