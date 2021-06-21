## Depth Map Prediction from a Single Image using a Multi-Scale Deep Network

[[<ins>Paper link</ins>]](https://arxiv.org/abs/1406.2283)

### <ins>Contributions:</ins>  

**<ins>Contributions:</ins>**  
* one of the pilot papers to tackle the supervised depth estimation on monocular images, that is intrinsically ill-posed problem because the inversion from a 2D image to the corresponding objects in the 3D world is not unique.
* architecture of two deep networks, one to estimates coarse and global depth strucute; another one refines the the results with local details of input images
* introduction of a scale-invariant error to encourage the deep networks weight more on the correctness of relative depth structure than the absolute scale



**<ins>Model Architecture:</ins>**  
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/fig1_reorganized.png" width="1128">



**<ins>About the Scale-Invariant Error:</ins>**  
The absolute scale of a scene is intrinsically ambiguous by only looking at a single image.



<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq1.png" width="1000">



<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq2.png" width="1000">



<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq3.png" width="700">



<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq4.png" width="700">



<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eval_metrics.png" width="1000">



**<ins>KITTI Dataset:</ins>**  
