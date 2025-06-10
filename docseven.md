# (Optional) Updating the Year Range

By default, the MyFavoriteAlbums application is set up to display data from 1993 to 2024. If your album rankings include years outside this range, the app will not break, but:
- Those albums will not appear in visualizations that filter or plot data by year (e.g. in the “Number One Albums” or “Band Comparison” tabs). 
- Your full data is still loaded and available, but anything outside the defined year range is simply ignored in those specific views.

Therefore, if your data includes years outside the 1993-2024 range, you will need to update the code in RStudio:

- In ```app_ui.R```: Update the ```sliderInput()``` for the “Number One Albums” tab. For example, to expand the range to 1990-2030:
    ```
    tabPanel("Number One Albums",
        ...
        sliderInput("rng", "Choose the Years", value = c(1990, 2030), min = 1990, max = 2030),
        ...
    ),
    ```
- In ```compare_bands.R```: Update the x-axis settings in both ```scale_x_continous()``` and ```expand_limits()```. For example, to expand the range to 1990-2030:
    ```
    scale_x_continuous(breaks=seq(1990,2030,1))+
    ...
    expand_limits(x=c(1990,2030), y=c(0,10))
    ```

Save these changes in both ```app_ui.R``` and ```compare_bands.R```.


