# Pix4D
Creating a 3D Model and Map of University of Maryland using Pix4D

### What can be done with Pix4D?
- Point Cloud
- 3D Mesh
- Orthomosaic

How Pix4D Works-
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

### Pix4D Outputs [name](url)

***
### Pix4D Mapper Desktop Interface

#### Getting Started
- Select as many images as you want for the project
- The Coordinate System would be automatically selected. Most of the time, it would be WGS 1984. It can also be edited as per our requirement.
- If the images are taken from a drone or a GPS enabled camera, the Geolocation and Orientation will be available under the Image Properties.
- The software will load the Camera Model automatically from the images as long as that particular model is in the database. If not, the information would be read from EXIF.
- The output coordinate system would also be automatically selected to WGS84. However, we can also modify it to our known coordinate system.
- The Processing Options Template gives us different templates to work on depending upon the type of images captured- aerial, terrestrial or agricultural. 
- In the Map View, the images will be positioned correctly on the map according to their geolocation.
- The Processing Options would now be available and one or more can be selected to start with.

### Georeferencing
//- Allows us to place the project on the earth. Can tell us where exactly was our project.
//- It can provide scale and orientation
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


#### How many GCPs?
- 3 at least
- 5 - 8 per project recommended
- Well spread out, near features of interest
- Not all of them in straight line
- Adding more and more GCPs
-- Law of Diminishing Return- The increase in accuracy will decrease
-- If more than 10-12, convert them to checkpoint for accuracy assessment


#### Methods of getting data
- RTK GPS- 0.02 m accuracy
- Consumer grade GPS- 5-10 m

#### Adding GCPs in Project
-


#### Measurements
-Requirements
- Reconstruction is of good quality
- GCP
