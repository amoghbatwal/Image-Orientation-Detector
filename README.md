# CSCI-B 551 Elements of Artficial Intelligence
## Image-Orientation-Detector

### Problem Statement

These days, all modern digital cameras include a sensor that detects which way the camera is being held when a photo is taken. This metadata is then included in the image ﬁle, so that image organization programs know the correct orientation — i.e., which way is “up” in the image. But for photos scanned in from ﬁlm or from older digital cameras, rotating images to be in the correct orientation must typically be done by hand. The task in this assignment is to create a classiﬁer that decides the correct orientation of a given image.

### Implementation

After running the model for several runs, we see that the highest accuracy is achieved when k is taken to be 11.
I would suggest the client to go with an odd K values (reason being to avoid clash of dominant angle) for their dataset. KNN algorithm is pretty fast and efficient as seen from the above running time and its accuracy. 
We observe that as the training size increases, the time required for KNN model to predict increase which is pretty obvious. But there is always a trade-off. Here, with increase in running time, we are also getting some improvement in the accuracy.

To tacle problems mentioned above, I looked up on how to numerically tweak the values to keep them mathematically same. This helped the output of these functions to not reach NaN or infinity!
Training the neuralnet also was a little challenging task as it was difficult to decide the right size of parameters/complexity of the network so that it doesnt overfit the data. To tackle this, we followed the crossvalidation technique and selected the model which gave least accuracy on validation set.
