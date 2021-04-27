# Image-Manipulation
Desktop application made in JAVA to manipulate image and add effects and filters on top of the images.
## How To Run
##### Interactive (GUI):

To run the software with graphical user interface run the following command at the appropriate directory in the CMD.

    java -jar CrossStitch.jar -interactive

##### Script (Batch file):

To run the software with the batch file run the following command at the appropriate directory in the CMD.

```
java -jar CrossStitch.jar -script pat_to_batch_file
```

(Batch file should be .txt file with appropriate commands)



## How to Use the Program
##### Batch file execution

Following are the commands supported in the batch file.
These are the supported commands and their description.

| NO.  | Command                        | Arguments                                                    | Description                                          |
| :--- | ------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------- |
| 1    | load <Pathname>                | Pathname = Path of the image file                            | Loads the image in 3 dimensional int array.          |
| 2    | save <Pathname>                | Pathname = Path at which you want to save the file           | Save the image at the location given.                |
| 3    | blur                           | -                                                            | Blurs the image.                                     |
| 4    | sharp                          | -                                                            | Sharpens the image.                                  |
| 5    | greyscale                      | -                                                            | Converts the coloured image in the Greyscaled image. |
| 6    | sepia                          | -                                                            | Converts the image into sepia toned image.           |
| 7    | dither <density> <withEssence> | density- int representing desired color density per channel. <br /> withEssence - boolean representing the desired image should be reduced with or without essence. | Reduces the colour density of the image.             |
| 8    | pixelate <numberofChunks>      | numberofchunks - int representing desired pixels across the width of the image. | pixelates the image.                                 |
| 9    | mosaic <numberofchunks>        | numberofchunks - int representing the total number of chunks in the desired image. | Converts the image into mosaic image.                |
| 10   | pattern <numberofchunks>       | numberofchunks - int representing desired pixels across the width of the image. | Generates cross stitch pattern from the images.      |
| 11   | quit/q                         | -                                                            | Quits the execution                                  |

- If you want to apply multiple operations on the same image. Just give commands one after another. For example

  ```
  load image.jpg
  blur
  sharp
  dither 2 true
  save image-manipulated.jpg
  ```

  this will apply blur on the image.jpg and after that it will apply sharpening on the blurred image and so on.

- if you want to have different images after all the operations just load the same image and save the image after applying any operations. For example

  ```
  load image.jpg
  blur
  save image-blur.jpg
  load image.jpg
  sharp
  save image-sharp.jpg
  ```


- The path for the images in the batch file can be given absolute or relative.



##### GUI:

![alt text](https://github.com/artikbharoliya/Image-Manipulation/blob/main/reference%20images/image%201.png)

To load and save images go to File menu and choose the appropriate function. 


![image 3](https://github.com/artikbharoliya/Image-Manipulation/blob/main/reference%20images/image%203.png)
The effect menu contains 

- Blur

- Sharp

- Greyscale

- Sepia

- Dither

- Dither with essence

- Pixelate

- Mosaic

  Shortcut (Hot keys) are indicated in the menu for the functions.
  
  
![image 4](https://github.com/artikbharoliya/Image-Manipulation/blob/main/reference%20images/image%204.png)



The cross-stitch menu contains the option to generate cross stitch pattern from the image.



![image 5](https://github.com/artikbharoliya/Image-Manipulation/blob/main/reference%20images/image%205.png)



To create Batch file click on the "Create Batch File" button. Enter your commands and click execute button to run the commands.

##### Saving of file:

To save the file press ctrl+s to save the image.

Enter the name of the image to be saved.

![image 6](E:\Northeastern\PDP\project5\ss\image 6.png)

To save the cross-stitch pattern just add extension of file name as .txt after generating the cross stitch image.

If you want to save image as image file you can skip adding extension. Image will be saved as jpg image. However if you want to save file as .png or .bmp add the extension after the file name.

