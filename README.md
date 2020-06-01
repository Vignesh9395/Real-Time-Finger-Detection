# Real-Time-Finger-Detection

Detect Fingers and Count in real time.

![Alt text](relative/fpdetgit.JPG?raw=true "Output")

This Project is done utilizing the inbuilt methods in OpenCV and sklearn.

The initial frames from the video are read and accumulated till a threshold is reached for [Background Subtraction](https://docs.opencv.org/3.4/d1/dc5/tutorial_background_subtraction.html).

Once the background in extracted, it's time for the [foreground](https://en.wikipedia.org/wiki/Foreground_detection) ( i.e: our hand) to be detected. This is done by calculating the absolute difference between the foreground and the background that is detected.

Fingers are then detected from the binary image of the foreground by finding the external [contours](https://docs.opencv.org/trunk/d4/d73/tutorial_py_contours_begin.html) (or) finger outlines and calculate the number of fingers using [ConvexHull Algorithm](https://en.wikipedia.org/wiki/Convex_hull_algorithms).

The steps after initial background detection will be repeated for every frame as the camera records.





