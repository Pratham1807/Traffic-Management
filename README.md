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
    If pixel value is greater than a threshold value, it is assigned one value (may be white), else it is assigned another value (may be  black). The function used is cv2.threshold. First argument is the source image, which should be a grayscale image. Second argument is the threshold value which is used to classify the pixel values. Third argument is the maxVal which represents the value to be given if pixel value is more than (sometimes less than) the threshold value. OpenCV provides different styles of thresholding and it is decided by the fourth parameter of the function. Different types are:<br>
  * cv2.THRESH_BINARY<br>
  * cv2.THRESH_BINARY_INV<br>
  * cv2.THRESH_TRUNC<br>
  * cv2.THRESH_TOZERO<br>
  * cv2.THRESH_TOZERO_INV<br>

  **2. Erosion :-**
   The basic idea of erosion is just like soil erosion only, it erodes away the boundaries of foreground object. A kernel slides through      the image (as in 2D convolution). A pixel in the original image (either 1 or 0) will be considered 1 only if all the pixels under the      kernel is 1, otherwise it is eroded (made to zero).
   
  **3. Dilation :-**
    It is just opposite of erosion. Here, a pixel element is '1' if atleast one pixel under the kernel is '1'. So it increases the white       region in the image or size of foreground object increases. Normally, in cases like noise removal, erosion is followed by dilation.         Because, erosion removes white noises, but it also shrinks our object. So we dilate it. Since noise is gone, they won't come back, but     our object area increases.
    
  **4. Opening and Closing :-**<br>
  * Opening :- Opening is just another name of erosion followed by dilation. It is useful in removing noise, as we explained above.<br>
  * Closing :- Closing is reverse of Opening, Dilation followed by Erosion. It is useful in closing small holes inside the                              foreground objects, or small black points on the object.
