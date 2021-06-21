## Depth Map Prediction from a Single Image using a Multi-Scale Deep Network

[[<ins>Paper link</ins>]](https://arxiv.org/abs/1406.2283)

**<ins>Contributions:</ins>**
* a pilot paper to tackle the depth estimation on a single monocular image, where the inversion from 2D pixels to the corresponding 3D object points is not unique
* a scale-invariant error


<ins>Model Architecture:</ins> 
<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/fig1_reorganized.png" width="1128">


<ins>Intuition behind the Scale-Invariant Error:</ins>
The absolute scale of a scene is intrinsically ambiguous by only looking at a single image.

<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq1.png" width="1000">


<img src="https://github.com/bolianchen/deep-learning-paper-reading/blob/main/depth_map_prediction_from_a_single_image_using_a_multi-scale_deep_network/images/eq2.png" width="1000">
