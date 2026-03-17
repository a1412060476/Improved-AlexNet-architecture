## Pseudocode of the Proposed Method

**Algorithm 1. Pseudocode of the proposed method**

Input: Training set D = {(xi, yi)}i=1N  
Output: Predicted label ŷ ∈ {wildfire, non-wildfire}

1. Initialize the parameters of the improved AlexNet  
2. For each training epoch do  
3. For each mini-batch {(xi, yi)} in D do  
4. Resize and normalize the input image xi  
5. Perform data augmentation on xi  
6. Extract low-level features using Conv1  
7. Reduce the spatial dimension using MaxPool  
8. Extract intermediate features using Conv2  
9. Enhance multi-scale contextual information using Light-MSA  
10. Further extract semantic features using Conv3  
11. Perform lightweight multi-scale feature fusion using the RepGhost-Inception module  
12. Generate high-level feature maps using Conv4  
13. Refine discriminative representations using the Hybrid Pooling Attention module  
14. Feed the refined features into the fully connected classification layer  
15. Obtain the prediction probability pi  
16. Compute the classification loss between pi and yi  
17. Update the network parameters by backpropagation  
18. End for  
19. End for  
20. For a test image, perform the same forward process from Step 4 to Step 15  
21. Output the predicted label ŷ