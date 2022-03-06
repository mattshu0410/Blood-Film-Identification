# Blood-Film-Identification

The current process for interpreting blood films within a haematology lab involves automated haematology analysers. These machines perform blood cell counts autonomously however when a sample is flagged, the blood smear must be reviewed manually which is extremely labour intensive. Furthermore, in some rural/regional areas where haematology labs are too expensive, blood samples have to be sent to metropolitan areas to be analysed. Our overarching goal is to be able to automate the identification of diseased white blood cells within a sample using a deep learning model and present them to a haematologist for confirmation. 

## Object Detection

The first stage involves training a YOLOv5s object detection model on BCCD dataset. This is model is then successively applied on slices of larger blood sample images with SAHI. The white blood cells - being the primary focus - are then cropped out.

## Classfication

This second stage involves training a ResNet34 classifer on Acevedo white blood cell dataset. It will then be fed the cropped-out white blood cells from the object detection stage for classification.

## Feature Extraction

This third stage involves... (TBA)
