# data_512_a4
## Final Project Plan

### Introduction
The Seattle public library has 27 branches containing electronic material and printed books. I am curious to see if there are any title checkout trends at the Seattle Public Library. I am curious to see if the Seattle Public Library or specific branches would benefit from an adjustment to their inventory of electronic material and printed materials.

Below are some research questions I hope to answer through my analysis: 
* With the introduction of e-materials and e-readers, is there a trend in electronic material checkouts over printed material checkouts?
*	Is there a correlation between library location and printed material checkout numbers over time?
*	Is there a correlation between “floating” material and checkout counts over time? Floating material is material that can travel between branch locations.
*	Is there a trend in the subject matter being checked out over time? 

To each of the research questions above, I already have assumptions as to the results of the analysis. My assumptions to the research questions are below. 

Each assumption is listed in the order of the questions posed above.
*	I assume that there is an increase trend over time for electronic material checkouts over printed books. There is an increased use of e-readers and an increased demand for electronic copies of books.
*	I assume that the main branch will show to have the most checkouts over time. The main campus has the largest collection of titles, and it makes sense that the main branch would have the largest checkout volumns. (See the bar graph here: https://data.seattle.gov/Community/Items-by-Location/i9et-ud68)
*	I assume that there are more checkouts for “floating” items because they are shared between branches. Floating items can be returned to a different location than it was checked out at. I believe it is also possible to request a title be moved to a specific location when a customer wants to check it out.
*	I have no assumptions on this question, so I am curious to see if I can find any trends. 

### Data Collection
The data I am using is collected and shared by the City of Seattle. The following is a disclaimer that is included in the Data Policy for using the data.

 *"The data made available here has been modified for use from its original source, which is the City of Seattle. Neither the City of Seattle nor the Office of the Chief Technology Officer (OCTO) makes any claims as to the completeness, timeliness, accuracy or content of any data contained in this application; makes any representation of any kind, including, but not limited to, warranty of the accuracy or fitness for a particular use; nor are any such warranties to be implied or inferred with respect to the information or data furnished herein. The data is subject to change as modifications and updates are complete. It is understood that the information contained in the web feed is being used at one's own risk."*
 
The entire data policy can be found here: https://data.seattle.gov/stories/s/Data-Policy/6ukr-wvup/.

I am using three datasets to perform my analysis: **Checkouts by Title**, **Library Collection Inventory** and **Integrated Library Systems (ILS) Data Dictionary**. These datasets are gathered and released by the Seattle Public Library.
#### Checkouts by Title:
This dataset is the monthly count of checkout titles starting in April 2005. This dataset includes printed and electronic versions of titles and their checkout counts aggregated by month. This data is updated monthly and publicly licensed. 

Here is the location to gather the data: https://data.seattle.gov/Community/Checkouts-by-Title/tmmm-ytt6

More information about this data set can be found in the Frequently Asked Questions PDF that can be found on the webpage above. I have provided a link for convince to the PDF here: https://data.seattle.gov/api/views/tmmm-ytt6/files/d37b9edc-c56f-46e4-aaea-cb882230cf3a?download=true&filename=Checkouts%20by%20Title%20FAQs.pdf

This data has 11 columns and 32.3 million rows. The columns are below:
+ UsageClass
+	CheckoutType
+	MaterialType
+	CheckoutYear
+	CheckoutMonth
+	Checkouts
+	Title
+	Creator
+	Subjects
+ Publisher
+ PublicationYear

#### Library Collection Inventory:
This dataset is the library inventory for the entire Seattle Public Library Collection. This data is refreshed monthly starting September 1, 2017 (last updated Nov 6, 2018) and is publicly licensed. Each month appends that month’s inventory, it does not overwrite the previous months inventory.

Here is the location to gather the data: https://data.seattle.gov/Community/Library-Collection-Inventory/6vkj-f5xf

More information about this data set can be found in the Frequently Asked Questions PDF that can be found on the webpage above. I have provided a link for convince to the PDF here: https://data.seattle.gov/api/views/6vkj-f5xf/files/857144b6-5761-4ab4-81be-d36a3287a5cc?download=true&filename=Library%20Collection%20Inventory%20FAQs.pdf

The data has 13 columns and 20.2 million rows. The columns are: 
+	BibNum
+	Title
+	Author
+	ISBN
+	PublicationYear
+	Publisher
+	Subjects
+	ItemType
+	ItemCollection
+	FloatingItem
+	ItemLocation
+	ReportDate
+	ItemCount

#### Integrated Library Systems (ILS) Data Dictionary:
This dataset contains the list of codes used in the Seattle Public Library’s datasets to categorize the titles. This data is updated yearly starting September 1, 2017 (last updated Nov 14, 2018), and is publicly licensed. 

Here is the location to gather the data: https://data.seattle.gov/Community/Integrated-Library-System-ILS-Data-Dictionary/pbt3-ytbc

The data has 7 columns and 571 rows. The columns are: 
+	Code
+	Description
+	Code Type
+	Format Group
+	Format Subgroup 
+	Category Group
+	Category Subgroup
### Limitations
One of the major concerns/limitations to this analysis is the assumption of universal access to the library and its resources.
This data assumes that everyone has access to the library locations or its electronic material, however that is not necessarily true. 
Below are the requirements to get a free library card and can be found on the Seattle Public Library website. 

**Everyone who lives, works, goes to school or owns property in King County (except Yarrow Point and Hunts Point) can get a free Library card. Apply online, then visit any Library location to pick up your card.**

The quote above can be found on the Seattle Public Library's website as well as other requriments to obtain a library card. The link for this can be found here: https://www.spl.org/using-the-library/get-started/get-started-with-a-library-card.

You must also show a valid photo ID and something that proves you meet the above requirements. This is broad list of people eligible to receive a free library card, however if you do not meet these requirements, there is a fee to get a library card. This means there is a portion of people who might not be able to get a library card due to the financial burden of not being able to prove they meet the requirements laid out by the Seattle Public Library.

Another limitation to the data collected is the availability of transportation to a physical location. If a person wants to check out a specific title that is only at a specific location, the ability to travel to that branch might not be available. Convenient public transportation, limitations in parking locations, and ability go during the hours of operations can be challenging for some and can skew the data that the library collects. 

Another limitation to the data collected is access to printed materials and electronic material can be limited. For the printed material, the number of printed copies might hinder your ability to check out the title. In the case of electronic material, access to an e-reader, computer or reliable internet connection can hinder some from checking out electronic material (i.e.  e-readers, computers and reliable internet connection require the ability to pay for these objects and services).
### Data Analysis Method
I plan on using Python to perform my analysis and create visualization to help communicate my findings. 
### Human Centered Design Concepts
The data collected is on book checkout patterns by humans, and therefore human centered. Another human centered design concept is that the results of this could be used to change the availability of certain resources to the public. The affects of this analysis have the potential to change the inventory of titles available electronically or in printed formats to the various branch locations. This could result in increased or decreases to access to certain material.
