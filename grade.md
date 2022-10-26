Grade: 93/100

-3: Did not modify the declaration of existing compute_image function correctly. It should return a void * and take a single struct pointer typecast as void * as argument.

-4: Did not explain the nature of the two curves. Increasing the number of threads should reduce the time taken to run. However, this is limited by the number of cores assigned to the VM and the number of threads per core. So, there should be an initial speedup and then the curves should plateau. The point where the curve plateaus depends on individual VM configs.
