# nosql-challenge

Module 12 challenge

This challenge is about a contract by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. Their provided data is what has been provided for analysis.

First, the data was imported using mongoDB import : 'mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json'. The database contained the collection "establishments".

The database was then updated with jupyter notebook " NoSQL_setup_starter.ipynb" by:

1. Adding a  new document with the following information:
  {
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
}

2. Checking the BusinessTypeID for the "Restaurant/Cafe/Canteen" business type and updating for the new restaurant added.

3. changing the data type for the RatingValue from string to integer and to Double for the longitude and latitude.


The analysis part was done in jupyter notebook "NoSQL_analysis_starter.ipynb".
4 questions were answered:

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a RatingValue greater than or equal to 4?

3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

4. How many establishments in each Local Authority area have a hygiene score of 0, Sorted from highest to lowest, and the top ten local authority areas displayed.
