# Team members:
 Kevin Clark, Rebekah Rowland, Amy Dach, Poonam Goel
# Group repository on GitHub : 
    https://github.com/poogoel/Final_Project.git
# Description of data source - 
    NFL Football stats located in the ESPN website.
# Expected data cleaning steps to make the data useful for machine learning:
    Formatting into readable CSV files 
# The machine learning models we plan on using:
    Custom Regression Model.
# The metrics we plan on using to evaluate the ml model: 
    Team Offensive statistics
# We plan on demonstrating our model (web app, jupyter notebook) :
    Web App.
# We plan on training the model (colab, personal computer, aws, Databricks)
    AWS.

ETL: NCAA College Football Statistics Amy Dach, Kevin Clark, Poonam Goel, Rebekah Rowland

Original Project Proposal: ● Data sources: ​We chose to scrape ESPN.com for both full team data and individual player statistics. ● What Transformations: ​Loading website HTML into Jupyter notebooks to be converted into pandas dataframes. Then, converting the data into a JSON and uploading into MongoDB for use as an API later down the road ● Where is data going to loaded: ​Jupyter notebooks, then to MongoDB

Extract: ● We decided to use BeautifulSoup to scrape the URLs that were set up in HTML to get the passing, receiving, and rushing stats for all 130 NCAA teams. ○ Full Team URL: ​https://www.espn.com/college-football/teams ○ Individual Team URLS: 130 Teams Example​:​https://www.espn.com/college-football/team/stats/_/id/2229/florid a-international-panthers

Transform: ● The HTML string itself was set up pretty clearly and fairly easy to parse. Using a for loop, we were able to import the individual team URLs into a Pandas Dataframe. From there, we were able to clean up the multiple statistical tables into three clean dataframes: passing, rushing, and receiving. We then imported those data frames into a dictionary, converting the dataframes into JSON strings that were ready to be uploaded.

Load: We chose to load our information into MongoDB because we wanted to avoid creating schemas and we had uniform tables which made it easy to upload without having to worry about primary keys.

Final MongoDB: The final collection has the passing, rushing, and receiving statistics saved as JSON strings for 130 NCAA teams.