# Image-Processing-Translation-and-Rotation-with-CUDA-Programming
## **Program Name**  
Image Translation and Rotation Program using CUDA Programming.  

## **Program Function**  
This program performs translation and rotation on an image specified in the program code. It rotates the downloaded image by 90° and applies translation or shifting. The program utilizes CUDA to execute the rotation and translation processes, enabling faster execution. By leveraging GPU programming, which can handle multiple processes simultaneously, the image is divided into smaller parts processed by multiple threads concurrently, making it significantly faster compared to using a CPU.  

## **Key Features**
- Rotate an image by 90°.
- Translate (shift) the image.
- Leverages CUDA for faster performance using GPU parallelism.

## **Steps to Perform**
1. Before starting the program, the status of the NVIDIA GPU is checked.
![image](https://github.com/user-attachments/assets/bd0735c1-349a-4c43-b0df-751cbb8a7a4b)
2. Install the required libraries and extensions for the program, and update the packages.
![image](https://github.com/user-attachments/assets/b49f3400-eda7-4fe0-ae33-03b13b44e959)
![image](https://github.com/user-attachments/assets/c119d30e-cd4e-493e-9f39-881541e3f7c9)
3. Upload the image to be translated and rotated.
![image](https://github.com/user-attachments/assets/f98540b4-d461-4a32-9ff5-81c51ef19118)
4. Once the data is uploaded successfully, the program displays the image data before and after translation and rotation to compare the results.
![image](https://github.com/user-attachments/assets/2c3d39e4-519f-4e44-a7a9-896f79848414)
5. The rotation and translation operations are implemented using CUDA within the kernel. The CUDA code for the translation and rotation program is stored in `translationimg.cu` and `rotation90.cu`, which are executed using nvcc CUDA.
![image](https://github.com/user-attachments/assets/b5134875-2a5b-4736-85bf-8891fe2df4f7)
6. After creating the CUDA program code, it is stored in `translationimg.cu` and `rotation90.cu`.
![image](https://github.com/user-attachments/assets/279a0b85-8426-491b-9512-fb23bd4bc1d7)
7. Once the files are saved, the program compiles the code using nvcc and executes it directly on the GPU.
![image](https://github.com/user-attachments/assets/d79b4482-aa7a-478f-9c1e-81d88f766cb0)
8. After completing the previous steps, the program displays the results of the rotation and translation, calculates the execution time estimation for both programs, and presents the output of the translated and rotated images.
![image](https://github.com/user-attachments/assets/a010b28c-8a9e-443d-9239-73fe926da2ad)

## **Prerequisites**
- NVIDIA GPU with CUDA support
- CUDA Toolkit installed

## **How to Run**
1. Compile kode translasi menggunakan CUDA nvcc
``!nvcc -o translation translationimg.cu `pkg-config --cflags --libs opencv4` -diag-suppress 611``
2. Menjalankan kode CUDA
`!./translation`
3. Compile kode rotasi menggunakan CUDA nvcc
``!nvcc -o rotation rotation90.cu `pkg-config --cflags --libs opencv4` -diag-suppress 611``
4. Menjalankan kode CUDA
`!./rotation`

## **Output Program**
![image](https://github.com/user-attachments/assets/f0b7df61-3fcd-49c4-af0d-f500f78328db)
![image](https://github.com/user-attachments/assets/218598b1-8259-4e0a-978b-90bae6e5367e)

The first image shows a translated image shifted by a quarter of the image width and a quarter of the image height, resulting in the final image being positioned in the bottom-right corner. This indicates that the values of tx and ty are positive.  
The second image shows an image rotated 90 degrees counterclockwise based on the calculation of x and y coordinates.  
Both images were processed and executed in approximately 1.34 seconds using CUDA.
