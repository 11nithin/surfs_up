# SURFS UP

## Purpose of the analysis

Before starting up Surf and Ice cream shop in Oahu. Investor wants more information about temperature trends before opening the surf shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.


## Results

### June Temprature Summary
![JUNE](https://github.com/11nithin/surfs_up/blob/main/Resources/June_Stat%20summary.PNG)

### December Temperature Summary

![DECEMBER](https://github.com/11nithin/surfs_up/blob/main/Resources/Dec%20_Stat%20summary.PNG)


 - Average temperature in June(74.9) is 3.86 degree higher than December(71.04) 
 - Standard deviation of June is less compared to December. It means more variation or spread in decemeber temperature
 - Minimum temerature in December is 56.0 and June is 64.0. But by looking at the quartiles even though there are some cold days temperature renges from 69 -74 F. 
  

## Summary
We pciked June and December in Oahu to determine if the surf and ice cream shop business is sustainable  year round. When we campare the month june and December there is only 3.86 degree differnece in average temparature. But there are cold days in December. Eventhough from the data it looks like Oahu weather is good for surfing and ice cream. Sales will be little less in December when compared to June. 

- Other than the temperature its good to do analysis collecting more data 
   - percipation each month to see the effect of rain
   - Wind condition on each month
  

#### Decemeber Percipitation
````
dec_prcp = session.query( Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
dec_prcp = list(np.ravel(dec_prcp))
dec_prcp_df = pd.DataFrame(dec_prcp)
dec_prcp_df.describe()
````
![dec](https://github.com/11nithin/surfs_up/blob/main/Resources/December_percipitation%20_summary.PNG)


#### June Percipitation
````
june_prcp = session.query( Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()
june_prcp = list(np.ravel(june_prcp))
june_prcp_df = pd.DataFrame(june_prcp)
june_prcp_df.describe()
````
 ![JUNE](https://github.com/11nithin/surfs_up/blob/main/Resources/June_percipitation%20_summary.PNG)


