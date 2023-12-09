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
The dataset provided information on average ratings of movie genres.

### Data analysis
#### Table 1: bom.movie_gross
Missing values were found in the domestic_gross and foreign_gross columns.
Missing values in the domestic_gross and foreign_gross columns were replaced by their respective median values.
This is because the median value is less sensitive to outliers, unlike the mean. The median also helps maintain the central tendency of the data.
Domestic_gross and foreign_gross columns were added to generate a new column 'box_office'.
The box office is the total earnings from a genre in the domestic and foreign markets.
I replaced genre_ids with their actual genre names using data from 'https://www.themoviedb.org/talk/5daf6eb0ae36680011d7e6ee'.
This was to make interpretation easier: that is knowing which genre got which rating.
The replacement data was as follows:
        MOVIE
        Action          28
        Adventure       12
        Animation       16
        Comedy          35
        Crime           80
        Documentary     99
        Drama           18
        Family          10751
        Fantasy         14
        History         36
        Horror          27
        Music           10402
        Mystery         9648
        Romance         10749
        Science Fiction 878
        TV Movie        10770
        Thriller        53
        War             10752
        Western         37
The box office was then plotted against the genres to give a clear visual of their relationship.
#### Table 2: movie_basics
I checked for missing values in the genres column  and found 5408 counts.
I replaced the missing values with the mode. The mode shows the most repeating genre and therefore was a reasonable replacement.
Next, I fetched top ten genres by grouping them by order of occurrence from highest to lowest.
Then I plotted the genres against their corresponding frequency of occurrence.
#### Table 3: movie_ratings
I previewed data in the movie_ratings table. Then i joined movie_basics and movie_ratings on common column genre_ids.

