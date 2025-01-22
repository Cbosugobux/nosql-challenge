# nosql-challenge

Module 12 - NoSQL Challenge

In this assignment, students were asked to use a database of UK food establishments and pyMongo to analyze a collection of documents in mongoDB.

The first step in doing this was to set up the database and the Jupyter Notebook.  In order to do this, we used a .JSON file provided to us.  Using pyMongo, students were asked to load the JSON file into mongoDB using the import feature in Mongo DB. To do this, students has to first create a database in Mongo called 'UK_Food'.  Next, create an 'establishment' collection. Following this, students assigned a variable to the collection of documents in the UK_Foods database.

Students were then asked to update the database with a new restuarant called 'Penang Flavours'. This JSON as given was missing some information.  Students had to update the information in the document and then add the updated document to the etablishments collection.

Once the database was complete, students were asked to do analysis of the database and its collection of documents. 
These questions were (answer follows each question):

1. Which Establishments have a Hygiene Score equal to 20?

In order to find these establisments, students had to query the database and, using count_documents, find the number of documents first.  There are 20 total establishments with a score equal to 20.  Next, students had to fetch all the documents matching the query and print out  the first establishment on the list.

3. Which establishments in London have a Rating Value greater than four?
In order to create and run this query, students had to use regular expression formatted code in order to find this information.  This is because the London Authority has a longer name than just 'London'. There are 33 establisments in London with a rating value greater than four.

4. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
  
For this question, students had to search within .01 degrees or 1.11 km (+/-) of Penang Flavours location.  In order to do this, first, students had to set parameters for the search by assigning the key assigning the latitude and longitude values to variables called latitude and longitude.  Next set up the calculations to find the boundarys of the search.  After the boundaries were set up, use a query to find documents in the database which met the parameters and had a Rating Value of 5.  These results were sorted by hygiene and all five have Hygiene scores of zero.

5. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

In order to find how many had scores of 0, students had to again query the databas, but this time, use a pipeline to find the answer to the query.  Using a match query, group query, and a sort query, Students then set up an pipe line that aggreagates the parameters and retuns the result.

Lastly, students had to create a Pandas dataframe using the results data and displace the number of rows and the first ten rows.


