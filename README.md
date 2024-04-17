# VTON : A 2D Virtual Try-On (DS5500 : Data Science Capstone Project)

## Author: Dilshath Shaik

## Abstract:

In this project, we explore the rapidly growing field of virtual try-on technology, which has become increasingly important with the rise of online shopping. Our approach introduces a new method that overcomes some of the typical challenges faced by current technologies, such as limited resolution and inaccuracies in how clothing fits onto a user's digital avatar. By using advanced image synthesis and deep learning models, our system can create high-resolution, realistic simulations of how different outfits will look on a person. We focused on ensuring that the clothing aligns accurately with the wearer’s body and pose, and that the fabric's texture and flow are realistically depicted. Our results show a clear improvement over existing methods, offering sharper images and more precise garment fitting. This project not only enhances the online shopping experience but also paves the way for future advancements in the field of virtual apparel trials.

## Introduction:

The digital transformation of the retail industry has been markedly accelerated by advancements in technology, particularly in the realm of e-commerce. Among the most promising developments in this field is virtual try-on technology, which allows consumers to visualize themselves in clothing through digital platforms before making a purchase. This innovation not only enhances the online shopping experience but also aims to reduce return rates caused by sizing issues or unmet expectations regarding fit and style.

The concept of virtual try-on systems is not new; however, traditional methods have struggled with issues such as low resolution, poor alignment of clothing with the user’s body, and unrealistic rendering of fabric properties. These limitations can detract from the user experience and fail to convincingly simulate the physical try-on experience.

In response to these challenges, our project introduces an advanced approach using deep learning techniques and image synthesis to create high-resolution, accurate representations of how clothes fit on a person’s digital avatar. Our method leverages state-of-the-art models in semantic segmentation, geometric matching, and texture rendering to ensure that the digital garments adhere closely to the user’s body contours and movements, and that the fabric’s dynamics are realistically portrayed.

This introduction sets the stage for a detailed discussion on our innovative solution, its implementation, and the tangible benefits it offers to both consumers and retailers in the e-commerce landscape.

## Methods:

The methodology unfolds in four major stages, as described below:

### Pre-processing:
The user's image I and its corresponding segmentation map S are processed to generate a clothing-agnostic version of the person's image I_a. This involves the removal of the clothing and arms from the image to prepare for the virtual try-on.
Simultaneously, the pose of the person P is estimated, which provides a skeletal framework that is crucial for aligning the new clothing item with the person's posture.

### Segmentation Generation:

The Segmentation Generator takes the pose map P and the clothing-agnostic person image I_a to synthesize a new segmentation map. This map predicts how the new garment will fit onto the person's body, segmenting the image into distinct regions like the torso, limbs, and the garment itself.

### Clothes Deformation:

The Geometric Matching Module (GMM) uses the clothing image c, the pose P, and the synthetic segmentation to warp the clothing item so that it aligns with the pose and body shape of the user. This step is critical to ensure that the garment conforms to the right contours and orientation of the person's figure.

### Try-On Synthesis:

In the final stage, the ALIAS Generator merges the deformed clothing with the user's clothing-agnostic image. It intelligently handles areas where the clothing item does not align perfectly with the body (M_misalign) to create a seamless composite.
The ALIAS Generator takes the inputs I_a ⊕ P ⊕ W(c, θ) (where W(c, θ) represents the warped clothing image) and synthesizes the final output image Ĩ. This output showcases the user wearing the selected outfit with realistic folds, shadows, and textures, as if the user is actually wearing the garment.

## Experimental Results(Evaluation):



## Discussion (analysis):



## Statement of contributions:

## Conclusion:

## References:

