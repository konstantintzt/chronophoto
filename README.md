# Chronophoto

With this program, you'll be able to generate a picture using the [chronophotography](https://en.wikipedia.org/wiki/Chronophotography) technique. You can choose whether you prefer to use a sequence of images, or a video. In both cases, the camera should be completely still while you record. Keep in mind that this program has only been tested on Windows yet.  

Example of a chronophotograph from Wikipedia:  

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Chronophotography_sport_360_Cross-_%28Almost%29.jpg/1200px-Chronophotography_sport_360_Cross-_%28Almost%29.jpg" style="max-width:50%">

## Usage

You need the [opencv-python](https://pypi.org/project/opencv-python/) library to run this program. You can install it by running `pip install opencv-python` in your terminal.  
To run the program, run `py chronophoto.py` in your terminal, with the necessary arguments.

### Arguments

**For all input**
 - `--inputpath` (required) : The path to the video or to the folder containing the image sequence.
 - `--show` (optional) : If you add this flag the final image will be shown in an opencv window.

**For video input**
 - `--time` (optional) : The amount of time (in seconds) between two frames you want to use.
 - `--framerate` (required if you use `--time`) : The framerate of the video in frames per second (FPS). Default is 30.

**For an image folder input**
 - `--filetype` (required) : Extension of the image filetype. Default is PNG.
 - `--nameformat` (required) : Base of the name of the image files. Default is "frame_". (i.e. The first image's name should be \<nameformat>0.\<filetype>)

## Output

Once you run the program, an image file called "output_img.\<filetype>" will be created in the directory of the input file(s).