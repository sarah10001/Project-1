[jupyter notebook file](https://github.com/sarah10001/Project-1/blob/main/Project-1.ipynb)
# MOVIE INDUSTRY EXPLORATION

Venturing into movie production can be a lucrative and glamorous business, and yet a highly risky endeavor.
It is therefore important to choose moves into the movie industry wisely and with precaution.
The movie genres range from drama, comedy, action, adventure, horror, sci-fi, and many more. 
Sometimes there is a thin line between movies that we are unable to distinguish one genre from the other. 
In such instances, we find that we can have romance/comedy or comedy/drama, or even action/comedy. 

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

## Data analysis
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
Since the genre_ids were comma-separated, I replaced each id on its own instead of as a group.
The box office was then plotted against the genres to give a clear visual of their relationship.
#### Table 2: movie_basics
I checked for missing values in the genres column  and found 5408 counts.
I replaced the missing values with the mode. The mode shows the most repeating genre and therefore was a reasonable replacement.
Next, I fetched the top ten genres by grouping them by order of occurrence from highest to lowest.
Then I plotted the genres against their corresponding frequency of occurrence.
#### Table 3: movie_ratings
I previewed data in the movie rating table. I then selected the genre and weighted_average_rating columns. 
I calculated weighted_average_rating as (SUM(averagerating * movie_count) / SUM(movie_count)).
Then I joined movie_basics and movie_ratings based on the common column 'movie_id'.
This was important in making available the genres column, which was then plotted against the weighted_average_rating column.

## Visualization
#### Table 1: bom.movie_gross

![image](https://github.com/sarah10001/Project-1/assets/151674519/4c43eefe-da96-462c-bb03-b5c74c82bc73)

#### Table 2: movie_basics
![image](https://github.com/sarah10001/Project-1/assets/151674519/17474dc2-e721-4070-b401-51df58e45807)

#### Table 3: movie_ratings
![image](https://github.com/sarah10001/Project-1/assets/151674519/5c6ec9b1-a61a-42d9-8eb6-a9229def3da9)


# Conclusions
Results from table 1 show the top 5 genre grouping in box_office as:
  1. Action, adventure, sci-fi
  2. comedy
  3. drama
  4. action, adventure, fantasy
  5. action, adventure, fantasy, sci-fi.

The graph from table 2 shows the leading genres in terms of frequency are:
  1. documentary
  2. drama
  3. comedy
  4. horror
  5. comedy, drama

The graph generated from table 3 shows leading genres by rating are:
  1. Comedy, documentary, fantasy
  2. documentary, family, musical
  3. history, sport
  4. game-show
  5. music, mystery

Looking at all the results from the three graphs, I deduced three genres that are doing very well.
Comedy appeared in all the graphs making it the best genre in terms of rating, frequency,
and box office followed by the drama genre.
Documentary appeared to be a safe choice owing to having the highest frequency.
Action, adventure, sci-fi had the highest returns owing to being the lead in the box office.

Findings:
  1. Comedy and drama are the safest genres to invest in since they appear at the top in the three graphs
  2. Action adventure sci-fi has the highest returns 
  3. Documentary has the highest rating

## Summary
Comedy, drama, action, adventure, and documentary are the best genres to invest in.

