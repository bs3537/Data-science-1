# Data Science - Spotifier
This is the Data Science portion for an Application that uses Machine Learning to build a Song Recommender based on a audio track analysis.

## Go to the app :point_right: [Spotifier](https://spotifier.netlify.com/)

## Flowchart
![Alt text](data/Flowchart.png)

## Project Info

- For the Data Science portion of this application, we used this Kaggle [Spotify Audio Features](https://www.kaggle.com/tomigelo/spotify-audio-features) Dataset. Dataset has a number of tracks and for every track an artist. You will also find Spotify's Track Id, along with a number of numeric audio features such as acousticness, danceability, tempo, speechiness and several more. We took this information and utilized a [KDTree](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KDTree.html) from Scikit Learn in order to model our Song Recommender. This method finds the songs nearest to each other in terms of the numerical audio features previously mentioned. From there we have a list of songs, and along with each song is a number of recommended songs(in the example we use 15). We then push it to AWS RDS PostgreSQL database.

## Presentation
<a href="http://www.youtube.com/watch?feature=player_embedded&v=d3GrBrgw7kQ
" target="_blank"><img src="http://img.youtube.com/vi/d3GrBrgw7kQ/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>

## Backend API Endpoint 




## Visual Representationss of What Our ML Model is doing
![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/Screen%20Shot%202019-09-24%20at%207.36.21%20PM.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/Screen%20Shot%202019-09-24%20at%207.36.39%20PM.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/Screen%20Shot%202019-09-24%20at%207.37.05%20PM.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/Screen%20Shot%202019-09-24%20at%207.37.52%20PM.png)

## Song Selections along with 200 Song Recommendations Based on 
Notice how they generally follow the same trajectory along the path across the features, naturally with a few outliers
This is helping to Visually convey how Songs are recommended based on songs nearest to it in terms of quantifable Audio Features such as accoustiness, danceability, energy etc.
![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/newplot.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/newplot1.png)

![Alt text](https://github.com/Build-Week-Spotify-Song-Suggester/Data-science/blob/master/data/newplot2.png)


## Logs

- 2019-09-21 - Started explanatory notebooks
- 2019-09-23 - Re-structured and organized folders, and files

## Contributing
Pull requests are welcome. However for major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
