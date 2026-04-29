# DeepLearning-Paper-with-Code

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![CV](https://img.shields.io/badge/CV-Computer%20Vision-blue) ![AIGC](https://img.shields.io/badge/AIGC-Generative%20AI-orange) ![VLM](https://img.shields.io/badge/VLM-Vision--Language-purple) ![LLM](https://img.shields.io/badge/LLM-Large%20Language%20Model-green)

There are paper with code for CV / AIGC / LLM / VLM.

[Updating...]

- **AIGC** (AI Generated Content)
    - [GAN](#Generative-Adversarial-Network)
    - [VAE](#Variational-Auto-Encoder)
    - [Diffusion](#Diffusion-Model)
- **LLM / VLM** (Large Language Model / Vision-Language Model)
    - [Transformer](#Attention-or-Transformer)
    - [ViT](#Vision-Transformer)
- **CV** (Computer Vision)
    - [Backbone](#Backbone)
    - [Optimization](#Optimization)
    - [Detection](#Object-Detection)
    - [Segmentation](#Object-Segmentation)
    - [Tracking](#Object-Tracking)
        - MOT
        - VOT
    - [FSS](#Few-Shot-Segmentation)
    - [FSL](#Few-Shot-Learning)
    - [3D-Face](#3D-Face-Reconstruction-and-Facial-Animation)
    - Others
        - [Detection-3D](#3D-Object-Detection)
        - [RGBD-SOT](#Salient-Object-Detection)
    - [Survey](#Survey)


## Generative Adversarial Network
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| GAN | [Generative Adversarial Networks](https://arxiv.org/abs/1406.2661) | arXiv(2014) | [code]
| pix2pix | [Image-to-Image Translation with Conditional Adversarial Networks](https://arxiv.org/abs/1611.07004) | arXiv(2016) / CVPR(2017) | [PyTorch](https://github.com/phillipi/pix2pix)
| CycleGAN | [Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks](https://arxiv.org/abs/1703.10593) | ICCV(2017) | [PyTorch](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix)
| pix2pixHD | [High-Resolution Image Synthesis and Semantic Manipulation with Conditional GANs](https://arxiv.org/abs/1711.11585) | arXiv(2017) / CVPR(2018) | [PyTroch](https://github.com/NVIDIA/pix2pixHD)
| BeautyGAN | [BeautyGAN: Instance-level Facial Makeup Transfer with Deep Generative Adversarial Network](http://liusi-group.com/pdf/BeautyGAN-camera-ready_2.pdf) | ACM MM(2018) | [TensorFlow](http://liusi-group.com/projects/BeautyGAN)
| StyleGAN | [A Style-Based Generator Architecture for Generative Adversarial Networks](https://arxiv.org/abs/1812.04948) | arXiv(2018) / CVPR(2019) | [TensorFlow](https://github.com/NVlabs/stylegan)
| StyleGAN2 | [Analyzing and Improving the Image Quality of StyleGAN](https://arxiv.org/abs/1912.04958) | arXiv(2019) / CVPR(2020) | [TensorFlow](https://github.com/NVlabs/stylegan2)
| StyleGAN2-ADA | [Training Generative Adversarial Networks with Limited Data](https://arxiv.org/abs/2006.06676) | NIPS(2020) | [PyTorch](https://github.com/NVlabs/stylegan2-ada-pytorch)
| StyleCLIP | [StyleCLIP: Text-Driven Manipulation of StyleGAN Imagery](https://arxiv.org/abs/2103.17249) | ICCV(2021) | [PyTorch](https://github.com/orpatashnik/StyleCLIP)
| MobileStyleGAN | [MobileStyleGAN: A Lightweight Convolutional Neural Network for High-Fidelity Image Synthesis](https://arxiv.org/abs/2104.04767) | arXiv(2021) | [PyTorch](https://github.com/bes-dev/MobileStyleGAN.pytorch)
| StyleGAN3 | [Alias-Free Generative Adversarial Networks](https://arxiv.org/abs/2106.12423) | NIPS(2021) | [PyTorch](https://github.com/NVlabs/stylegan3)
| HairCLIP | [HairCLIP: Design Your Hair by Text and Reference Image](https://arxiv.org/abs/2112.05142) | CVPR(2022) | [PyTorch](https://github.com/wtybest/HairCLIP)
| HairMapper | [HairMapper: Removing Hair from Portraits Using GANs](https://onethousandwu.com/HairMapper.github.io/) | CVPR(2022) | [PyTorch](https://github.com/oneThousand1000/HairMapper)
> More implementation for GANs can be found in [PyTorch-GAN](https://github.com/eriklindernoren/PyTorch-GAN)

## Variational Auto-Encoder
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| VAE | [Auto-Encoding Variational Bayes](https://arxiv.org/abs/1312.6114) | arXiv(2013) / ICLR(2014) | [PyTorch](https://github.com/AntixK/PyTorch-VAE)
> More implementation for VAEs can be found in [PyTorch-VAE](https://github.com/AntixK/PyTorch-VAE).

## Diffusion Model
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| DDPM | [Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2006.11239) | arXiv(2020) / NIPS(2020) | [PyTorch](https://github.com/lucidrains/denoising-diffusion-pytorch)

---

## Attention or Transformer
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| Transformer | [Attention Is All You Need](http://arxiv.org/abs/1706.03762) | arXiv(2017) | [TensorFlow](https://github.com/tensorflow/tensor2tensor)
| Non-local | [Non-local Neural Networks](https://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Non-Local_Neural_Networks_CVPR_2018_paper.pdf) | CVPR(2018) | [PyTorch](https://github.com/facebookresearch/video-nonlocal-net)
| [Image Transformer](https://gojay.top/2020/05/15/Image-Transformer/) | [Image Transformer](https://arxiv.org/abs/1802.05751) | arXiv(2018) | [code]
| ViT | [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](http://arxiv.org/abs/2010.11929) | arXiv(2020) | [PyTorch](https://github.com/google-research/vision_transformer)
| Swin Transformer | [Swin Transformer: Hierarchical Vision Transformer using Shifted Windows](https://arxiv.org/abs/2103.14030) | arXiv(2021) | [PyTorch](https://github.com/microsoft/Swin-Transformer)
| ResT | [ResT: An Efficient Transformer for Visual Recognition](http://arxiv.org/abs/2105.13677) | arXiv(2021) | [PyTorch](https://github.com/wofmanaf/ResT)
| DS-Net | [Dual-stream Network for Visual Recognition](http://arxiv.org/abs/2105.14734) | arXiv(2021) | [code]
| TransCNN | [Transformer in Convolutional Neural Networks](http://arxiv.org/abs/2106.03180) | arXiv(2021) | [PyTorch](https://github.com/yun-liu/TransCNN)
| Shuffle Transformer | [Shuffle Transformer: Rethinking Spatial Shuffle for Vision Transformer](http://arxiv.org/abs/2106.03650) | arXiv(2021) | [PyTorch](https://github.com/speedinghzl/ShuffleTransformer)

## Vision Transformer
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| ViT | [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929) | arXiv(2020) / ICLR(2021) | [PyTorch](https://github.com/lucidrains/vit-pytorch)
> More implementation for ViTs can be found in [vit-pytorch](https://github.com/lucidrains/vit-pytorch).

---

## Backbone
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| LeNet-5 | [Gradient-based learning applied to document recognition](http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf) | IEEE(1998) | [code]
| AlexNet | [ImageNet Classification with Deep Convolutional Neural Networks](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf) | NIPS(2012) | [code]
| [NIN](https://gojay.top/2019/08/31/NIN-Network-In-Network/) | [Network In Network](https://arxiv.org/abs/1312.4400) | arXiv(2013) | [PyTorch](https://github.com/Gojay001/DeepLearning-pwcn/tree/master/Classification/NIN/Code)
| VGG | [Very Deep Convolutional Networks for Large-Scale Image Recognition](https://arxiv.org/abs/1409.1556) | ICLR(2015) | [code]
| [GoogLeNet](https://gojay.top/2019/09/05/GoogLeNet/) | [Going deeper with convolutions](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Szegedy_Going_Deeper_With_2015_CVPR_paper.pdf) | CVPR(2015) | [PyTorch](https://github.com/Gojay001/DeepLearning-pwcn/tree/master/Classification/GoogLeNet/Code)
| [ResNet](https://gojay.top/2019/09/08/ResNet/) | [Deep Residual Learning for Image Recognition](http://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf) | CVPR(2016) | [PyTorch](https://github.com/Gojay001/DeepLearning-pwcn/tree/master/Classification/ResNet/Code)
| Inception-v4 | [Inception-v4, Inception-ResNet and the Impact of Residual Connections on Learning](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/viewFile/14806/14311) | AAAI(2017) | [code]
| DenseNet | [Densely Connected Convolutional Networks](http://openaccess.thecvf.com/content_cvpr_2017/papers/Huang_Densely_Connected_Convolutional_CVPR_2017_paper.pdf) | CVPR(2017) | [code]
| DLA | [Deep Layer Aggregation](https://openaccess.thecvf.com/content_cvpr_2018/papers/Yu_Deep_Layer_Aggregation_CVPR_2018_paper.pdf) | CVPR(2018) | [PyTorch](https://github.com/ucbdrive/dla)
| ShuffleNet | [ShuffleNet: An Extremely Efficient Convolutional Neural Network for Mobile Devices](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhang_ShuffleNet_An_Extremely_CVPR_2018_paper.pdf) | CVPR(2018) | [code]
| MobileNetV3 | [Searching for MobileNetV3](http://openaccess.thecvf.com/content_ICCV_2019/papers/Howard_Searching_for_MobileNetV3_ICCV_2019_paper.pdf) | ICCV(2019) | [code]
> More information can be found in [Awesome - Image Classification](https://github.com/weiaicunzai/awesome-image-classification).

## Object Detection
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| R-CNN | [Rich Feature Hierarchies for Accurate Object Detection and Semantic Segmentation](http://openaccess.thecvf.com/content_cvpr_2014/papers/Girshick_Rich_Feature_Hierarchies_2014_CVPR_paper.pdf) | CVPR(2014) | [code]
| SPP | [Spatial Pyramid Pooling in Deep Convolutional Networks for Visual Recognition](https://link.springer.com/content/pdf/10.1007/978-3-319-10578-9_23.pdf) | TPAMI(2015) | [code]
| Fast R-CNN | [Fast R-CNN](http://openaccess.thecvf.com/content_iccv_2015/papers/Girshick_Fast_R-CNN_ICCV_2015_paper.pdf) | ICCV(2015) | [code]
| [Faster R-CNN](https://gojay.top/2019/10/19/Faster-R-CNN/) | [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks](https://arxiv.org/abs/1506.01497) | NIPS(2015) | [PyTorch](https://github.com/Gojay001/faster-rcnn.pytorch)
| SSD | [SSD: Single Shot MultiBox Detector](https://arxiv.org/abs/1512.02325) | ECCV(2016) | [Caffe](https://github.com/weiliu89/caffe/tree/ssd)
| YOLO | [You Only Look Once: Unified, Real-Time Object Detection](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Redmon_You_Only_Look_CVPR_2016_paper.pdf) | CVPR(2016) | [code]
| YOLOv2 | [YOLO9000: Better, Faster, Stronger](http://openaccess.thecvf.com/content_cvpr_2017/papers/Redmon_YOLO9000_Better_Faster_CVPR_2017_paper.pdf) | CVPR(2017) | [code]
| FPN | [Feature Pyramid Networks for Object Detection](http://openaccess.thecvf.com/content_cvpr_2017/papers/Lin_Feature_Pyramid_Networks_CVPR_2017_paper.pdf) | CVPR(2017) | [code]
| RetinaNet | [Focal Loss for Dense Object Detection](https://openaccess.thecvf.com/content_ICCV_2017/papers/Lin_Focal_Loss_for_ICCV_2017_paper.pdf) | ICCV(2017) | [code]
| YOLOv3 | [YOLOv3: An Incremental Improvement](https://arxiv.org/abs/1804.02767) | arXiv(2018) | [Offical](https://github.com/pjreddie/darknet)
| CornerNet | [CornerNet: Detecting Objects as Paired Keypoints](https://openaccess.thecvf.com/content_ECCV_2018/papers/Hei_Law_CornerNet_Detecting_Objects_ECCV_2018_paper.pdf) | ECCV(2018) | [PyTorch](https://github.com/princeton-vl/CornerNet)
| CenterNet | [Objects as Points](https://arxiv.org/abs/1904.07850) | arXiv(2019) | [PyTorch](https://github.com/xingyizhou/CenterNet)
| YOLOv4 | [YOLOv4: Optimal Speed and Accuracy of Object Detection](https://arxiv.org/abs/2004.10934) | arXiv(2020) | [Offical](https://github.com/AlexeyAB/darknet)
| YOLOF | [You Only Look One-level Feature](https://arxiv.org/abs/2103.09460) | CVPR(2021) | [PyTorch](https://github.com/megvii-model/YOLOF)
> More information can be found in [awesome-object-detection](https://github.com/amusi/awesome-object-detection).

## Object Segmentation
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| FCN | [Fully convolutional networks for semantic segmentation](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Long_Fully_Convolutional_Networks_2015_CVPR_paper.pdf) | CVPR(2015) | [PyTorch](https://github.com/yassouali/pytorch_segmentation)
| U-Net | [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/abs/1505.04597) | MICCAI(2015) | [PyTorch](https://github.com/yassouali/pytorch_segmentation)
| Seg-Net | [SegNet: A Deep Convolutional Encoder-Decoder Architecture for Robust Semantic Pixel-Wise Labelling](https://arxiv.org/abs/1505.07293) | arXiv(2015) | [PyTorch](https://github.com/yassouali/pytorch_segmentation)
| DeepLab V1 | [Semantic Image Segmentation with Deep Convolutional Nets and Fully Connected CRFs](https://arxiv.org/abs/1412.7062) | arXiv(2014) / ICLR(2015) | [PyTorch](https://github.com/yassouali/pytorch_segmentation)
| PSPNet | [Pyramid Scene Parsing Network](https://openaccess.thecvf.com/content_cvpr_2017/papers/Zhao_Pyramid_Scene_Parsing_CVPR_2017_paper.pdf) | CVPR(2017) | [PyTorch](https://github.com/yassouali/pytorch_segmentation)
| DeepLab V2 | [DeepLab: Semantic Image Segmentation with Deep Convolutional Nets, Atrous Convolution, and Fully Connected CRFs](https://arxiv.org/abs/1606.00915) | arXiv(2016) / TPAMI(2017) | [PyTorch](https://github.com/yassouali/pytorch_segmentation)
| [Mask R-CNN](https://gojay.top/2020/08/17/Mask-R-CNN/) | [Mask R-CNN](http://openaccess.thecvf.com/content_ICCV_2017/papers/He_Mask_R-CNN_ICCV_2017_paper.pdf) | ICCV / TPAMI(2017) | [PyTorch](https://github.com/facebookresearch/detectron2)
| DeepLab V3 | [Rethinking Atrous Convolution for Semantic Image Segmentation](https://arxiv.org/abs/1706.05587) | arXiv(2017) | [PyTorch](https://github.com/yassouali/pytorch_segmentation)
| PointNet | [PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation](https://openaccess.thecvf.com/content_cvpr_2017/papers/Qi_PointNet_Deep_Learning_CVPR_2017_paper.pdf) | CVPR(2017) | [PyTorch](https://github.com/fxia22/pointnet.pytorch)
| PointNet++ | [PointNet++: Deep Hierarchical Feature Learning on Point Sets in a Metric Space](https://proceedings.neurips.cc/paper/2017/file/d8bf84be3800d12f74d8b05e9b89836f-Paper.pdf) | NIPS(2017) | [PyTorch](https://github.com/erikwijmans/Pointnet2_PyTorch)
| DeepLab V3+ | [Encoder-Decoder with Atrous Separable Convolution for Semantic Image Segmentation](https://openaccess.thecvf.com/content_ECCV_2018/papers/Liang-Chieh_Chen_Encoder-Decoder_with_Atrous_ECCV_2018_paper.pdf) | ECCV(2018) | [PyTorch](https://github.com/yassouali/pytorch_segmentation)
| DGCNet | [Dual Graph Convolutional Network for Semantic Segmentation](https://arxiv.org/abs/1909.06121) | BMVC(2019) | [PyTorch](https://github.com/lxtGH/GALD-DGCNet)
| SETR | [Rethinking Semantic Segmentation from a Sequence-to-Sequence Perspective with Transformers](http://arxiv.org/abs/2012.15840) | CVPR(2021) | [PyTorch](https://github.com/fudan-zvg/SETR)
| Segmenter | [Segmenter: Transformer for Semantic Segmentation](http://arxiv.org/abs/2105.05633) | arXiv(2021) | [PyTorch](https://github.com/rstrudel/segmenter)
| SegFormer | [SegFormer: Simple and Efficient Design for Semantic Segmentation with Transformers](http://arxiv.org/abs/2105.15203) | arXiv(2021) | [PyTorch](https://github.com/NVlabs/SegFormer)
| FTN | [Fully Transformer Networks for Semantic ImageSegmentation](http://arxiv.org/abs/2106.04108) | arXiv(2021) | [code]

## Object Tracking
### MOT (Multiple Object Tracking)
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| [SORT](https://gojay.top/2020/06/14/SORT/) | [Simple Online and Realtime Tracking](https://arxiv.org/abs/1602.00763) | ICIP(2016) | [PyTorch](https://github.com/abewley/sort)
| [DeepSORT](https://gojay.top/2020/06/20/DeepSORT/) | [Simple Online and Realtime Tracking with a Deep Association Metric](https://arxiv.org/abs/1703.07402) | ICIP(2017) | [PyTorch](https://github.com/nwojke/deep_sort)
| [Tracktor](https://gojay.top/2019/11/09/Tracktor/) | [Tracking without bells and whistles](https://arxiv.org/abs/1903.05625) | ICCV(2019) | [PyTorch](https://github.com/Gojay001/tracking_wo_bnw)
| [FFT](https://gojay.top/2020/03/05/FFT-Flow-Fuse-Tracker/) | [Multiple Object Tracking by Flowing and Fusing](https://arxiv.org/abs/2001.11180) | arXiv(2020) | [code]
| [JRMOT](https://gojay.top/2020/02/28/JRMOT/) | [JRMOT: A Real-Time 3D Multi-Object Tracker and a New Large-Scale Dataset](https://arxiv.org/abs/2002.08397) | arXiv(2020) | [code]
| [Tracklet](https://gojay.top/2020/03/26/Tracklet/) | [Multi-object Tracking via End-to-end Tracklet Searching and Ranking](https://arxiv.org/abs/2003.02795) | arXiv(2020) | [code]
| DMCT | [Real-time 3D Deep Multi-Camera Tracking](https://arxiv.org/abs/2003.11753) | arXiv(2020) | [code]
| [FairMOT](https://gojay.top/2020/05/25/FairMOT/) | [A Simple Baseline for Multi-Object Tracking](https://arxiv.org/abs/2004.01888) | arXiv(2020) | [PyTorch](https://github.com/Gojay001/FairMOT)
| CenterPoint | [Center-based 3D Object Detection and Tracking](https://arxiv.org/pdf/2006.11275.pdf) | CVPR(2021) | [PyTorch](https://github.com/tianweiy/CenterPoint)

### VOT (Visual Object Tracking)
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| DepthTrack | [Real-time depth-based tracking using a binocular camera](https://github.com/Gojay001/DeepLearning-pwcn/tree/master/Tracking/Binocular%20camera/DepthTrack.pdf) | WCICA(2016) | [code]
| BinocularTrack | [Research on Target Tracking Algorithm Based on Parallel Binocular Camera](https://github.com/Gojay001/DeepLearning-pwcn/blob/master/Tracking/Binocular%20camera/BinocularTrack.pdf) | ITAIC(2019) | [code]
| SiamFC| [Fully-Convolutional Siamese Networks for Object Tracking](https://arxiv.org/abs/1606.09549) | ECCV(2016) | [PyTorch](https://github.com/zllrunning/SiameseX.PyTorch)
| SiamRPN| [High Performance Visual Tracking with Siamese Region Proposal Network](https://openaccess.thecvf.com/content_cvpr_2018/papers/Li_High_Performance_Visual_CVPR_2018_paper.pdf) | CVPR(2018) | [PyTorch](https://github.com/huanglianghua/siamrpn-pytorch)
| [SiamRPN++](https://gojay.top/2020/05/09/SiamRPN++/) | [SiamRPN++: Evolution of Siamese Visual Tracking with Very Deep Networks](http://openaccess.thecvf.com/content_CVPR_2019/papers/Li_SiamRPN_Evolution_of_Siamese_Visual_Tracking_With_Very_Deep_Networks_CVPR_2019_paper.pdf) | CVPR(2019) | [PyTorch](https://github.com/STVIR/pysot)
| [SiamMask](https://gojay.top/2019/11/26/SiamMask/) | [Fast Online Object Tracking and Segmentation: A Unifying Approach](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Fast_Online_Object_Tracking_and_Segmentation_A_Unifying_Approach_CVPR_2019_paper.pdf) | CVPR(2019) | [PyTorch](https://github.com/Gojay001/SiamMask)
| [GlobalTrack](https://gojay.top/2020/01/04/GlobalTrack/) | [GlobalTrack: A Simple and Strong Baseline for Long-term Tracking](https://arxiv.org/abs/1912.08531) | AAAI(2020) | [PyTorch](https://github.com/huanglianghua/GlobalTrack)
| SiamCAR | [SiamCAR: Siamese Fully Convolutional Classification and Regression for Visual Tracking](https://openaccess.thecvf.com/content_CVPR_2020/papers/Guo_SiamCAR_Siamese_Fully_Convolutional_Classification_and_Regression_for_Visual_Tracking_CVPR_2020_paper.pdf) | CVPR(2020) | [PyTorch](https://github.com/ohhhyeahhh/SiamCAR)
| SiamBAN | [Siamese Box Adaptive Network for Visual Tracking](https://openaccess.thecvf.com/content_CVPR_2020/papers/Chen_Siamese_Box_Adaptive_Network_for_Visual_Tracking_CVPR_2020_paper.pdf) | CVPR(2020) | [PyTorch](https://github.com/hqucv/siamban)
| SiamAttn | [Deformable Siamese Attention Networks for Visual Object Tracking](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yu_Deformable_Siamese_Attention_Networks_for_Visual_Object_Tracking_CVPR_2020_paper.pdf) | CVPR(2020) | [PyTorch](https://github.com/msight-tech/research-siamattn)
| [PAMCC-AOT](https://gojay.top/2020/02/25/PAMCC-AOT/) | [Pose-Assisted Multi-Camera Collaboration for Active Object Tracking](https://arxiv.org/abs/2001.05161) | AAAI(2020) | [code]
| [TSDM](https://gojay.top/2020/05/23/TSDM/) | [TSDM: Tracking by SiamRPN++ with a Depth-refiner and a Mask-generator](https://arxiv.org/abs/2005.04063) | arXiv(2020) | [PyTorch](https://github.com/Gojay001/TSDM)
| SiamGAT | [Graph Attention Tracking](https://arxiv.org/abs/2011.11204) | CVPR(2021) | [PyTorch](https://github.com/ohhhyeahhh/SiamGAT)
| RE-SiamNets | [Rotation Equivariant Siamese Networks for Tracking](https://arxiv.org/abs/2012.13078) | CVPR(2021) | [PyTorch](https://github.com/dkgupta90/re-siamnet)

## Few-Shot Segmentation
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| [OSLSM](https://gojay.top/2020/10/19/OSLSM/) | [One-Shot Learning for Semantic Segmentation](https://arxiv.org/abs/1709.03410) | BMVC(2017) | [Caffe](https://github.com/lzzcd001/OSLSM)
| [co-FCN](https://gojay.top/2020/10/19/co-FCN/) | [Conditional Networks for Few-Shot Semantic Segmentation](https://openreview.net/pdf?id=SkMjFKJwG) | ICLR(2018) | [code]
| AMP | [AMP: Adaptive Masked Proxies for Few-Shot Segmentation](https://openaccess.thecvf.com/content_ICCV_2019/papers/Siam_AMP_Adaptive_Masked_Proxies_for_Few-Shot_Segmentation_ICCV_2019_paper.pdf) | ICCV(2019) | [Pytorch](https://github.com/MSiam/AdaptiveMaskedProxies)
| [SG-One](https://gojay.top/2020/10/20/SG-One/) | [SG-One: Similarity Guidance Network for One-Shot Semantic Segmentation](https://arxiv.org/abs/1810.09091) | arXiv(2018) / TCYB(2020) | [PyTorch](https://github.com/xiaomengyc/SG-One)
| CENet | [Learning Combinatorial Embedding Networks for Deep Graph Matching](https://openaccess.thecvf.com/content_ICCV_2019/papers/Wang_Learning_Combinatorial_Embedding_Networks_for_Deep_Graph_Matching_ICCV_2019_paper.pdf) | ICCV(2019) | [Pytorch](https://github.com/Thinklab-SJTU/PCA-GM)
| PANet | [PANet: Few-Shot Image Semantic Segmentation with Prototype Alignment](http://openaccess.thecvf.com/content_ICCV_2019/papers/Wang_PANet_Few-Shot_Image_Semantic_Segmentation_With_Prototype_Alignment_ICCV_2019_paper.pdf) | ICCV(2019) | [PyTorch](https://github.com/kaixin96/PANet)
| [CANet](https://gojay.top/2020/10/20/CANet/) | [CANet: Class-Agnostic Segmentation Networks with Iterative Refinement and Attentive Few-Shot Learning](https://openaccess.thecvf.com/content_CVPR_2019/papers/Zhang_CANet_Class-Agnostic_Segmentation_Networks_With_Iterative_Refinement_and_Attentive_Few-Shot_CVPR_2019_paper.pdf) | CVPR(2019) | [PyTorch](https://github.com/icoz69/CaNet)
| [PGNet](https://gojay.top/2020/07/28/PGNet/) | [Pyramid Graph Networks with Connection Attentions for Region-Based One-Shot Semantic Segmentation](https://openaccess.thecvf.com/content_ICCV_2019/papers/Zhang_Pyramid_Graph_Networks_With_Connection_Attentions_for_Region-Based_One-Shot_Semantic_ICCV_2019_paper.pdf) | ICCV(2019) | [code]
| [CRNet](https://gojay.top/2020/07/10/CRNet/) | [CRNet: Cross-Reference Networks for Few-Shot Segmentation](https://openaccess.thecvf.com/content_CVPR_2020/papers/Liu_CRNet_Cross-Reference_Networks_for_Few-Shot_Segmentation_CVPR_2020_paper.pdf) | CVPR(2020) | [code]
| FGN | [FGN: Fully Guided Network for Few-Shot Instance Segmentation](https://openaccess.thecvf.com/content_CVPR_2020/papers/Fan_FGN_Fully_Guided_Network_for_Few-Shot_Instance_Segmentation_CVPR_2020_paper.pdf) | CVPR(2020) | [code]
| OTB | [On the Texture Bias for Few-Shot CNN Segmentation](https://arxiv.org/abs/2003.04052) | arXiv(2020) | [TensorFlow](https://github.com/rezazad68/fewshot-segmentation)
| [LTM](https://gojay.top/2020/07/29/LTM/) | [A New Local Transformation Module for Few-Shot Segmentation](https://arxiv.org/abs/1910.05886) | MMMM(2020) | [code]
| SimPropNet | [SimPropNet: Improved Similarity Propagation for Few-shot Image Segmentation](https://arxiv.org/abs/2004.15014) | IJCAI(2020) | [code]
| [PPNet](https://gojay.top/2020/12/02/PPNet/) | [Part-aware Prototype Network for Few-shot Semantic Segmentation](https://arxiv.org/abs/2007.06309) | ECCV(2020) | [PyTorch](https://github.com/Xiangyi1996/PPNet-PyTorch)
| PFENet | [PFENet: Prior Guided Feature Enrichment Network for Few-shot Segmentation](https://arxiv.org/abs/2008.01449) | TPAMI(2020) | [PyTorch](https://github.com/Jia-Research-Lab/PFENet)
| PMMs | [Prototype Mixture Models for Few-shot Semantic Segmentation](https://arxiv.org/abs/2008.03898) | ECCV(2020) | [PyTorch](https://github.com/Yang-Bob/PMMs)
| GFS-Seg | [Generalized Few-Shot Semantic Segmentation](https://arxiv.org/abs/2010.05210) | arXiv(2020) | [code]
| SCL | [Self-Guided and Cross-Guided Learning for Few-Shot Segmentation](https://arxiv.org/pdf/2103.16129.pdf) | CVPR(2021) | [PyTorch](https://github.com/zbf1991/SCL)
| ASGNet | [Adaptive Prototype Learning and Allocation for Few-Shot Segmentation](https://arxiv.org/pdf/2104.01893.pdf) | CVPR(2021) | [PyTorch](https://github.com/Reagan1311/ASGNet)
| HSNet | [Hypercorrelation Squeeze for Few-Shot Segmenation](https://openaccess.thecvf.com/content/ICCV2021/papers/Min_Hypercorrelation_Squeeze_for_Few-Shot_Segmentation_ICCV_2021_paper.pdf) | ICCV(2021) | [PyTorch](https://github.com/juhongm999/hsnet)
| BAM | [Learning What Not to Segment: A New Perspective on Few-Shot Segmentation](https://arxiv.org/abs/2203.07615) | CVPR(2022) | [PyTorch](https://github.com/chunbolang/BAM)
> More information can be found in [Few-Shot-Semantic-Segmentation-Papers](https://github.com/xiaomengyc/Few-Shot-Semantic-Segmentation-Papers).

## Few-Shot Learning
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| [RN](https://gojay.top/2019/08/21/RN-Realation-Network/) | [Learning to Compare: Relation Network for Few-Shot Learning](https://arxiv.org/abs/1711.06025) | CVPR(2018) | [PyTorch](https://github.com/Gojay001/LearningToCompare_FSL)
| SimSiam | [Exploring Simple Siamese Representation Learning](https://arxiv.org/abs/2011.10566) | CVPR(2021) | [PyTorch](https://github.com/PatrickHua/SimSiam)

## 3D Face Reconstruction and Facial Animation
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| 3DMM | [A Morphable Model For The Synthesis Of 3D Faces](https://dl.acm.org/doi/10.1145/311535.311556) | SIGGRAPH(1999) | [code]
| CameraCalibration | [A Flexible New Technique for CameraCalibration](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/tr98-71.pdf) | TPAMI(2000) | [code]
| Bilinear | [Bilinear Models for 3-D Face andFacial Expression Recognition](https://d1wqtxts1xzle7.cloudfront.net/49198237/tifs.2008.92459820160928-12079-1abw3dh-libre.pdf?1475124509=&response-content-disposition=inline%3B+filename%3DBilinear_Models_for_3_D_Face_and_Facial.pdf&Expires=1678444054&Signature=LMHkODHpSWWRiDuM1HKyl9vtuq7oTkysoLJEm8eXLlkGR~qQT1JFJzNc0dLj3rPBSWEPMuUKA7WILvlwOJFdzW6wej0vnyavrdQyct~v3eBgYomgzGz70QML7EL3K8VjuuI8rJ6ruMgus6wD8dcUh4et3tAvPZKu7CNv7DW0sP2hP-PwhNDf~8wgb0EJQdN7sd-5cSjkcKgMlt6PJ2WvFiFh3YExXNzrmmE-pa2gzndIYgqMP3H-pNZ5pBSG0OUxJEjOrFyIW9nwmDgxNYQjtwXmZv3hVJ4vMn2RavklUY26UvWd4V9AtW8VBmKq-Uo41lWc2j59sfURFbAVkEwh3g__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA) | TIFS(2008) | [code]
| DDE | [Displaced Dynamic Expression Regression forReal-time Facial Tracking and Animation](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/tr98-71.pdf) | TOG(2014) | [code]
| FaceWarehouse | [FaceWarehouse: a 3D Facial Expression Databasefor Visual Computing](http://kunzhou.net/2012/facewarehouse-tr.pdf) | TVCG(2014) | [code]
| Face2Face | [Face2Face: Real-Time Face Capture and Reenactment of RGB Videos](https://openaccess.thecvf.com/content_cvpr_2016/papers/Thies_Face2Face_Real-Time_Face_CVPR_2016_paper.pdf) | CVPR(2016) | [code]
| DynamicAvatars | [Real-time Facial Animation with Image-based Dynamic Avatars](https://eprints.whiterose.ac.uk/134265/1/TianjiaShao_Realtime_Facial_Animation.pdf/) | TOG(2016) | [code]
| FLAME | [Learning a model of facial shape and expression from 4D scans](https://3dvar.com/Li2017Learning.pdf) | TOG(2017) | [Tensorflow](https://github.com/Rubikplayer/flame-fitting) [PyTorch](https://github.com/soubhiksanyal/FLAME_PyTorch)
| Nonlinear | [Nonlinear 3D Face Morphable Model](http://cvlab.cse.msu.edu/project-nonlinear-3dmm.html) | CVPR(2018) | [Tensorflow](https://github.com/tranluan/Nonlinear_Face_3DMM)
| DynamicRigidityPrior | [Stabilized real-time face tracking via a learned dynamic rigidity prior](https://dl.acm.org/doi/10.1145/3272127.3275093) | TOG(2018) | [code]
| Deep3D | [Accurate 3D Face Reconstruction with Weakly-Supervised Learning: From Single Image to Image Set](https://openaccess.thecvf.com/content_CVPRW_2019/papers/AMFG/Deng_Accurate_3D_Face_Reconstruction_With_Weakly-Supervised_Learning_From_Single_Image_CVPRW_2019_paper.pdf) | CVPR(2019) | [Tensorflow](https://github.com/Microsoft/Deep3DFaceReconstruction) [PyTorch](https://github.com/sicxu/Deep3DFaceRecon_pytorch)
| SimpleAnimation | [Face It!: A Pipeline for Real-Time Performance-Driven Facial Animation](https://www-live.dfki.de/fileadmin/user_upload/import/10613_ICIP2019.pdf) | ICIP(2019) | [code]
| RingNet | [Learning to Regress 3D Face Shape and Expression from an Image without 3D Supervision](https://openaccess.thecvf.com/content_CVPR_2019/papers/Sanyal_Learning_to_Regress_3D_Face_Shape_and_Expression_From_an_CVPR_2019_paper.pdf) | CVPR(2019) | [Tensorflow](https://github.com/soubhiksanyal/RingNet)
| FOCUS | [To fit or not to fit: Model-based Face Reconstruction and Occlusion Segmentation from Weak Supervision](https://arxiv.org/abs/2106.09614) | arXiv(2021) | [PyTorch](https://github.com/unibas-gravis/Occlusion-Robust-MoFA)
| MICA | [Towards Metrical Reconstruction of Human Faces](https://arxiv.org/abs/2204.06607) | ECCV(2022) | [PyTorch](https://github.com/Zielon/MICA)
| HRN | [A Hierarchical Representation Network for Accurate and Detailed Face Reconstruction from In-The-Wild Images](https://arxiv.org/abs/2302.14434) | CVPR(2023) | [PyTorch](https://github.com/youngLBW/HRN)

## Salient Object Detection
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| UC-Net | [UC-Net: Uncertainty Inspired RGB-D Saliency Detection via Conditional Variational Autoencoders](https://openaccess.thecvf.com/content_CVPR_2020/papers/Zhang_UC-Net_Uncertainty_Inspired_RGB-D_Saliency_Detection_via_Conditional_Variational_Autoencoders_CVPR_2020_paper.pdf) | CVPR(2020) | [PyTorch](https://github.com/JingZhang617/UCNet)
| JL-DCF | [JL-DCF: Joint Learning and Densely-Cooperative Fusion Framework for RGB-D Salient Object Detection](https://openaccess.thecvf.com/content_CVPR_2020/papers/Fu_JL-DCF_Joint_Learning_and_Densely-Cooperative_Fusion_Framework_for_RGB-D_Salient_CVPR_2020_paper.pdf) | CVPR(2020) | [PyTorch](https://github.com/jiangyao-scu/JL-DCF-pytorch)
| SA-Gate | [Bi-directional Cross-Modality Feature Propagation with Separation-and-Aggregation Gate for RGB-D Semantic Segmentation](https://arxiv.org/abs/2007.09183) | ECCV(2020) | [PyTorch](https://github.com/charlesCXK/RGBD_Semantic_Segmentation_PyTorch)
| BiANet | [Bilateral Attention Network for RGB-D Salient Object Detection](https://arxiv.org/abs/2004.14582) | TIP(2021) | [Code]
| DSA^2F | [Deep RGB-D Saliency Detection with Depth-Sensitive Attention and Automatic Multi-Modal Fusion](http://arxiv.org/abs/2103.11832) | CVPR(2021) | [Code]

## 3D Object Detection
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| [PV-RCNN](https://gojay.top/2020/06/23/PV-RCNN/) | [PV-RCNN: Point-Voxel Feature Set Abstraction for 3D Object Detection](http://openaccess.thecvf.com/content_CVPR_2020/papers/Shi_PV-RCNN_Point-Voxel_Feature_Set_Abstraction_for_3D_Object_Detection_CVPR_2020_paper.pdf) | CVPR(2020) | [PyTorch](https://github.com/sshaoshuai/PV-RCNN)

## Optimization
| Title | Paper | Conf | Code |
|:--------|:--------:|:--------:|:--------:|
| ReLU | [Deep Sparse Rectifier Neural Networks](http://proceedings.mlr.press/v15/glorot11a/glorot11a.pdf) | JMLR(2011) | [code]
| Momentum | [On the importance of initialization and momentum in deep learning](http://proceedings.mlr.press/v28/sutskever13.html) | ICML(2013) | [code]
| Dropout | [Dropout: a simple way to prevent neural networks from overfitting](https://dl.acm.org/doi/10.5555/2627435.2670313) | JMLR(2014) | [code]
| Adam | [Adam: A Method for Stochastic Optimization](https://arxiv.org/abs/1412.6980) | ICLR(2015) | [code]
| BN | [Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift](https://arxiv.org/abs/1502.03167) | ICML(2015) | [code]
| GDoptimization | [An overview of gradient descent optimization algorithms](https://arxiv.org/abs/1609.04747) | arXiv(2016) | [code]
| StableLoss | [Single-frame regularization for temporally stable cnns](https://arxiv.org/abs/1902.10424) | CVPR(2019) | [code]

## Survey
| Title | Paper | Conf |
|:--------|:--------:|:--------:|
| 3D-Detection-Survey-2019 | [A Survey on 3D Object Detection Methods for Autonomous Driving Applications](http://wrap.warwick.ac.uk/114314/1/WRAP-survey-3D-object-detection-methods-autonomous-driving-applications-Arnold-2019.pdf) | ITS(2019)
| [FSL-Survey-2019](https://gojay.top/2020/07/07/FSL-Survey-2019/) | [Generalizing from a Few Examples: A Survey on Few-Shot Learning](https://arxiv.org/abs/1904.05046) | CSUR(2019)
| MOT-Survey-2020 | [Deep Learning in Video Multi-Object Tracking: A Survey](https://arxiv.org/abs/1907.12740) | Neurocomputing(2020)
| Transformer-Survey-2021 | [A Survey of Transformers](http://arxiv.org/abs/2106.04554) | arXiv(2021)