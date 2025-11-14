**Team Members:**

Avneesh Nolkha   
Ayushee Mittal     
Smita Sasindran    
Vishesh Sethi    

--------------
**File 1:**

**Targets:** 
Accuracy: 99.4, Target Params: 10k   
Base model with less than 10K params  

**Results:**
 - Best Train acc: 99.11
 - Best Test Acc: 98.64
 - Total Params: 9580

**Analysis:** 
Total Params = 9580. Our target is to reduce this to less than 8K params. In next file we're aiming for even a lighter model and we will use global average pooling to further reduce the number of params. Then we can focus on achieving desired accuracy as we're already very near to 99.4 %. We've reached 98.6 without adding any #FantasticBeasts.

**File Link:**
https://github.com/avneesh-nolkha/EVA5/blob/master/Session5/EVA5A5F1.ipynb

-----------------
**File 2:**

**Targets:** 
Target Accuracy: 99.4, Target Params: < 8k   
Our aim here is to reduce the number of params and we will use a GAP layer to reduce the number of params and some more minor changes to the model just to reduce the number of params.

**Results:**
 - Best Train acc: 98.40
 - Best Test Acc: 98.50
 - Total Params: 7710

**Analysis:**
So we can see we have overfitting here in some epochs. We will add BatchNorm and dropout to reduce overfitting and increase accuracy.

**File Link:**
https://github.com/avneesh-nolkha/EVA5/blob/master/Session5/EVA5A5F2.ipynb


------
**File 3:**

**Targets:**
Target Accuracy: 99.4   
In the last file we realised we had overfitting and so we will add BatchNorm and dropout to reduce overfitting.

**Results:**
 - Best Train acc: 99.17
 - Best Test Acc: 99.21
 - Total Params: 7910 

**Analysis:**
We tried adding droput and Batchnormalization in this file. While Normalization gave good results and reduced overfitting. Dropout made things bad. It reduced overfitting but it reduced the Accuracy. So we decided to drop dropout out of the code and we're getting good results. Now we just need to tweak LR and momentum to reach the desired Results.

**File Link:**
https://github.com/avneesh-nolkha/EVA5/blob/master/Session5/EVA5A5F3.ipynb

------
**File 4:**

**Targets:**
Target Accuracy: 99.4   
In this file we need to tweak the LR rate and momentum.

**Results:**
 - Best Train acc: 99.49
 - Best Test Acc: 99.43
 - Total Params: 7910

**Analysis:**
In this file we need to tweak the LR rate and momentum.

Learning rate: The learning rate controls how quickly the model is adapted to the problem. Smaller learning rates require more training epochs given the smaller changes made to the weights each update, whereas larger learning rates result in rapid changes and require fewer training epochs.

A learning rate that is too large can cause the model to converge too quickly to a suboptimal solution, whereas a learning rate that is too small can cause the process to get stuck.

Momentum: Momentum pushes your output towards global optimum. Too big or too small will ruin everything. In other words, momentum changes the path you take to the optimum. It helps overcome local optimum (If you get stuck).

For example: If you have an objective function, you have to decide how to move around on it. Steepest descent on the gradient is the simplest approach, but fluctuations could be a big problem. Adding momentum helps solve that problem.

NOTE: High momentum should always be accompanied by low learning rate, else you will overshoot the global optimum.

**File Link:**
https://github.com/avneesh-nolkha/EVA5/blob/master/Session5/EVA5A5F4.ipynb
https://github.com/avneesh-nolkha/EVA5/blob/master/Session5/EVA5A5F4(a).ipynb
