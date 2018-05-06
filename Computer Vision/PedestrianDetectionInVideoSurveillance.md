## [Pedestrian detection in video surveillance using fully convolutional YOLO neural network](https://www.researchgate.net/publication/317967088_Pedestrian_detection_in_video_surveillance_using_fully_convolutional_YOLO_neural_network) 

1. Combine detection and classification tasks using CNN.
2. YOLO CNN - Drawbacks:
    * Full connected layers that obstruct applying the CNN to images with different resolution.
    * Limits the ability to disitinguish small close human figures in groups
3. Changed network architecture overcoming above drawbacks.
4. Datasets:
    * Caltech
    * Kitty
    * Moscow city surveillance data
5. Two stages of traning:
    * Pre-trained new added convolutional layers on Caltech, Kitti
        * Didn't freeze the initial layers
    * Fine tune on ow datasets
        * Learning only for new layers
 6. For both stages, 
    * SGD RMSProp
    * Batch Normalisation
