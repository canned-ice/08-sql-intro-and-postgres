# 08-sql-intro-and-postgres

**Author**: Candice, Brai, Jason
**Version**: 1.0.0 (increment the patch/fix version number up if you make more commits past your first submission)

## Overview
We are creating a database that the local server that runs off our a machine and allows access by other users.

## Getting Started
 
 Clone https://github.com/canned-ice/08-sql-intro-and-postgres. Install dependencies. Run through the terminal. 

## Architecture

Html, Css, Javascript, handlebars, Jquery, Express, nodemon

## Change Log

08-23-2018 12:45pm - Application now has a fully-functional express server supported by a local postgres, with GET and POST routes for the book resource.

## Credits and Collaborations

https://expressjs.com/

https://github.com/codefellows-seattle-301d37/08-sql-intro-and-postgres
-->

## Routing and Where Things are Going. 

app.delete (/articles)
	-Browser places the request of wanting to  remove/delete the item.
	-That request than goes to the server. 
	-Then the SQL DELETE gets sent to the database to complete the removal.
	-Than the DB sends a complete notice back to the server. 
	-Than the server lets the browser know that the request was completed.

app.delete (/articles:id)

Its pretty much the same process as the .delete. The :id is specifically requesting a certain item from the DB to be removed. 

	-Browser places the request for the item to be deleted.
	-Server receives that request and then completes the SQL request DELETE to the DB. 
	-DB than confirms that the item requested has been removed. 
	-server sends confirmation that the item has been deleted.

app.get(‘/articles’)
 	-The browser is requesting all the articles. It does it by a client query. 
	-The server than takes that request and requests that data from the DB
    -Then the DB returns the data rows that hold all the articles to the sever. Which then the server delivers back the data rows of articles to the browser to see. 

app.get(‘/new-article)
	-The browser sends the request of a new-article to the server 
	-The server than sends a response with a new.html file for the user to fill. 

app.post(‘/articles)
      -The user enters their request within the browser using the post method the data is included in the body of the request to the server. 
      -From the server to the DB, the information that was submitted in the post like making a new article, the information in the body that was passed will be saved.
      -From the DB, it tells the server that they received the data.
      -Than the server sends a message to the browser and lets the user know the data was successfully saved.

app.put 
    -The put method is used when a user request data to be change from the db.
	-The browser sends the request of the change to the server. 
	-Then the server sends the SQL article update to the DB to have it stored. 
	-DB than tells the server that article update has been saved.
	-Server than tells the browser that the change was successful.

	
