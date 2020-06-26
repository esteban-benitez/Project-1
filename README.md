# Udacity-Data-Scientist-Project-1
Welcome to my El Nino Data Analysis in Python

Libraries required:

*pandas
*numpy
*matplotlib
*descartes
*geopandas
*shapely.geometry
*scipy

Motivation for the project includes an ongoing interest in utilizing scientific computing in both science, and industry.  El Nino data analysis grabbed my attention because of the recent media on global warming; therefore the possible oceanic changes that might take place.  

Github project consists of the following,

    directory -- data:
    ------------------
         contains the data files captured by the El Nino project, and the shape file utilized to plot the locations of the buoys capturing the data based on the latitude, and longitudinal coordinates.  Also contains the subscript data file tao-all2.dat and tao-all2.missing which notate the missing cells of data in the generalized el nino data set.
    
    jupyter notebook -- Notebook.ipynb:
    -----------------------------------
         The jupyter notebook of python code used in numerical calcualtions.
 
    markdown -- README.md:
    ----------------------
         This markdown holds various information on the github repository.  My basic questions of the initial dataset were threefold,
            1.  Where are the buoys located geographically?
            2.  What were the maximum, and average for each attribute of zonal wind, meridonal wind, humidity, air temperature?
            3.  Is there any statistical linear relationship between the attributes?
            
Resuls of the Analysis indicate as previously stated that there are 59 buoys arranged in 12, pencil like vertical lines along the equator, in the Pacific Ocean.  Buoy 34 had the maximum humidity of 99.4 where the group average was 84.5 degrees, while buoys 19, and 14 contained the maximum wind velocities in the eastern, and western direction, respectively.  A visual note indicates that the three aforementioned buoys are located within North West quadrant of the 2 dimensional world view map.  

Initially, utilizing the python's normaltest(), was modified for the Shapiro normality test on the indexed el nino data frames due to the small population sizes.  Each day range per buoy was analyzed under said Shapiro normality test, per each attribute.  The Latitude, and Longitude attributes were the only attributes with large non parametric consistencies, which could be expected as the data values are the result of scientific placement, not natural phenomena.  While natural in terms of data generation, it is still interesting that all the attributes of zonal winds, meridonal winds, humidity, air temperature, and sub surface temperature buoys were flip floped with large portions of the data was normally distributed.

Based on the normality results analysis, each dataframe series were assigned a statistical correlation coefficient test from the scipy library in python.  For Non Parametric sets the Tau test statistic was compared with the p-value at the .05 level, and each Parametric test was calculated on the pearsonr().  Substituting the associated correlation coefficients with zero, if unable to reject the null hypothesis, the calculations were visulized based on the population mean for each study.  The humidity and air temparture had the strongest relationship, where the negative value indicates just the direction of the linearity.  Humidity seemed to have a secondary effect on sub surface temparture.  The positional data had little effect on humidity, and air temperature had increasing strengths of relationship in a linear sense.
            
Acknowledgements:

I must thank Udacity for giving me the opportunity work with data, and grant the idea's project.  Additioanlly, the UCI Machine Learning Repository must also be commended, as without the interesting data set, I feel I would not have been as driven to succeed.  Also, I would like to thank all the stack overflow boards I viewed during those more challengning coding times.
            
    
    

