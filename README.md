# DSRL
Learning Disentangled Semantic Representations for Interpreting CNN-based Object Classification

##Model and dataset

- **model**

The project now supports two different vggs (vgg_16, vgg_13) and alexnet. If you want to use another model, you will need to modify the model as mentioned 
in this project such as extracting the feature values of the last convolutional layer, etc.
- **dataset**

The project now supports **vocpart,  cub200, celeba,  helen**.  You can add your own dataset in the way similar to the datasets above.


##Document Structure
--utils.py [the utility modules used for networks]
--vgg_sncfcm_multi_train.py [the CNN network used for VGGs with space loss and clustering loss]
--vgg_space_multi_train.py [the CNN network used for VGGs with space loss]
--vgg_ncfcm_multi_train.py [the CNN network used for VGGs with clustering loss]
--vgg_ori_multi_train.py [the CNN network used for VGGs]
--SpectralClustering.py [the module of Fuzzy C-means clustering and its evaluation index]
--alexnet_sncfcm_multi_train.py [the CNN network used for alexnet with space loss and clustering loss]
--alexnet_space_multi_train.py [the CNN network used for alexnet with space loss]
--alexnet_ncfcm_multi_train.py [the CNN network used for alexnet with clustering loss]
--alexnet_ori_multi_train.py [the CNN network used for alexnet]
--load_utils.py [the driver of utility modules]
--newPad2d.py [the rewrite of deplicated padding]
--alexnet_visual_train.py [the visualization of feature maps]
--NC_dataset_process_voc.py [the dataset processing and evaluation metric for VOC dataset]
--NC_dataset_process_helen.py [the dataset processing and evaluation metric for Helen dataset]
--NC_dataset_process_celeb.py [the dataset processing and evaluation metric for CelebA dataset]
--NC_dataset_process_voc_multi.py [the dataset processing and evaluation metric for VOC dataset of Multi-category classification]
--NC_dataset_process_cub.py [[the dataset processing and evaluation metric for Cub dataset]

##Requirement

The environment should have all of the following packages:

torch=1.13.0
torchvision=0.14.0
opencv-python
matplotlib
sklearn

##Usage

First get the parameters of the model by running  modelname_sncfcm/space/ncfcm/ori_multi_train.py.
Then qualitatively and quantitatively evaluate the interpretability of the model through runs modelname_visual_train.py 
and NC_dataset_process_datasetname.py, respectively.


## Citation
If you use this project in your research, please cite it.
