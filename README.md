# EE231
## HFNET
Run application.ipynb to show our application
Reference:https://github.com/ethz-asl/hfnet
train_explore:  Process of exporting labels of google landmarks with superpoint and netVLAD, and then distill to get the student model.
The outputs are saved in EXPER_PATH, which is too large to be uploaded here but is available on Google Drive.
https://drive.google.com/drive/folders/1EeG0GBsqh271rInTTbPrsRe96g6nuXHL?usp=sharing

output path: hfnet/dataset/EXPER_PATH

test_explore: Process of evaluating the trained models.

The datasets are downloaded as indicated in the [dataset documentation](doc/datasets.md). SfM models of Aachen, RobotCar, CMU, and Extended CMU, built SuperPoint and usable with HF-Net, are provided [here](https://projects.asl.ethz.ch/datasets/doku.php?id=cvpr2019hfnet). Download and unpack the HF-Net weights in `hfnet/dataset/EXPER_PATH/hfnet/`. To localize with NV+SP, download the network weights of [NetVLAD](http://rpg.ifi.uzh.ch/datasets/netvlad/vd16_pitts30k_conv5_3_vlad_preL2_intra_white.zip) and [SuperPoint](https://github.com/MagicLeapResearch/SuperPointPretrainedNetwork/blob/master/superpoint_v1.pth) and put them in `hfnet/dataset/DATA_PATH/weights/`.



## Superpoint
Reference: https://github.com/rpautrat/SuperPoint
Process of training with synthetic dataset: Superpoint_train_explore.ipynb

output :
https://drive.google.com/drive/folders/1tHNplSRgd6IUNkYT9LgR3UAM6HTM-7D1?usp=sharing

output path: SuperPoint/SuperPointDATA/EXPER_DIR

[MS-COCO 2014](http://cocodataset.org/#download) and [HPatches](http://icvl.ee.ic.ac.uk/vbalnt/hpatches/hpatches-sequences-release.tar.gz) should be downloaded into `SuperPoint/SuperPointDATA/DATA_DIR`. The Synthetic Shapes dataset will also be generated there. The folder structure should look like:
```
$DATA_DIR
|-- COCO
|   |-- train2014
|   |   |-- file1.jpg
|   |   `-- ...
|   `-- val2014
|       |-- file1.jpg
|       `-- ...
`-- HPatches
|   |-- i_ajuntament
|   `-- ...
`-- synthetic_shapes  # will be automatically created
```
