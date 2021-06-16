HFNET
Run application.ipynb to show our application
Reference:https://github.com/ethz-asl/hfnet
train_explore:  Process of exporting labels of google landmarks with superpoint and netVLAD, and then distill to get the student model.
The outputs are saved in EXPER_PATH, which is too large to be uploaded here but is available on Google Drive.
https://drive.google.com/drive/folders/1EeG0GBsqh271rInTTbPrsRe96g6nuXHL?usp=sharing
output path: hfnet/dataset/EXPER_PATH

test_explore: Process of evaluating the trained models.

The datasets are downloaded as indicated in the https://github.com/ethz-asl/hfnet/blob/master/doc/datasets.md. SfM models of Aachen, RobotCar, CMU, and Extended CMU, built SuperPoint and usable with HF-Net, are provided https://projects.asl.ethz.ch/datasets/doku.php?id=cvpr2019hfnet. Download and unpack the HF-Net weights in $EXPER_PATH/hfnet/. To localize with NV+SP, download the network weights of NetVLAD(http://rpg.ifi.uzh.ch/datasets/netvlad/vd16_pitts30k_conv5_3_vlad_preL2_intra_white.zip) and SuperPoint(https://github.com/MagicLeapResearch/SuperPointPretrainedNetwork/blob/master/superpoint_v1.pth) and put them in $DATA_PATH/weights/.