## [Detecting Pedestrians Using Patterns of Motion and Appearance](http://www.merl.com/publications/docs/TR2003-90.pdf)

1. Pedestrian Detection System 
   * Integrates image intensity inforamtion with motion information.
2. **Intensity** - 
    * The algorithms scans entire input image in order ot find a pattern of intensities which is consistent with the target
    object.
    * Above approach works well for face detection.
    * Performs poorly on pedestrian detection.
    * Images of pedestrians varied - due to changes in body pose and clothing.
    * Video surveillance systems - 
        * Poor resolution of images.
        * This implies only pedestrain target may just occupy 100-200 pixels.
3. **Motion** - Human motion distinguishable from other motions
    * Some approaches have used motion to recognize people and detect them
    * These approaches try to track moving objects over many frames and then analyze the motion
    to look for periodicity or other cues
4. Combine approaches used in *2* and *3* points.
    * Gives good results for low resolution images under difficult conditions such as rain and snow
5. Using rectangle filters which measures:
    * Differences between region averages at various scales, orientations and aspect ration.
6. Extracting motion information from pair or sequence of images in various ways.
    * Block motion estimation
    * Optical Flow - expensive
    * Take difference between pair of images
        * Regions where sum of the absolute values of the differences is large correspond to motion.
        * Information about the direction of the motion can be extracted between shifted versions of the second image in
        time with the first image.
7. Motion filters operate on 5 versions of images:
        * Exact Image
        * Shifted Upwards
        * Shifted Left
        * Shifted Right
        * Shifted Down
5. Training process:
    * Uses AdaBoost ot select a subset of features
    * Appearance filters, Motion Direction filters, Motion Shear Filters, Motion Magnitude filters
    
