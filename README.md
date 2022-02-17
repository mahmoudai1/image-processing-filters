# Digital Image Processing Filters

• Digital Image Processing filters developed by python using ipywidgets.


# I. Filters Used:
**1. Impulse Noise (Salt and Pepper):**
• A random number is used to plot the black/white pixel on the image, with respect 4/8-neighbor, to fill the image with noise.


**2. Gaussian Noise:**
• Normal Distribution is applied to the image with respect the mean and the std deviation properties to fill the image with noise.


**3. Unsharp Masking and High-boost Filtering:**
• Blurring is first applied to the image with a specified kernel size, and then, create a mask by subtracting the real image with the blurred filter, then, add the real image to a variable K and multiply by the mask to sharpen the image. Where K >= 1, and for K > 1 is for High-boosting.


**4. Fourier Transform:**
• A Fourier Transform is applied by looping through the row and columns of an image to apply the summation, and loop through each pixel of an image to get each x and y. By multiplying the existed pixel with the exponential of *[(−𝑗 × 2𝜋)(𝑥𝜇/𝑀 + 𝑣𝑦/𝑁)] (where 𝜇 and 𝑣 ≥ 0)* and then adding the output to an empty created matrix of the same size as the real image we get the output image.


**5. Median Filter:**
• First, read an image and then translate it into Binary and obtain the number of rows and columns of the image (M, N). Traverse the image. For every 3 x3 area, then find the median of the pixels (by sorting the matrix and get the median) and replace the current pixel by the median. The purpose is to reduce noises like salt and pepper noise.


**6. Gaussian Filter:**
• Gaussian filtering is used to blur images and remove noise, in one dimension.


**7. Averaging Filter:**
• Apply the smoothing 3x3 average filter (1/16) * matrix[1,2,1;2,4,2;1,2,1].

• Multiply the image with the filter to produce a new image after noise cancelation.


**8. Interpolation (Bicubic):**
• Apply the interpolation kernel function with the mathmatical formulas.

• Apply pad function to pad the first and last two columns and rows of the image where the 16 (4x4) nearby pixels is used.

• Take the image, scaler ratio and cofficient as parameters to bicubic_interpolation function.

• Multiply 1/ratio with every row and column +2 to get the nearby pixels values of the coordinaties.

• Floor these values for computing.

• Making 3 matrices for (kernel of x values, kernel of y values and the nearby pixels).

• Dot product the 3 matrices inside a matrix of zeros(matrixImage).

• Return this matrix (matriximage) to produce the image after the bicubic interpolation filter.


**9. Interpolation (Bicubic):**
• Sobel filter consists of vertical and horizontal operators as known as Gx and Gy.

• We apply these filters to the gray scaled image by multiplying Gx with the gray scaled image and get sum1 and sum2 by multiplying Gy with the gray scaled image and then we take the sum of both and use this equation *sqrt(pow([𝐺𝑥(𝐴)], 2) + pow([𝐺𝑦(𝐴)], 2))*. This is implemented in the algorithm by looping through the gray scaled image and get sum1 and sum2, and then update the image pixels with the equation *sqrt(pow([𝐺𝑥(𝐴)], 2) + pow([𝐺𝑦(𝐴)], 2))*.


**10. Interpolation (Bicubic):**
• First, it calculates normalized histogram for the image, then, the cumulative distribution function is calculated by taking the sum of the normalized values of the image, and the transfer functions is then calculated by multiplying the values of the normalized by the cumulative distribution, then the last thing is to apply the transfered values for each pixel of the image.



# II. Tools and Frameworks:
• Jupyter-Lab
• Python3.8
• ipywidgets
• NumPy
• OpenCV
• Matplotlib

# Contact:
• mahmoud.ahmed48@msa.edu.eg

<br/>

#### Made with :heart: in Egypt
