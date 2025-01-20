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
2. Install the required libraries and extensions for the program, and update the packages.
3. Upload the image to be translated and rotated.
4. Once the data is uploaded successfully, the program displays the image data before and after translation and rotation to compare the results.
5. The rotation and translation operations are implemented using CUDA within the kernel. The CUDA code for the translation and rotation program is stored in `translationimg.cu` and `rotation90.cu`, which are executed using nvcc CUDA.
6. After creating the CUDA program code, it is stored in `translationimg.cu` and `rotation90.cu`.
7. Once the files are saved, the program compiles the code using nvcc and executes it directly on the GPU.
8. After completing the previous steps, the program displays the results of the rotation and translation, calculates the execution time estimation for both programs, and presents the output of the translated and rotated images.

## **Prerequisites**
- NVIDIA GPU with CUDA support
- CUDA Toolkit installed

## **How to Run**
1. Compile kode translasi menggunakan CUDA nvcc
`!nvcc -o translation translationimg.cu `pkg-config --cflags --libs opencv4` -diag-suppress 611`
2. Menjalankan kode CUDA
`!./translation`
3. Compile kode rotasi menggunakan CUDA nvcc
`!nvcc -o rotation rotation90.cu `pkg-config --cflags --libs opencv4` -diag-suppress 611`
4. Menjalankan kode CUDA
`!./rotation`
