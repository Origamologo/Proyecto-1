# Analysis of Civitatis' marketing strategy
![portada](https://culturainquieta.com/images/Luis_Art%C3%ADculos/GunsReplacedWithSelfieSticks_humor_cine_Tumblr_SelfieStick_CulturaPop_memes_culturainquieta/GunsReplacedWithSelfieSticks_16_humor_cine_Tumblr_SelfieStick_CulturaPop_memes.jpg)

# Description
Civitatis is an OTA (Online Tour Agency) focused on spanish speakers tourists, that was founded in 2008. In 2016 they opened their first phisical shop in the centre of Madrid, but their business is mainly based on the internet. They have pursued several marketing campaings including tv and radio advertisements, but the key of their success is that they've managed to settle their brand operating apart from the main rating platforms in tourism business like tripadvisor or yelp.

- **The key of success**<br/>
When you book an activity through an OTA, you'll always know who the local provider is and the OTA will crearly be the intermediary. On the other hand, through civitatis you'll never know with whom you'll be doing the activity as this is not shown in the booking process; you'll finish with a voucher in which their brand name will be the most visible item (if not the only one), no matter if you will be doing the activity with mr so-and-so.<br/>
And as it has been said before, they are not present in any of the tourism rating platforms, so any issues will be directly reported to them: they are their own rating platform. In this way they can check the quality of the local providers with whom they colaborate, substitute them with their own brand and they don't have to compete with other companies in the 'review arena'. 

- **The challenge**<br/>
The company has had a consistent growth untill the covid-19 crisis which forced the whole tourism industry to stop and restart from zero. In the post-covid casecenario, with the travels to and from foreing countries highly restricted, the brand presence among locals has been crucial for recovery.

# Objetive
The objective of this project is to measure the effectiveness of civitatis' marketing strategy. To do so we will focus on Barcelona, one of the most competitive cities in the tourism industry, and we'll analize the performance of the most popular activity in civitatis' web page, the so called 'free tour', before and after the lockdown. We will compare this information with the public data on tourism provided by the spanish goverment to check how it has been the performance of the company in comparison with the general evolution of the sector.<br/> We'll also try to automate all the processes as much as posible, so the data will update and clean every time we run the code without further intervention.

**Free tour? What?? Why???**<br/>
A 'free tour' is a tour in which the tourist has to pay nothing to join the activity, although he can tip the guide at the end of it. On the other hand, the local guide must pay a fixed amount of money for each client that joins the tour to the OTA that provides the tourists. Taking on account that the risk for the companies is nearly zero, it's easy to figure out why this model, created by Chris Sandemans in 2003, is nowadays followed by tons of companies (just type 'free tour' on google and enjoy) and has become one of the main battle fields for walking tours companies.<br/>
To check if the tourist who booked the activity actually showed up so they can charge the guide (remember that it's free and you might feel in the mood for a beer in stead of walking when the tour begins), civitatis ask the client for a review. This is a very easy step for the client and he doesn't have to share any information if he doesn't want to, it works as a check in. If a tourist that was not reported by the local guide sends a review, the company will know that the guide is cheating... But for what matters to us, this means that the reviews in civitatis are a trustful source of information regarding how many people joins the tours they promote.

# Working plan 
To achieve the objetive, the information from the reviews of civitatis' free tour in Barcelona will be compared with the tourism data provided by the spanish government. We will follow this steps:
  1. **Get and clean the goverment data:** We will work with the csv 2078 downloaded from https://datos.gob.es It must be cleaned and enriched with some extra information. We'll have to extract the data for the tourist area we want to analize and organized it to get the variables that we will be using, mainly the number of tourist organized by date and separated by their origin.
  2. **Get and clean the civitatis reviews:** The reviews will be scraped from https://www.civitatis.com/es/barcelona/free-tour-barcelona/opiniones This information must be cleaned and organized to get the relevant data that we need for this study which, as for the goverment data, will mainly be the number of tourist organized by date and separated by their origin.
  3. **Generate data frames for visualization:** Once we had cleaned the data, we will select what we need to perform our study.
  4. **Compare the data and drop conclusions:** Finally, we will visualize the obtained data through graphics that will help us to understand how has been the evolution of tourism in general and the performance of civitatis in particular before and after the covid-19 crisis.

### Structure of the project files
​
The structure of this project is composed of:<br/>
  a. A folder of notebooks:<br/>
    **1_limpieza.ipynb:** contains the study and cleaning of the data given by the spanish goverment.<br/>
    **2_scraping.ipynb:** performs the scraping of the reviews of the civitatis' freetour in barcelona.<br/>
    **3_limpieza_scraping.ipynb:** contains the study and cleaning of the data obtained in the scraping.<br/>
    **4_dataframes.ipynb:** using the cleaned data, generates the data frames with just the needed information for the study.<br/>
    **5_visualization.ipynb:** graphs and conclusions of the study.<br/>
    
  b. src folder:<br/>
    **limpieza.py:** contains all the functions used in the cleaning and generation of data<br/>
    **scraping.py:** contains the function used in the scraping<br/>
    
  c. data folder: contains both the data used and generated for the study