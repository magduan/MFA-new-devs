# Frequently Asked Questions (FAQ)

## Table of Contents
1. [Setup and Installation](#one)
2. [Working With Your Album Data File](#two)
3. [Running and Navigating the Application](#three)
4. [Publishing Your Application Online](#four)
5. [Troubleshooting and Common Issues](#five)

<hr>
<a id="one"></a>

## Setup and Installation

### Do I need to reinstall R and RStudio every time? 
No. You only need to install R and RStudio once. After that, you can open RStudio whenever you want to use the application.

### I am getting a “package not found” error. What should I do? 
Make sure you installed all required packages. 
In RStudio, run the following commands in the *Console* pane:
```
install.packages("dplyr")
install.packages("DT")
install.packages("shiny")
install.packages("ggplot2")
```
If an error persists, check for typos or internet connectivity issues.

<hr>

<a id="two"></a>

## Working With Your Album Data File

### Do I have to fill in every column in the album spreadsheet?
No, none of the columns are strictly required. However, we recommend filling out the following to get the most out of the application’s visualizations:
- Year
- Ranking
- Album
- Artist 
- Rating

The Vinyl, EP, and Live columns are optional and should only be filled in if they apply to that album (mark “v” if you own it on vinyl, “EP” if it is an EP, “Live” if it is a live recording).

### Can I update my album data later? 
Yes!
To update your album data:
1. Open your ```album-rankings.csv``` file and add or edit entries as needed. 
2. Save the file. 
3. Re-run the application in RStudio to load the updated data.

### What if I forget to save my album spreadsheet as a ```.csv``` file? 
The application only reads ```.csv``` files. When saving or downloading your spreadsheet, make sure to choose ```.csv``` as the file format.

<hr>

<a id="three"></a>

## Running and Navigating the Application
### Can I use MyFavoriteAlbums without an internet connection?
Yes, you can use/run the application locally without an internet connection. However, an internet connection is needed to:
- Download R, RStudio, or packages.
- Publish your application using shinyapps.io.

### Nothing happens when I click “Run App” in RStudio. What should I check? 
Make sure the following are in place:
- The ```app.R``` file is open in RStudio, and you are clicking “Run App” from that tab.
- The required packages are installed. 
- All files are present, including ```album-rankings.csv``` in the correct folder.
- There are no error messages in the *Console* pane.

If you see a new or unfamiliar error message (not related to the items above), copy and paste it into Google. Many common issues have already been answered on forums like Stack Overflow.

### What does it mean if a visualization is blank? 
This usually means that your dataset does not contain any relevant data for the filters you have selected, or there may be formatting issues in your ```album-rankings.csv``` file. Double-check that your file includes entries that match the selected filters. Also, make sure that all column names and formats are correct (for example, the Year column should contain four-digit numbers like 1998, not written-out text like “nineteen ninety-eight”).

<hr>
<a id="four"></a>

## Publishing Your Application Online

### Is publishing on shinyapps.io required? 
No. Publishing is optional. It lets others access your application through a link, but you can use it privately on your own computer without publishing.

### Can I update my published application after adding new data? 
Yes. After editing your ```album-rankings.csv``` file or other application code, re-run the application in RStudio. Click the **Publish** button again. The site will update your application with the latest version.

<hr>
<a id="five"></a>

## Troubleshooting and Common Issues

### I accidentally deleted a code file from the application folder. What should I do?
To restore the missing file:
1. Re-download the original ```MyFavoriteAlbums``` file from the [GitHub repository](https://github.com/UW-Example-Student/MyFavoriteAlbums).
2. Copy/drag the missing code file back into your working folder.

### I want to start over with new album data. How do I reset the application?
To reset the application with a new album list: 
1. Delete or rename your existing ```album-rankings.csv``` file in the ```data``` subfolder. 
2. Create a new version of your album list and save it as ```album-rankings.csv```. 
3. Place the new file in the ```data``` subfolder. 
4. Run the application again. Your updated data will now be displayed.
