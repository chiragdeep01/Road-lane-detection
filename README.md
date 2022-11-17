# Road-lane-detection
In this project i have used OpenCV to detect road lanes for self driving cars. By detecting road lanes we can help self driving cars in good lane keeping and turning on a curved road.
## Preprocessing image
- First i have performed GaussianBlur on the image.
- Then the image is converted to hsv format.
- Then i have created a mask to detect the yellow road lanes.
- Then i have used CannyEdge detector which helps Hough transform.




![1](https://user-images.githubusercontent.com/85057931/170327066-0c79ff57-bec1-4b20-82a9-ec3d040ac650.png)

## Cropping image
I cropped the image where the lanes are to be detected to avoid false detections. Without this cropping i got some detections on buildings, etc.


So i defined a region of interest where lane detections have to be made and then used bitwise AND to crop the image.


![2](https://user-images.githubusercontent.com/85057931/170327709-434eb794-0a12-4377-8370-6d77140d687c.png)

## Lane detection
I used Probabilistic Hough Transform to detect lines in the Preprocessed image and then drew these lines over on the image.

![3](https://user-images.githubusercontent.com/85057931/170327566-c811baef-b827-4120-8fb7-312545f41582.png)

## Conclusion
This method worked on video and can be used in real time and doesn't require much expensive hardware.

### Limitations
This is a naive approach to road lane detection problem in self driving cars and has its limitations

- Algorithm has trouble finding road lanes when there are shadows over them.
- Sunlight also affects the algorithm in detecting the road lanes.

These problems can be solved using a deep learning based approach. I have tried to build a simple approach to a problem without using deep learning so that no expensive hardware is required.
