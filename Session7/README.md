**Team Members:**

Avneesh Nolkha  
Ayushee Mittal  
Smita Sasindran  
Vishesh Sethi   

-----

**RF and output layer sizes**
```
Layer               | RF  | Output Size   
conv1 (depthwise)   | 3   | 32   
conv2 (1x1)         | 3   | 32   
conv3 (depthwise)   | 5   | 32    
conv4 (1x1)         | 5   | 32   
maxpool1            | 6   | 16   
conv5 (depthwise)   | 10  | 16   
conv6 (1x1)         | 10  | 16   
conv7 (depthwise)   | 14  | 16   
conv8 (1x1)         | 14  | 16   
maxpool2            | 16  | 8   
conv9 (dilated)     | 32  | 6   
maxpool3            | 36  | 3   
conv10 (1x1)        | 36  | 3     
gap                 | 52  | 1   
```

---------


Final Accuracy: 82%   
Number of parameters: 935,052   
Epochs: 50   
