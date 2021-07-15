# The Temporal Opportunist: Self-Supervised Multi-Frame Monocular Depth

Images in this summary are borrowed or tweaked from those in [<ins>the original paper</ins>](https://arxiv.org/abs/2104.14540) or [its CVPR21 presentation video](https://storage.googleapis.com/niantic-lon-static/research/manydepth/manydepth_cvpr_cc.mp4).  
 </br>
 
## Contributions:   
* Following its previous work MonoDepth2, this paper proposes ManyDepth that is an adaptive self-supervised dense depth estimation approach able to make use of sequence information (multiple frames) at test time when it is available.
<p align="center">
<img src="https://github.com/bolianchen/private-deep-learning-paper-reading/blob/main/the_temporal_opportunist_self_supervised_multi_frame_monocular_depth/images/fig1_v.png" width="480">
</p>

* An adaptive cost volume is proposed to extract and fuse features from multiple frames for depth prediction.  

</br>


## Intentions of Using Multiple Frames at Test Time

## Model Architecture: 
<p align="center">
<img src="https://github.com/bolianchen/private-deep-learning-paper-reading/blob/main/the_temporal_opportunist_self_supervised_multi_frame_monocular_depth/images/fig2_c1.png" width="1080">
</p>

## Key Issues of Applying Cost Volume:
### Cost Volume Overfitting

### Unknown Depth Scale

### Test Frames without Baselines
