Your report should be checked in to this folder.

The purpose of this experiment and the experimental setup is to show how multithreading reduces the time taken in seconds by parallelizing an expensive computation. To do so, we tested two images from the Mandelbrot and tested with varying threads from 1, 2, 3, 4, 5, 10, 50, 100. Intuitively, as the number of threads increases, functional multithreading should allow for parallelization to reduce the time taken in seconds.

I ran the experiment on a macOS Catalina Version 10.15.6 2.8 GHz Intel i7

Command line:

A: time ./mandel -x -.5 -y .5 -s 1 -m 2000 -n [insert number of threads]

B: time ./mandel -x 0.2869325 -y 0.0142905 -s .000001 -W 1024 -H 1024 -m 1000 -n [insert number of threads]

Explain the shape of the two curves. What is the optimal number of threads? Why do curves A and B have a different shape? (Hint: modify your program to print a message when each thread starts and stops)

Both curves show the time taken in seconds decreasing as more threads are added. It appears as though 10 is the optimal number of threads. After 10, B has a sharper decrease and then flattens out while A has a period of steady decrease after the initial sharp decrease. The difference in shape is likely due to how in A, since there are less things to do, some of the initial threads finish before the program even creates the remaining threads. As B has more data to process each thread takes time to finish filling its part of the image.

