# TraficSpeedRadarDetection



![result](https://user-images.githubusercontent.com/87234353/203464198-a318c420-1817-40dd-bc9d-1b310d59b519.jpeg)

The objective of this project is to create a traffic radar using Image Processing in Python by using 
OpenCV and TensorFlow. When it comes to tracking the speed of vehicles on a segment of road, the vital steps of this projects is:
• Vehicle Detection
• Speed estimation
• Capturing vehicle picture


- Vehicle detection
the vechiles is stationary as the speed camera is stationary image subrtaction is implemented to detect moving object

- Speed estimation
![speed estimator](https://user-images.githubusercontent.com/87234353/203464669-0e7d2a37-c119-40fc-9cd8-803b2cab12c0.PNG)

- Capturing Vechicle image
Based on Contour detection, the image of a particular ID is saved to a folder along with the 
speed. Picture is saved as soon as the speed is estimated.


- Method
1. ROI -> region of interest and masking =>  Image subtraction is performed to detect a moving vehicle. (Image Subtraction helps find the difference between two frames). Masking is performed to make the moving vehicles appear white and the rest of the image black
![image](https://user-images.githubusercontent.com/87234353/203464978-3386eaaa-f21d-4b21-9df5-52d4ba99c866.png)

2. Contour Detection and object tracking
Based on the area threshold of number of pixels, the contours are detected. The threshold is used to 
avoid detecting contours of smaller moving objects that are not vehicles. The object is tracked based 
on the distance between two contours between frames. An ID is assigned to each contour.
![image](https://user-images.githubusercontent.com/87234353/203465078-99076903-ef75-461e-a79c-83e8d9b17c17.png)

3. Speed Estimation 
Time difference between the position of a vehicle is calculated and the speed is estimated based on a 
formula. The timer starts when the vehicle crosses the first line, and the timer ends when the vehicle 
crosses the second line. 
![image](https://user-images.githubusercontent.com/87234353/203465130-5ef73c3a-7231-4ebe-a14e-1f28e943cf24.png)

4. Save vehicle data
The picture of the bounding box (the vehicle) is saved into a file along with the speed. Vehicles 
crossing the speed limit is segregated into a separate folder.
![image](https://user-images.githubusercontent.com/87234353/203465185-f0d65603-dfd4-4b9b-9f7c-7671f2d248d0.png)

5. Summary
The vehicle data is saved in a text file. The vehicles that exceeded the speed limit are pointed. A 
summary of number of vehicles and the speed violators are displayed

![image](https://user-images.githubusercontent.com/87234353/203465209-fef3a913-e421-4d4a-a518-0e8e2e87d57f.png)

