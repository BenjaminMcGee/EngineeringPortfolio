This folder contains only electrical engineering, video 
processing projects.

The video AI+OpenCVFaceFinder is a demonstration of
a project I made using OpenCV, Python, an imported 
neural network, and an Nvidia Jetson Nano. The objective
was to make something that could pick out a face and eyes
in a live camera feed, overlay a cross of lines on the
center of the face, box the face, and mark various facial 
features. The video processiong was handled by importing 
each frame to the program and having the pre-trained neural 
network find what it was looking for. The neural network 
would return the coordinates of the features it found in 
arrays, which OpenCV would then interpret and mark 
appropriately on the frame then display the frame.

The video OpenCVColorTrackerEgg is a demonstration of an
OpenCV and Python project I made that tracks a specific
color in a live video. The program does this by finding 
all of the pixels in a frame that contain the color that 
is within a tolerance range of the color it is looking for.
Once it has found all of these pixels, it creates a binary 
mask, replacing the correct color with white, and every 
other color with black. The program then uses an OpenCV 
perimiter tracing algorithm to find the perimiter of each 
cluster of these correctly colored pixels. After having 
found each perimiter, the program takes the area of each 
cluster to determine whether it is worth noticing, or just 
noise. After filtering out the noise, the program selects
the largest cluster of valid pixels, draws a box around it
by using the maximum and minimum array positions of the 
cluster, and then uses those values to draw a cross over 
the center. The program then displays the origional frame, as
well as all intermediate processing frames.
