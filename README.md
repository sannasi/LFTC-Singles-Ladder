
# LFTC Singles Ladder	
Tennis Club Ladder is web application which allows a tennis club to setup and run an internal singles challenge ladder.
Players can see who is available to play, send and accept challenges to play, record results and see a filtered list of ladder updates.

See the live app [here](https://tennis-club-ladder.herokuapp.com/) (See [**_login_**](#login) below for credentials to use)

Created by:  [Pat Rivet](https://www.linkedin.com/in/pat-rivet/)

## Screenshots:
![Screenshot one](/assets/TennisLadder_Screenshot_1.png)

## Installation

 - Clone this repo ```git clone https://github.com/patrivet/TennisClubLadder.git```
 - ```npm install``` in the client directory.
 - ```npm install``` in the server directory.
 - Create a ```.env``` file in the server directory and populate with the following:-
	 - DB_URL=   your mongo database URL (see Database setup)
	 - PORT=  your server's port number.
	 - HOST=   your server's hostname.
	 - SECRET_KEY= your own chosen secret key (is used to sign access tokens).
	 
 - Create a ```.env``` file in the client directory and populate with the following:-	
 	 - REACT_APP_SERVER_URL=  URL to your server. Note: Defaults to http://localhost:3001 if not set.
	 - REACT_APP_TIMEOUT=  Number of minutes a logged in session will last before being timed out. Note: Defaults to 30 minutes if not set.

### Database setup:
To use TennisClubLadder, an initial import of dummy data is required. 
Run the following command, replacing *<database_dump directory>* 
with the directory /data/DB_files/

```mongorestore -d <database_name> <database_dump_directory>```

e.g. ```mongorestore -d tennis_ladder_db /data/DB_files/```


## Login:<a name="login"></a>
The following credentials can be used to login:-
username: grant.shields@tennis.com
password: ladder123

Login with any other user by following the same format as above - i.e. combine with their first and last names, with a period inbetween, and use the same password   e.g. _firstName.lastName@tennis.com_

## Tech stack:

- [React](https://reactjs.org/)
- [Sass](https://sass-lang.com/)
- [React-router](https://reactrouter.com/)

**Back-end:**
- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/)
- [Mongoose](https://mongoosejs.com/)
- [JWT](https://www.npmjs.com/package/jsonwebtoken)
- [Bcrypt](https://www.npmjs.com/package/bcrypt)
