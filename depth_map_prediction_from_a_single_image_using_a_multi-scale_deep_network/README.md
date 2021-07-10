## Depth Map Prediction from a Single Image using a Multi-Scale Deep Network

[[<ins>Paper link</ins>]](https://arxiv.org/abs/1406.2283)

  
  
## Contributions:   
* one of the pilot papers to tackle the supervised depth estimation on a monocular image, that is intrinsically ill-posed problem because the inversion from a 2D image to the corresponding objects in the 3D world is not unique.
* architecture of two deep networks, one to estimates coarse and global depth strucute; another one refines the the results with local details of input images
* introduction of a scale-invariant error to encourage the deep networks weight more on the correctness of relative depth structure than the absolute scale




## Model Architecture: 
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/fig1_reorganized.png" width="1128">





## Invention of a Scale-Invariant Error:
The main source of ambiguity to estimate depth on a single image comes from absolute scale. Hence, this paper proposes a metric to evaluate the quality of a estimated depth map, that focuses on relative relationship between points in a scene rather than the global scale.  

<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq1.png" width="1000">



The scale-invariant error can be derived to a simpler form by letting a new variable. 
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq2.png" width="1000">


<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq3.png" width="700">


## Training Loss:
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq4.png" width="700">



<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eval_metrics.png" width="1000">



## KITTI Dataset:
