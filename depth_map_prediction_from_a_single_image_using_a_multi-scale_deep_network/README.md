## Depth Map Prediction from a Single Image using a Multi-Scale Deep Network

[[<ins>Paper link</ins>]](https://arxiv.org/abs/1406.2283)

  
  
## Contributions:   
* one of the pilot papers to tackle the supervised depth estimation on a monocular image, that is intrinsically ill-posed problem because the inversion from a 2D image to the corresponding objects in the 3D world is not unique.
* architecture of two deep networks, one to estimates coarse and global depth strucute; another one refines the the results with local details of input images
* introduction of a scale-invariant error to encourage the deep networks weight more on the correctness of relative depth structure than the absolute scale




## Model Architecture: 
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/fig1_reorganized.png" width="1128">





## Invention of a Scale-Invariant Error:
The main source of ambiguity to estimate depth on a single image comes from absolute scale. Hence, this paper proposes a metric to evaluate the quality of a estimated depth map, that focuses on relative relationship between points in a scene rather than the global scale. For instance, if all the points of a estimated depth map are 1/10 of the ground-truth depths, the scale-invariant error would be 0 since the estimation perfectly conserve the relative relationship.

<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq1.png" width="1000">



The scale-invariant error can be derived to a simplified form by letting a new variable. I did not manage to do the derivations through Equation (1) to (3) by myself, but I did write a simple program to calculate their values on some test inputs and check their equivalence. I noticed the denominator of Equation (2) in [its arXiv version](https://arxiv.org/abs/1406.2283) must be multiplied by 2 and realized later the authors have revised it for [the NeurIPS version](https://proceedings.neurips.cc/paper/2014/file/7bccfde7714a1ebadf06c5f4cea752c1-Paper.pdf)
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq2.png" width="1000">

The 1st term of Equation (3) is a normal L2 error, so we can conclude that its 2nd term is responsible to compensate for scale-invariance.  
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq3.png" width="700">


## Training Loss:
The training loss is determined by adding a weighting parameter to the 2nd term of Equation (3) to encourge different degree of scale-invariance.  
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq4.png" width="700">


## Depth Evaluation Metrics:
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/evaluation_metrics.png" width="1000">

## Eigen Split of the KITTI Dataset:
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eigen_split.png" width="1000">
