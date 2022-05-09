# TC-Vis


An automation of the visualization of a tropical cyclone path for NOAA scientists in real-time as data is collected by satellites.

# Background
One way that researchers and scientists learn about hurricanes is to study their tracks using data from various weather agencies. The tracks of hurricanes can bring to light several insights by examining the life cycle of the hurricane, including the direction and speed of the hurricane, the evolution of the hurricane’s intensity, and any landfall locations. Together, these insights enable scientists and emergency managers to prepare for future hurricanes by detailing the paths of past hurricanes.


Unfortunately, there are not many open source software that can easily provide scientists and emergency managers. One current package in Python called Tropycal (https://tropycal.github.io/tropycal/index.html) provides a way to simplify the process of retrieving and analyzing tropical cyclone data (Fig. 1). This tool allows for quick visualization of a given tropical cyclone using data obtained from various datasets such as HURDAT, IBTrACS reanalysis, and National Hurricane Center Best Track data. 

While this tool provides many benefits, it lacks the ability to show additional information that may be useful. For example, it would be useful to know the date of each dot during the lifetime of the storm to better understand the context of when the tropical cyclone is moving. In addition, it would be useful to know the maximum sustained wind speed and minimum sea level pressure (SLP) of the tropical cyclone at any given point. This information is readily available from many weather agencies, and by including these into a visual would provide a comprehensive graphic that could be useful to various key stakeholders.

# Method
The goal of this project is to create software that produces a comprehensive visual of the lifecycle of a hurricane using two user input arguments: the name and year of a tropical cyclone. To this end, I wrote a set of functions and commands in Python to pull data from IBTrACS and produce a visual that can be automated for various tropical cyclones. 

The Python code leveraged several state-of-the-art libraries including Cartopy, Matplotlib, Numpy, Xarray, and Pandas to read the data and produce the data visualizations. I began by taking the user input arguments and subsetting the IBTrACS data for the specific tropical cyclone. Thereafter, I placed this data into a Pandas DataFrame to then plot using Cartopy and Matplotlib on a geospatial map. The annotations used the IBTrACS information to dynamically detail the life cycle of the tropical cyclone. The end result is a visualization of the tropical cyclone’s path and its physical characteristics. 

