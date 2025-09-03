# Drone-Based-Thermal-Analysis-Tool

# About
The `Drone-Based-Thermal-Analysis-Tool` is a collection of Python modules that take photogrammetric projections of thermal images taken by a drone-based system to allow the user to "draw" a temperature path along the path of their choosing. The program is split into two separate aspects:
1. A **Temperature Orthomosaic**: This is currently built with Agisoft Metashape, but current work is being done to transition this into ArcGIS's platform for Photogrammetry. The temperature images are stitched together into a singular TIFF (Tag Image File Format) file. This is used to get the temperature information that was sensed during the flights.
2. A **Digital Elevation Orthomosaic**: Also currently built with Agisoft Metashape. Here, the algorithm takes advantage of a photgrammetric technique of Structure from Motion (SfM). By knowing how different objects move in relation to the observer (the drone), the theory of Motion Parallax can be employed to create the elevation maps. With more triangulation points (i.e., maximizing the number of images taken over a flight), the elevation maps can be improved upon and create an accurate model of the surface of the ground during the flight

Applications of this system are limited to the users imagination. Any drone-based thermal image can be analyzed with our simple tool that inspects a line of analysis. In the case of the development of this program, the application is meant to inspect underground water pipelines to discover leaks that can be 

# Optimization
Since this algorithm relies on photogrammetric Structure from Motion, optimizing the flights for ideal orthomosaic generation is key. This includes maximizing the number of images taken per linear distance flown. In other words, maximizing frontal overlap is key to creating accurate stitches of individual images as well as detailed Digital Elevation Maps. What the team found was especially key to ideal orthomosaic processing, was utilizing a wrapped flight path. Here, maximizing the side overlap as well allows the program to triangulate more points and thus, generate the best...
