# Pick and Park Machine Learning 


## Features
> This application functions by detecting a parking spot
> and calculating it's size. It then detects a vehicle 
> and determines the type and length of the vehicle.

## Running the Algorithm
Uses scripts object_size.py and object_size_mine.py
To run the application, execute the following commands.

Object Command:
- python object_size.py --image images/example_01.png --width 0.955

Car Command:
- python object_size.py --image images/example_01.png --width 500

Steps involved:
Find contours in the image.
Get the minimum area rectangle for the contours.
Draw the mid points and the lines joining mid points of the bounding rectangle of the contours.
Grab the reference object from the contours and calculate Pixel Per Metric ratio.
Calculate and print the bounding rectangle's dimensions based on the reference object's dimensions.
Assumptions:
There is a reference object in the image which is easy to find and it's width/height is know to us.
Uses "Pixel Per Metric" ratio to calculate the size based on the given reference object.
Reference object properties:
We should know the dimensions of this object (in terms of width or height).
We should be able to easily find this reference object in the image, either based on the placement of the object (like being placed in top-left corner, etc.) or via appearances (like distinctive color and/or shape).
Used the United States quarter as the reference object.
Used the OpenCV's find contours method to find the objects in the image and calculated their dimensions.

Second Algorithm:
Uses frozen_inference_graph.pb, main.py, and coco.names
Command:
Run main.py which will use webcam to identify objects shown
