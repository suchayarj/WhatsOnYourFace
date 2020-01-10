# WhatsOnYourFace

**Presentation Link: https://docs.google.com/presentation/d/1WirouORE1BTJmqjE8Qd94nHhls4L0t5KmRRavSkZqW8/edit#slide=id.p **

## Motivation
As a data scientist who loves cosmetics, I would like to utilize my skills in finding out harmful chemicals in cosmetic products sold in California. I would like to further explore if one chemical is more harmful than the other and if there are any brands or companies that have higher chance of using very harmful chemicals ingredients more than others


## Data
The Chemicals in Costmetics dataset reflect information that has been reported from 2009-2019 to California Safe Cosmetics Program. It includes more than 100,000 inputs of cosmetics containing ingredients linked to cancer or reproductive harm reported.


The table consists of 20 columns but interested in examining the following columns:
- CDPHId (Product ID)
- ProductName
- CSF (Color/Scent/Flavor)
-

**Please note that each product can be input multiple times if it has more than one scent/flavor/color or more than one chemicals

## Workflow and EDA
- Import data to pandas data frame and clean
- First observation
    - total of 34908 reported products
    - total of 584 reported companies

- Determine the most reported chemical
![picture](img/chembypercent.png)
Titanium dioxide comes up really high. 

- Find out the most reported primary categories. To answer this, I grouped the data by the product id and primary category and plot the bar graph. 

![picture](img/catcount.png)

- Most reported chemical by primary categories

![picture](img/chembycat.png)
Yellow block refers to Titanium Dioxide. This evidently shows that Titanium Dioxide has been reported the most across all primary categories. However, this triggers a question if Titanium Dioxide is actually very harmful or not.

After some research on this chemical, I discovered that Titanium Dioxide is actually FDA approved. Although it is considered harmful, but there are other chemicals that are much more compared to it.  

-  Next step I did was to categorize chemicals into VERY HARMFUL or not according to World Health Organization's list of 10 chemicals of major concerns even with low amount of exposure. I combined this list with Dirty Dozen ingredients investigated in Suzuki Foundation

![picture](img/harmfulcomp.png)

- Calculating ratio very harmful product to total products reported for each company

![picture](img/ratiohist.png)
## Hypothesis Testing

