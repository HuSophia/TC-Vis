# TC-Vis: A Data Visualization Tool for Exploring Hurricane Lifecycles

**TCVis** is a user-friendly tool designed for visualizing tropical cyclone tracks using data from the International Best Track Archive (IBTrACS). 
By allowing users to input the storm's name and year, the software generates detailed plots that illustrate the storm's path along with its wind radii in four quadrants. 
Utilizing libraries such as Cartopy for map projections and Matplotlib for graphical rendering, TCVis produces clear and informative visualizations that show the storm's 
trajectory, wind intensity, and pressure variations over time. This algorithm is currently used by NOAA scientists to gain insights on severity of tropical cyclones and for reporting purposes. The resulting plots are saved as a PNG file, serving as a valuable resource for researchers and meterologists, and anyone interested in the dynamics of tropical cyclones. 

## Main Functions
- **`'LonTo360(dlon)'`** : Converts longitudes from -180 to 180 degrees to 0 to 360 degrees.
-  **`'get_by_name(name, year, ibtrack_file)'`** : Retrieves and processes the storm data for the specified name and year.
-  **`'draw_quadrants_arcs(xcenter, ycenter, radii, lw=2, ec='crimson', ax=None)'`**: Draws wind radii arcs around the storm center. 
-  **`'draw_quadrants_wedges(xcenter, ycenter, radii, lw=2, ec='crimson', fc='lime')`**, alpha=1, ax=None)` : Draws wind radii wedges around the storm center.

## Notes 
- The script assumes the IBTrACS CSV file has a specific format. Make sure the file matches the expected format. 
- The visualization is created using the PlateCarree projection with coastlines and national borders added.





