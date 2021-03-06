# Movie-Collection

This application create two views that allows you to do a few things with your movie collection. The "add movie" view allows you to add a new movie to your collection. Once you have completed adding a movie it will automatically add this movie into your collection and appear on the screen. If you get rid of a movie there is a feature that will delete that movie. Each movie shows different properties of the movie such as the name, runtime, release date and an image if provided. In the manage genre view you can see your current projects and the total movies within each project. You are able to delete empty projects but not projects that contain at least 1 movie. This is the extent of my project if you have any questions/comments please contact me.

## SQL 

CREATE TABLE movies (
    id SERIAL PRIMARY KEY,
    name varchar(255),
    genre_id INT REFERENCES "movies",
	release_date date,
	runtime time,
	image_path varchar(255)
	
);

CREATE TABLE genre (
    id SERIAL PRIMARY KEY,
    genre varchar(150),
    
);

SELECT * FROM "movies";


SELECT "genre".*,  COUNT("movies") FROM "genre" LEFT JOIN "movies" ON "genre"."id" = "movies"."genre_id" GROUP BY "genre"."id";

## Built with these technologies:
- HTML
- CSS
- JAVASCRIPT
- SQL
- EXPRESS
- ANGULAR JS
- ANGULAR MATERIAL
- NODE.JS

## Install on local host
1. Download project
2. In terminal/command prompt type:
    * npm install
    * npm start
3. Open web browser and type in localhost:5000, press enter

## Screen Shot
![alt text](https://github.com/lvang5/Movie-Collection/blob/master/Screen%20Shot%202018-08-27%20at%2012.53.22%20PM.png)



## Completed features
- [x] Created views Add Movie and manage genre
- [x] Created a controller and router for each view
- [x] In client side added routes to access information in the server: 
    * create(POST)
    * read(GET)
    * delete (DELETE)
- [x] Added pg to communicate database
- [x] Added server side  routes to communicate back with client
    * create(POST)
    * read(GET)
    * delete (DELETE)
- [x] Added CSS styling to HTML
- [x] Added database 


### Next Steps
Features that I would like to add to this project are:
* Adding more CSS features and Angular Material UI
* Add an API
* Better formatting to each view



### Authors
Lais Vang

#### Acknowledgments
* CSS Styling: W3 School


