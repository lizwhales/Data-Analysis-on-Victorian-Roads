# COMP20008-Project2
Project 2 for COMP20008 - Element Of Data Processing  


Investigating how population growth is impacting Victorian Roads. Analysis areas include: Traffic Signal Volume Data and Population Growth,  
Motor Vehicle Registration vs. Population and  Growth Rate Comparisons and Correlations. 


Collaborative work of:  
Harold Fangyuan Liu - 1166132  
Andy Ng -  1170648  
Desmond Wong - 1166527  
Elizabeth Wong - 1082634   


<mark>DO NOT ATTEMPT TO RUN THE CODE WITHOUT DOWNLOADING ALL FILES</mark>  

Code Running Description for Traffic Volume Data (in the folder General_Population_Traffic_Volume):  
Dataset link: https://discover.data.vic.gov.au/dataset/traffic-signal-volume-data  
Due to the large sizes of the csv files (over 1 GB), each year from 2014 to 2020 must be downloaded. Within these VSDATA_ zip files which are named by year,  
e.g: VSDATA_2014, there are more zips which all need to be extracted manually until there are no zip files. In some years there are inconsitencies within these folders,  
where they have more zip folders inside, please unzip these and extract them out; removing all the folders. The result should be VSDATA_ folders from 2014 to 2020 with nothing   
but their year's csv's inside, which are ordered by date. Please place these VSDATA folders in the folder "General_Population_Traffic_Volume".  
Note: If there are extra folders inside VSDATA the code will not run.  

Order of Running Code:
1. Please run the "Create_Necessary_Files.ipynb" first to create the necessary files.  
2. Then run you can move on "Random_90day_Sampler.ipynb", where the code needs to be run once for every single year of VSDATA_. This can be done by manually changing the "year"  variable. This was done like this due to a worry about memory usage issue and crashing a computer. Everytime "Random_90day_Sampler.ipynb" is run for a new year, a new folder  
"chosen_" should be created for that year, inside this will be the randomly sampled 90 days / files. If a singular year is run more than once there will be an additional 90  
files for each time it is run. For each year's data, it will be concatenated into a singular csv "_final.csv" and stored in the folder "Sampled_Data_Per_Year".  
3. After running "Random_90day_Sampler.ipynb" for all the years 2014-2020, run "TotalandPeak_Volume_PerYear.ipynb" for each year, this can be done by changing the "year" variable  this will take the data from "Sampled_Data_Per_Year" and filter it into a new csv "_filtered.csv" for each year. This will be saved in the folder "filtered_data"  
4. After this is run for all the years 2014-2020, the final code can be run, "TotalandPeak_Volume_OverYears.ipynb". This will take all the filtered data that was just created  
and once again merge them all into one csv, one ontop of the other. This final csv file will be called "traffic_all_years.csv". This code file will also create the relevant  
diagrams "Daily_volume.png", "Morning_Peak_Hour.png", "Evening_Peak_Hour.png".

Code Running Description for Correlation_Growth (1).ipynb (in folder Growth_By_LGA):
Dataset link: https://www.abs.gov.au/statistics/people/population/national-state-and-territory-population/

Due to making wrangling easier, download Victorian_Population.csv which is the sliced csv from the original XML file that was then converted to csv.
The original dataset was also renamed to Victorian_Population to enable more meaningful naming conventions.

Dataset link: https://postcode.auspost.com.au/product_display.html?id=1

Please download Australian_Postcodes.csv as it is no longer avaliable for free to the public. At the time of downloading the csv, it was free, however it is no longer free.

Dataset link: https://discover.data.vic.gov.au/dataset/traffic-volume

Please download the Traffic_Growth.csv dataset. It is the same dataset as the link above but it has just been renamed and used as Traffic_Growth.csv within the Correlation_Growth (1).ipynb file. Thank you ^^

