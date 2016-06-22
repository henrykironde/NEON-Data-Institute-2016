Welcome to the Etherpad NEON Data Institute 2016 Etherpad!
This is a space where you can share notes and ideas with each other. 

https://public.etherpad-mozilla.org/p/2016-06-20-NEONDI

Institute Website:
http://neon-workwithdata.github.io/neon-data-institute-2016/


TAG #NEONDI16 

## Workshop Presentations

https://figshare.com/articles/NEON_Data_Institute_2016_-_Presentations/3444917





## Load R Package from Github 


# install devtools
# install.packages("devtools")
library(devtools)

# install_github("lwasser/neon-aop-package/neonAOP")
library(neonAOP)



Replace Data - 
We found a few glitches in two of the CHM tiff datasets. These are the fixed versions (and the download data buttons on the website are now updated for these files):
###############################
SOAP Canopy Height Model File:
https://ndownloader.figshare.com/files/5407880
TEAK Canopy Height Model File:
https://ndownloader.figshare.com/files/5408828



Data Issues 
Please use the space below to document issues that you find in our lessons & data.
####################

The link to the lesson code for "Raster 101" appears to be broken:
http://neon-workwithdata.github.io/neon-data-institute-2016/code/i 
This works: http://neon-workwithdata.github.io/neon-data-institute-2016/R/raster-101/
Yes, but the link to download the code on that page is not functioning
It may be because there is no code on the page? I think they are using purl() to pull out just the R code from the md and the script they're using to do that might have had an issue since there aren't any code examples on that particular page.
Here's the raw md file for that particular page: https://raw.githubusercontent.com/NEON-WorkWithData/neon-data-institute-2016/gh-pages/_posts/institute-materials/day1_monday/2016-06-20-raster-101.md
Thanks!
Hi guys - there is no code for that lesson - it's just a markdown page with images. i was going to create a slide show from it but ran out of time. i will fix the code link (remove it) later! Thank you for the feedback! Keep it coming! --Leah
FIXED!!! No more link.  Gold star!

Please indicate the size of the data being deliver so that the end user can obtain the needed resources before delivery.

There was mention of a HDF5 tutorial. Could you direct us to that, please?

http://neondataskills.org/HDF5/ - Thanks!


Here is a link to my wrapper script to run when you upgrade R
https://github.com/butterflyology/updateR


EPSG codes at www.spatialreference.org It's awesome. Super helpful when you don't know the coordinate ref of your data!


Directory for Monday evening/night activity
http://npk.io/TSVJ+

For a Python interface to the OpenTopography data, check out: https://github.com/matt-oak/Summer2016/tree/master/OpenTopo



PRESENTATIONS FROM MONDAY
=========================

https://figshare.com/articles/NEON_Data_Institute_2016_-_Presentations/3444917



Start by putting up objectives/tasks that students will be working though:
1. Import a raster — A lidar canopy height model (lidar/Teak_lidarCHM.tif)
For the CHM, set values == 0 to NA (not trees)
Visualize density and plot vertical cutoff lines.
Classify the raster according to some distribution – low medium and tall trees. This could be done using a histogram potentially or we could just decide that 6m is generally grasses / understory, 10m small trees,and the rest are tall trees. A function could import the desired thresholds. 
Plot the classified raster, add a legend for each “class” - legends are super tricky to simplifying this process with a function would be good.  see: http://neon-workwithdata.github.io/neon-data-institute-2016/R/classify-by-threshold-R/  for my take on forcing a legend outside of the plot area using par settings. You may have other better forms of magic to make this work well. :)
Export the plot figure to a pdf – publishable
Export the classified raster as a geotiff with NaFlagg = -9999 to an outputs folder.

http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002598


## exercises

https://github.com/naupaka/NEONDI-2016-tuesday-exercises

## Some helpful sites on plotting:

http://nicercode.github.io/guides/plotting/
http://gastonsanchez.com/teaching/r-graphical-parameters-cheatsheet.pdf
http://www.statmethods.net/graphs/index.html
    