## Table of Contents
1. [albums_by_band.R](#one)
2. [albums_by_year.R](#two)
3. [compare_bands.R](#three)
4. [number_one_albums.R](#four)
5. [vinyl.R](#five)

<hr>
<a id="one"></a>

# [albums_by_band.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/albums_by_band.R)
- ## Filter albums by band/artist.
### Description
Filter albums by band/artist.
### Usage
```albums_by_bands(band.var)```
### Arguments
| ```band.var``` | A String specifying the name of the band/artist. |
|---------:|------------|
### Value
Returns a data frame with columns: Album, Year, and Rating, filtered by the specified band/artist.
### Examples
```albums_by_bands(“10,000 Maniacs”)```<br>
```albums_by_bands(“beabadoobee”)```

- ## Calculate and display average album rating for a band/artist.
### Description
Calculate and display average album rating for a band/artist.
### Usage
```band_mean_rating(band.var)```
### Arguments
| ```band.var``` | A String specifying the name of the band/artist. |
|---------:|------------|
### Value
Prints the average rating of the specified band/artist as a formatted String.
### Examples
```band_mean_rating(“10,000 Maniacs”)``` <br>
```band_mean_rating(“beabadoobee”)```

- ## Count and display the number of ranked albums for a band/artist.
### Description
Count and display the number of ranked albums for a band/artist.
### Usage
```band_album_count(band.var)```
### Arguments
| ```band.var``` | A String specifying the name of the band/artist. |
|---------:|------------|
### Value
Prints the number of ranked albums of the specified band/artist as a formatted String.
### Examples
```band_album_count(“10,000 Maniacs”)``` <br>
```band_album_count(“beabadoobee”)```

<hr>
<a id="two"></a>

## [albums_by_year.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/albums_by_year.R)
- ## List the top albums for a specific year in ascending ranking order.
### Description
List the top albums for a specific year in ascending ranking order.
### Usage
```year_albums(year.var)```
### Arguments
| ```year.var``` | An integer specifying the year to filter by. |
|---------:|------------|
### Value
Returns a data frame with columns: Ranking, Album, and Artist, ordered by ascending Ranking.
### Examples
```year_albums(2024)``` <br>
```year_albums(1993)```

<hr>
<a id="three"></a>

## [compare_bands.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/compare_bands.R)
- ## Compare album ratings between two bands/artists over time.
### Description
Compare album ratings between two bands/artists over time. Each artist’s ratings are plotted using distinct colors (red and blue), with album release years on the x-axis and ratings on the y-axis.
### Usage
```band_album_comparison_chart(var.artist1, var.artist2)```
### Arguments
| ```var.artist1``` | A String specifying the name of the first band/artist (plotted in red). |
|:---------|------------|
| ```var.artist2``` | A String specifying the name of the second band/artist (plotted in blue). |
### Value
Returns a ggplot object representing the album ratings over time for both artists.
### Examples
```band_album_comparison_chart(“10,000 Maniacs”, “beabadoobee”)``` <br>
```band_album_comparison_chart(“Bon Iver”, “Japanese Breakfast”)```

<hr>
<a id="four"></a>

## [number_one_albums.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/number_one_albums.R)
- ## List the number one album for each year in a given range.
### Description
Filters the album dataset to return the top-ranked album (```Ranking == 1```) for each year between the specified start and end years, inclusive.
### Usage
```number_one_album(var.startyear, var.endyear)```
### Arguments
| ```var.startyear``` | An integer specifying the start year of the range. |
|:---------|------------|
| ```var.endyear``` | An integer specifying the end year of the range. |
### Value
Returns a data frame with columns: Year, Album, and Artist for the top-ranked album in each year.
### Examples
```number_one_album(1993, 2001)``` <br>
```number_one_album(2004, 2012)```

<hr>
<a id="five"></a>

## [vinyl.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/vinyl.R)
- ## Find top-rated albums not owned on vinyl.
### Description
Identifies albums with a rating of 9 or higher that are not currently owned on vinyl, sorted in descending order of rating.
### Usage
```missing_vinyl()```
### Value
Returns a data frame with columns: Album, Artist, and Rating for albums missing from the vinyl collection, sorted by Rating in describing order.

- ## Find years with the most vinyl records owned.
### Description
Analyzes the dataset to count how many vinyl records are owned for each year. The result is a list of years sorted by vinyl count in descending order (excluding years with no vinyl albums).
### Usage
```year_most_vinyl()```
### Value
Returns a data frame with columns: Year and n (number of vinyl records owned for that year), sorted by n in descending order.
