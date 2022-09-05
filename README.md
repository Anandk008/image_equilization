# image_equilization
Using Histogaram and this code is made with MPI
( Parallel programming )

# README
Instructions :-
1. Import the python Libraries.
2. Write functions for Histogram Equalisation of image.
3. Then Initialise the MPI function and distribute all the functions to Threads as below :
➢ 0th thread will do the showing it will show the Input Image.
➢ 1st thread will show the Histogram of this image.
➢ 2nd thread will show PDF, CDF, and all calculation.
➢ 3rd thread will show Construct the image and will show the histogram of that
reconstructed image.
Calculations :-
1. Calculate the frequency of each pixel by traversing the whole img, as the image is
8bit grey so it will contain intensity varying from 0-255 and make a array of that.
2. Now, calculate the PDF by dividing frequency of image pixels with total no. of pixels
3. For CDF just sum the numbers which are before the i’th element of PDF array and
append it to CDF array , vut the total sum of this array will be ‘1’
4. Now for Histogram creation multiply values of CDF array with 256 ( max grey value )
And the round that value to its nearest number.
Now we have a array of histogram so now replace the new values of pixels in the image,
Now we have a complete image which is equalised.
Speed Up :-
1. If we are having more cores then we will distribute every simple task to all threads,
processes like - calculating PDF, CDF, Image construction will be distributed to single
single thread .
2. But, we have made our program in python so it will require to load all the
dependencies which are required so for working of each thread a fixed amount will
be required.
