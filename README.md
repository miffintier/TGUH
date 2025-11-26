# TGUH
Text-semantic Guided Unsupervised Community Exploration Hashing for Image Retrieval

# Main Dependencies
-python 3.9.12
-pytorch 1.13.1
-torchvision 0.14.1
-numpy 1.21.5

# Data
The VOC2012, FLICKR25K and MSCOCO datasets are all publicly available.
You can download VOC2012 at https://pjreddie.com/media/files/VOCtrainval_11-May-2012.tar
You can download FLICKR25K at http://press.liacs.nl/mirflickr/mirflickr25k.v3b/mirflickr25k.zip
You can download MSCOCO at http://images.cocodataset.org/zips/train2014.zip   http://images.cocodataset.org/zips/val2014.zip
# Training
First, utilize the pre-trained OFA model to generate text descriptions for images.
````
Then, generate image-text features using CLIP..
````
$cd clip_feature
$ python clip_img_feature.py
$ python clip_text_feature.py
````

Then, create similarity matrix.
$ cd train_Matrix
$ python Create_Matrix.py
````
Then,perform community detection based on similarity matrix.
$ python create_community.py

Then, write the community detection results into run.py.
$ python run.py

The relevant parameters can be adjusted in the file's config.