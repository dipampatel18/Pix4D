# Pix4D
Creating a 3D Model of the Mascot University of Maryland - The Testudo using [Pix4D](https://www.pix4d.com/)

### What can be done with Pix4D?
Pix4D develops a suite of software products that use photogrammetry and computer vision algorithms to transform DSLR, fisheye, RGB, thermal and multispectral images into 3D maps and 3D model. It creates-
- Point Cloud
- 3D Mesh
- Orthomosaic

## Modeling the Testudo

Since I didn't have a drone, I manually collected nearly 1400 images using a Nikon D3200 DSLR Camera and opted for a Terrestrial option over Aerial. Since I wanted to create a model of Testudo located outside the McKeldin Library, I opted for the Pix4D Model instead of Pix4D Mapper as that would give better results for a model.

<p align="center">
  <img width="650" height="380" src="/Files/Testudo Image.JPG">
</p>

The processing of the images was performed on the Pix4D Cloud as it is faster and more efficient compared to the local machine. I followed the [YouTube Tutorial](https://www.youtube.com/watch?v=ZNKOWP8qAMY&list=PL8ZbncaV3f_anQs_DoyKUxmNDApxM0HT8&index=1) and a short course on [LinkedIn Learning](https://www.linkedin.com/learning/learning-pix4d-drone-mapping/drone-mapping?u=41910388). Anyone willing to learn it, I would highly recommend both the tutorials as they would provide s quick and easy tutorials on all different concepts and techniques.

If you wish to try out the Testudo model, you can [Download]() the Demo Video, Images and Model and use them on the Pix4D trial version. In case you are loading the model in the software, the software would need the source images to properly load all model, so it is advised to download all the images and provide the software with the path of those images whenever prompted. More technical details about the processing can be found in the Report.

<p align="center">
  <img width="650" height="380" src="/Files/Testudo 3D Model.png">
</p>

It is really fascinating to see the precision involved in matching the pixels (also called Tie Points in Pix4D) and thereby creating a realistic 3D model. It also has the feature to measure length, area or volume of a desired object/location. If the model has some pixels off their location, they can be readily edited as per our requirement.

## How Pix4D Works

### Bundle Block Adjustment (BBA)
- Camera's Position - External Camera (EO) and Internal Camera (IO) parameters are calculated
- Determine the camera orientation based on the angles and perspectives
- Points and perspective-angle calculate reconstruction imagery

### Automatic Aerial Triangulation (AAT)
- Detection of prominent points from multiple directions
- Wide overlapping aerial images
- Calculate relative positions - Nodes and Camera

### Photogrammetry
- Measurement and Evaluation Methods of Remote Sensing
- Determine the spatial position
- Determine three-dimensional shape of objects
- Use photographs and accurate measurement images
- Mapped display of data based on photos and positions

***

### Pix4D App
Planning a New Mission
- POLYGON for 2D Maps
- GRID for 2D Maps
- DOUBLE GRID for 3D Models
- CIRCULAR for Single 3D Model
- FREE FLIGHT Advanced Users

### Datum
- Map to real-world location translation
- Latitude, longitde and altitude coordinates
- Anchor base point: locations on the Earth's surface

### Coordinate System
- Specification for every location on Earth
- Numbers, letters, and symbols

### Map Projection
- Geodetic coordinates to plane coordinates
- Projects datum ellipsoidal coordinates and height onto flat map
- Grid system for plotting locations

***

### Getting Started
- Select as many images as you want for the project
- The Coordinate System would be automatically selected. Most of the time, it would be WGS 1984. It can also be edited as per our requirement.
- If the images are taken from a drone or a GPS enabled camera, the Geolocation and Orientation will be available under the Image Properties.
- The software will load the Camera Model automatically from the images as long as that particular model is in the database. If not, the information would be read from EXIF.
- The output coordinate system would also be automatically selected to WGS84. However, we can also modify it to our known coordinate system.
- The Processing Options Template gives us different templates to work on depending upon the type of images captured- aerial, terrestrial or agricultural. 
- In the Map View, the images will be positioned correctly on the map according to their geolocation.
- The Processing Options would now be available and one or more can be selected to start with.

### Georeferencing
- Allows us to place the project on the earth. Can tell us where exactly was our project.
- It can provide scale and orientation
- Situate the Project
- Make measurements
- Provide scale and orientation to the project
- Improves processing time (in case of image geolocation as the software would know which images are close to each other and make the matching easier)
- Reduce error accumulation (Ground Control Points- Characteristics features or objects that have been placed on the scene and for which the GPS coordinates have been measured and recorded)
-GCP
- Characteristic feature with known, accurate coordinates
- e.g. Survey grade GPS station
- Total station
- Online Map Services
-Image Geotags
- GPS coordinates for each image (EXIF or txt file)
- e.g. Consumer Grade GPS
- RTK GPS Logger


### How many GCPs?
- 3 at least
- 5 - 8 per project recommended
- Well spread out, near features of interest
- Not all of them in straight line
- Adding more and more GCPs
-- Law of Diminishing Return- The increase in accuracy will decrease
-- If more than 10-12, convert them to checkpoint for accuracy assessment


### Methods of getting data
- RTK GPS- 0.02 m accuracy
- Consumer grade GPS- 5-10 m


### Measurements
-Requirements
- Reconstruction is of good quality
- GCP


### Self

- Add GCPs manually - 2D GCP recommended from Google Coordinates
- Add manual tie points for objects of interest and optimize it for the project to take into consideration


### Merging the Projects
- Create two projects to be merged - A , B
- Process step-1 for both the projects
- Add Manual Tie Points in A
- Add the same MTPs in B (with the same name)
- Reoptimize each project

- Create a new project with the option 'Project merged from existing projects'
- Choose to treat same objects with the same name as the same
- Click Finish
- Reoptimize and Generate quality report if needed
- Further process

### Editing the Mosaic
- Under the mosaic editor, you get the option of editing the orthomosaic for regions where the perspective is unclear
- Ortho projection and planar projection
- The map pixels can be assigned colors using the projection
- Draw your region 
- Using the ortho projection, it will use the same algorithm as it was used to generate the orthomosaic in step-3, but use the images that were particularly selected by the user. Hence, improve the output
- In planar, it is going to take a single image's content onto the desired region. Since, it will be a projection from a single image, the perspective is not going to be corrected, thus the distances will not be true. Used mostly for trees or objects of minimum interest
- Band information and color mapping options available
- Draw the region on the mosaic, and add a particular projection (and the images) to improve the mosaic

### Saving the Mosaic
- Changes in Mosaic, affect the local copy and not exported
- To output the modified mosaic, save and export- orthomosaic will be overwritten
- Grid DSM and other formats would be generated if selected


### Sequoia
Multispectral camera from Parrot used for Agricultural projects
To measure the reflectance of different regions of the field
- Modified 
  - Broadband
  - Digital filters
- Multispectral
  - Narrow bands
  - Necessary radiometric data is provided
- The Processing Options Template would be 'Ag Multispectral'

- Outputs
  - Monochrome Imagery
    - Reflectance Maps
    - Index Maps
    - Prescription Maps
  - RGB Imagery
    - Orthomosaic
