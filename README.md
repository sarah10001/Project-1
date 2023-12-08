# MOVIE INDUSTRY EXPLORATION

Venturing into movie production can be a lucrative and glamorous business, and yet a highly risky endevor.
It is therefore important to choose moves into the movie industry wisely and with precaution.
The movie genres range from drama, comedy, action, adventure, horror, sciFi, and many more. 
Sometimes there is a thin line between movies that we are unable to distinguish one genre from the other. 
In such instances, we find that we can have romance/comedy or comedy/drama or even action/comedy. 

## BUSINESS UNDERSTANDING
Client: Microsoft
### Objectives
1. To find out which movie genres rank highest in the box office
2. To identify movie genres that rank highest in movie ratings
3. To find out the most popular movie genres

## Data understanding 
### Data source
The data used in this project has been derived from movie sites:
  1. Box Office
  2. IMDBLinks
  3. Rotten Tomatoes
  4. TheMovieDB
  5. The Numbers
     
This project focuses on specific columns (genre_ids, box_office, rating) contained in the following datasets:
  1. bom.movie_gross.csv
  2. movie_basics
  3. movie_ratings
  4. tmdb.movies.csv

### Data description
#### Table 1: bom.movie_gross
This dataset provided information on box office which is the sum of domestic_gross and foreign_gross. 
In other words, the box office is the total earnings from the movie genres in the country of production and outside its borders.
#### Table 2: movie_basics
The dataset provided information on movie genres
#### Table 3: movie_ratings
The dataset provided information on average rating.

### Data analysis
#### Table 1: bom.movie_gross
Missing values in the domestic_gross and foreign_gross columns were replaced by their respective median values.
This is because the median value is less sensitive to outliers unlike the mean. The median also helps maintain central tendency of the data.
