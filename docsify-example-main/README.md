# <a id="home-page"></a>Introduction to MyFavoriteAlbums

## What is MyFavoriteAlbums?

MyFavoriteAlbums is an open-source music data analysis tool built in R that allows you to upload a CSV file containing your favorite albums and automatically generates an [interactive web dashboard](https://cholstro.shinyapps.io/shiny-music/) based on that data. The application utilizes a user-friendly interface with built-in visualizations and customizable filters for exploring musical preference trends over the years. MyFavoriteAlbums puts you in control, with fully written code that you can reference or adapt to create your own custom data analysis functions—no need to start from scratch or cut corners.

## Features Included in MyFavoriteAlbums

- **Explore number one albums by year range:** View and analyze your number one ranked albums across any span of years.
- **Filter by artist/band:** See all your favorite albums from a specific artist/band at a glance. 
- **View favorite albums from a specific year:** Focus on a single year to view your favorite albums from that time. 
- **Track vinyl ownership and trends:**  Identify which top-rated albums you do not yet own on vinyl, and see a ranked breakdown of the years from which you own the most vinyl records. 
- **Compare artist/bands side-by-side:**  Select two artists/bands and compare how you have rated their albums over time.

## Features Not Included in MyFavoriteAlbums

- **Stream music:** MyFavoriteAlbums does not host or play audio files, and it is not connected with external music platforms like Spotify or Apple Music.
- **Recommend albums:** MyFavoriteAlbums only displays and filters the album information you provide. 
- **Edit data live:** To make changes to your favorite albums list, you must manually update the CSV file containing this data and reupload it as the application does not allow for editing this dataset through the webpage.

## Summary of the Repository and What It Contains

All the source code and data for MyFavoriteAlbums are hosted in a public [GitHub repository](http://github.com/UW-Example-Student/MyFavoriteAlbums/).

Here is a summary of all files in the repository: 
- [data/](https://github.com/UW-Example-Student/MyFavoriteAlbums/tree/main/data) folder: Contains the core dataset for the application (```album-rankings.csv```), which holds the favorite albums of the user.
- [app.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/app.R): The main script that runs the Shiny app. It brings together the UI and server code, loads the data, and connects everything.
- [app_server.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/app_server.R): Contains the server logic that processes data and updates the outputs (like plots and tables) based on user input.
- [app_ui.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/app_ui.R): Defines how the app looks and what controls (like dropdowns and sliders) users can use to explore their album data.

The remaining files are used to process and summarize the album data, based on the purpose suggested by each filename. They help prepare the data for visualizations or tables displayed in the Shiny app.
- [albums_by_band.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/albums_by_band.R)
- [albums_by_year.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/albums_by_year.R)
- [compare_bands.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/compare_bands.R)
- [number_one_albums.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/number_one_albums.R)
- [vinyl.R](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/vinyl.R)

## System Architecture Overview
The MyFavoriteAlbums application is organized into three main components: 
- Data Layer: Contains the raw album ranking data in ```.csv``` format.
- R Files: Contains scripts to process data and run the Shiny web application.
- User Interface: Delivered through a Shiny-hosted web application and viewed on a local web browser.

These parts interact as follows: 

The data (in the CSV file) is loaded by the R scripts → the scripts clean, analyze, and visualize the data → the Shiny app provides an interactive user interface for users to view and filter album rankings.
