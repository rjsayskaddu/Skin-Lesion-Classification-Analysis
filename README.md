# Skin-Lesion-Classification-Analysis
 Skin Lesion Classification Analysis: A Comparative Study.<br>
 
 In today’s parlance, there are three standard forms in which skin cancer exists namely
melanoma, squamous cell carcinoma (SCC) and basal cell carcinoma (BCC) of which
melanoma is the most hazardous due to its unpredictable nature. Hence, early detection of
lesions which form the base of skin cancer is required to cure it. To begin with, the approach
of dermoscopy has empowered a sensational lift in clinical diagnostic capacity to the point that
skin cancer can be identified in the clinic at an early stage using either visual dermoscopy or
some other artificial intelligence supported tool. The worldwide acceptance of this technology
has permitted usage of enormous collection of dermoscopy pictures of lesions and benevolent
sores approved by histopathology. The increment of trends in innovations of the regions of
image processing and AI has enabled us to permit differentiation of dangerous lesions from the
numerous benign mimics that require no biopsy. In this paper, using the HAM 10000 dataset,
we compare six different Transfer Learning nets which provide accurate and more classified
identification of lesion images into different form of cancer producing cells. VGG19,
InceptionV3, InceptionResNetV2, ResNet50, Xception and MobileNet transfer learning
techniques are used for comparison of skin lesion. We added layers such as DropOut, Pooling,
Batch Normailzation and Dense in the bottom most layer of transfer learning nets. From the
experimental results, we identified that MobileNet is giving better accuracy when compared
with VGG19, InceptionV3, InceptionResNetV2, ResNet50, Xception nets. 

 There are six different pre trained models used in the project which can be used by changing the import in block[18].<br>
* from keras.applications.inception_v3 import InceptionV3
* from keras.applications.resnet50 import ResNet50
* from keras.applications.vgg19 import VGG19
* from keras.applications.mobilenet import MobileNet
* from keras.applications.inception_resnet_v2 import InceptionResNetV2
* from keras.applications.xception import Xception

## Innovation & novelty?
- The older deep learning approach basically uses two different networks to
individually perform lesion segmentation and classification, but we are using multiscale fully-convolutional residual networks.
- Using ADAM optimizer to reduce memory usage and improve computational
efficiency
- Using the general features as a starting point to evolve new features, we also obtained
better classification accuracy which helped with the discrimination between malignant
and benign skin lesions.
- To keep the advantage of the faster computation time with a high LR, we decreased
the LR dynamically every 3 epochs depending on the validation accuracy. With the
‘ReduceLROnPlateau’, we choose to reduce the LR by half if the accuracy is not
improved after 3 epochs. 
- We decreased LR for every 3 epochs to achieve a global minimum which
isn’t possible if we reduce LR with every epoch. We didn’t use 5 epochs
since it was too time taking. 
