# deep_fake_detector - Trains a SVM model to classify original vs deep fakes

based on the DeepfakeTIMIT repository:

Trained 3 kernels: Linear, RBF and Sigmoid

The Linear and RBF kernel have 100% prediction accuracy at all intervals.  So they are perfectly separable.  The Sigmoid kernel
has an accuracy of 85% at .5 threshold in terms of average classification score across frames.

Data processing involved reading all files, applying viola-jones algorithm to detect faces, creating features composed of SSIM, PSNR, MSE and grayscaled histogram with 256 color bins.

Didn't do much optimization on processinig.  The viola-jones can take an hour or more to do.  Left it on while watching Great British Baking show :D.

