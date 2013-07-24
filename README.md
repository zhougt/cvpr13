cvpr13
======
This package includes the codes and the data related to the SUN 09 dataset. The code files are in code_class_public/. You can start with:

>> cd code_class_public
>> demo

The data files are stored in dataset_dbox_public/. They are:

1. sun09_dbox_class/train_detR/
rootfeat_512.mat: The GIST features for each training image.
class_***/catgy_***.mat: The number after "class_" is the index of an image class. The number after "catgy_" is the index of an object category. The ".mat" file stores the unary object similarities from the training class to each training image. Note that there are five features in measuring the similarities between two objects: color histograms, HoG, texton, LBP and location histograms.
class_***/stats.mat: The number after "class_" is the index of an image class. The ".mat" file stores the numbers of ground-truth objects in each category.

2. sun09_dbox_class/test_detR/ contains similar information for test images.

3. sun09_dbox_results/ saves the learned weights and the measured performance.

4. sun09_dbox_data.mat: the SUN 09 data files
trfiles: the filename of each training image.
tsfiles: the filename of each test image.
objectcategories: the 111 object category names.
dbox: the ground-truth bounding boxes on training images.
dbox_det: the object detection results on training images.
dboxts: the object detection results on test images.
catgy: the object category of each bounding box in dbox.
catgy_det: the object category of each bounding box in dbox_det.
catgyts: the object category of each bounding box in dboxts.
cfc_det: the detection confidence of each bounding box in dbox_det.
cfcts: the detection confidence of each bounding box in dboxts.

5. sun09_dbox_labels.mat: the SUN 09 label files
trfiles: the filename of each training image.
tsfiles: the filename of each test image.
scene_names: the image class names.
labeltr: the labeling matrix of training images.
labelts: the labeling matrix of test images.
clstr: the 58 image classes used in our experiments.

6. sun09_dbox_mstree_exmarr_4.mat: the object spanning tree of each class.
mstree: the tree structures. 1: on-top-of; 2: above; 3: below; 4: next-to. Note that the spatial relation is asymmetric, i.e. sky-above-road indicates road-below-sky. Thus, a negative sign is used to encode the asymmetric relations.
sprlncount: the count of each spatial relation.
