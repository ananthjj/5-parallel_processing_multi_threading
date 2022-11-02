Grade: 93/100

-3: Did not modify the declaration of existing compute_image function correctly. It should return a void * and take a single struct pointer typecast as void * as argument.

-4: Did not explain the nature of the two curves. Increasing the number of threads should reduce the time taken to run. However, this is limited by the number of cores assigned to the VM and the number of threads per core. So, there should be an initial speedup and then the curves should plateau. The point where the curve plateaus depends on individual VM configs.

-4: Updated by Daniel Balasubramanian on 11/2/22:

This statement in your report is unclear:

"The difference in shape is likely due to how in A, since there are less things to do, some of the initial threads finish before the program even creates the remaining threads."

A better wording is:

"The difference in shape is likely due to how in A, because the work is not divided evenly between threads, some threads finish earlier than others, and the overall running time is bottlenecked by the running time of the threads where the majority of the work is assigned."

