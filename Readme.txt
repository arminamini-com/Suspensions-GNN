This package contains the necessary dataset for predicting the force chain network of suspensions in a 2D system, as explained in our referenced paper.

## Contents

1. **Data Conversion**: 
   - The raw data from direct simulations is converted into tensor representations, readable by our graph neural network model. 
   - After conversion, we use the PyTorch Geometric package, DeeperGCN, to train the model.
   - These tensors contain:
     - **Node features**: Size ratio
     - **Edge attributes**: Dimensionless gap, relative distances \( r_{ij} \), \( r_i \), \( r_j \), and the sine and cosine of the angle between particles and the flow direction
     - **Class labels (y)**: 0 if the particle pair is not in frictional contact, 1 if they are in contact

2. **Available Datasets**: 
   - Both the raw data (interaction + particle + data output of suspensions) and tensor datasets (.pt format) are available for use.

3. **Code Availability**: 
   - The code for training and validation is provided.

4. **Handling Imbalanced Datasets**: 
   - For imbalanced datasets, one can use Balanced Cross Entropy (BCE) instead of traditional binary cross entropy. 
   - BCE is a variant of the standard cross-entropy loss function used to address class imbalance issues in binary classification tasks. 
   - In binary classification, cross-entropy loss measures the performance of a model whose output is a probability value between 0 and 1. 
   - When dealing with imbalanced datasets, the standard cross-entropy loss can lead to suboptimal performance as the model may become biased towards the majority class. 
   - BCE introduces a weighting factor to balance the contribution of each class to the overall loss, helping the model pay more attention to the minority class and leading to better performance across both classes.


for more details about the GNN method please go to the below URL:
https://pytorch-geometric.readthedocs.io/en/latest/generated/torch_geometric.nn.models.DeepGCNLayer.html#torch_geometric.nn.models.DeepGCNLayer

***Data at other values of the control parameters can be requested from the authors.
