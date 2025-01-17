# geolakes
Collection of scripts used for figures or calculations in the geolakes publication. 


### Creating summary figure of data available in WQP

First, you need to pull down the number of records by site type and characteristic type over time from the Water Quality Portal using functions from `R/wqp_retrieval_functions.R`:

```{r}
getAllRecordsCounts()
```

These queries take time to run and cache individual files (each site type, characteristic type combination is one file). Once all files are cached, the function will create a single CSV file stored in `data/`. If the function is aborted, you can just rerun `getAllRecordsCounts()` and it will skip the queries that already have stored files in `cache/`. 

Once the `data/wqp_database_counts.csv` file exists, you can use the plotting functions from `R/wqp_plotting_functions.R`:

```{r}
plotSparklinesBarchart()
```

This function will create the the barchart with sparklines figure and save it as a PNG in `figures/`. 

</br>

Disclaimer
----------
This software is in the public domain because it contains materials that originally came from the U.S. Geological Survey, an agency of the United States Department of Interior. For more information, see the official USGS copyright policy at [http://www.usgs.gov/visual-id/credit_usgs.html#copyright](http://www.usgs.gov/visual-id/credit_usgs.html#copyright)

This information is preliminary or provisional and is subject to revision. It is being provided to meet the need for timely best science. The information has not received final approval by the U.S. Geological Survey (USGS) and is provided on the condition that neither the USGS nor the U.S. Government shall be held liable for any damages resulting from the authorized or unauthorized use of the information. Although this software program has been used by the USGS, no warranty, expressed or implied, is made by the USGS or the U.S. Government as to the accuracy and functioning of the program and related program material nor shall the fact of distribution constitute any such warranty, and no responsibility is assumed by the USGS in connection therewith.

This software is provided "AS IS."


 [
    ![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)
  ](http://creativecommons.org/publicdomain/zero/1.0/)
