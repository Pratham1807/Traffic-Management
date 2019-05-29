# Traffic-Management
Counting the number of vehicles passing a given area on a road

#### Plan of Action :- 
  1. Using Background Subtraction to obtain Foreground
  2. Using OpenCV filters (Threshold, Erode, Dilate, Opening, Closing)
  3. 
  4.
  5.
  
  
  ### 1. Backgroung Subtraction
  
  ### 2. Using OpenCV filters : 
   **1. Threshold :-** 
    If pixel value is greater than a threshold value, it is assigned one value (may be white), else it is assigned another value (may be       black). The function used is cv2.threshold. First argument is the source image, which should be a grayscale image. Second argument is       the threshold value which is used to classify the pixel values. Third argument is the maxVal which represents the value to be given if     pixel value is more than (sometimes less than) the threshold value. OpenCV provides different styles of thresholding and it is decided     by the fourth parameter of the function. Different types are:<br>
  * cv2.THRESH_BINARY<br>
  * cv2.THRESH_BINARY_INV<br>
  * cv2.THRESH_TRUNC<br>
  * cv2.THRESH_TOZERO<br>
  * cv2.THRESH_TOZERO_INV<br>
