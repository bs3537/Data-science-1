# Data Science - Spotifier
This is the Data Science portion for an Application that uses Machine Learning to build a Song Recommender based on a audio track analysis.

## 👉 Go to the app [Spotifier](https://spotifier.netlify.com/)

## 👇 Flowchart
![Alt text](data/Flowchart.png)

## 👇 Project Info

- For the Data Science portion of this application, we used this Kaggle [Spotify Audio Features](https://www.kaggle.com/tomigelo/spotify-audio-features) Dataset. Dataset has a number of tracks and for every track an artist. You will also find Spotify's Track Id, along with a number of numeric audio features such as acousticness, danceability, tempo, speechiness and several more. We took this information and utilized a [KDTree](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KDTree.html) from Scikit Learn in order to model our Song Recommender. This method finds the songs nearest to each other in terms of the numerical audio features previously mentioned. From there we have a list of songs, and along with each song is a number of recommended songs(in the example we use 15). We then push it to AWS RDS PostgreSQL database.

## 📹 Presentation
[![Spotifier Presentation Link to YouTube Video](http://img.youtube.com/vi/d3GrBrgw7kQ/0.jpg)](http://www.youtube.com/watch?v=d3GrBrgw7kQ)



## 👇 Backend API Endpoint 

Endpoints that do not say ‘No Auth Required’ or Log In/Register/Log Out will all require authentication    
**Register**   
```
POST - https://spotify-song-suggester.herokuapp.com/createnewuser      
--- parameters ---      
- username      
- password 
```
**Log In**  
```
GET - https://spotify-song-suggester.herokuapp.com/login   
--- takes in ---   
- username   
- password 
```  
**Log Out**   
```
GET - https://spotify-song-suggester.herokuapp.com/oauth/revoke-token   
```
**Get All Tracks (for testing) - No Auth Required**   
```
GET - https://spotify-song-suggester.herokuapp.com/tracks/tracks  
- Limit 10 per page   
```
**Get Track By Name (trackid) - No Auth Required**    
```
GET - https://spotify-song-suggester.herokuapp.com/tracks/track/{name}   
```
**Save/Favorite Track by Name (trackid)**    
```
POST - https://spotify-song-suggester.herokuapp.com/tracks/save/{trackid}   
```
**Get User’s Saved/Favorited Tracks**   
```
GET - https://spotify-song-suggester.herokuapp.com/tracks/savedtracks  
```
**Get Suggested/Recommended Tracks by Name (trackid) - No Auth Required**   
```
GET - https://spotify-song-suggester.herokuapp.com/tracks/recs/{trackid} 
- returns 10 similar songs with song details  
```
**Remove Song From Saved/Favorited**   
```
DELETE - https://spotify-song-suggester.herokuapp.com/tracks/remove/{trackid}   
```   

## 📊 Visual Representationss of What Our ML Model is doing
![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/Screen%20Shot%202019-09-24%20at%207.36.21%20PM.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/Screen%20Shot%202019-09-24%20at%207.36.39%20PM.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/Screen%20Shot%202019-09-24%20at%207.37.05%20PM.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/Screen%20Shot%202019-09-24%20at%207.37.52%20PM.png)

## 👇 Song Selections along with 200 Song Recommendations Based on 
Notice how they generally follow the same trajectory along the path across the features, naturally with a few outliers
This is helping to Visually convey how Songs are recommended based on songs nearest to it in terms of quantifable Audio Features such as accoustiness, danceability, energy etc.
![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/newplot.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/newplot1.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/newplot2.png)


## 👇 Logs

- 2019-09-21 - Started explanatory notebooks
- 2019-09-23 - Re-structured and organized folders, and files

## 📜 Contributing
Pull requests are welcome. However for major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## 👮 License
[MIT](https://choosealicense.com/licenses/mit/)
