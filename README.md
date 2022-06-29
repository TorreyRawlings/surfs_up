# Surfs_up
#### The purpose of this analysis is to determine if a surf board & ice cream shop would be a good idea to open up in the island of Oahu. We are hoping to see if this would be a successful business throughout the year not just during a few months. To do this we are analyzing weather data to determine how many months have warm enough weather that ice cream would be popular. Here are some highlights:

  - In the month of June it can get up to 85 degrees and doesnt go lower than 64 degrees. With an average temperature of 64 degrees. 
  - In the month of December it gets as high as 83 degrees but goes as low as 56 degrees. The average temperature is 71 degrees.
  - It looks like the main different is the low temperature. Which is about a 8 degree difference. 


## Summary of the analysis: 
  - It doesnt seem like it gets too cold in winter that people would not want ice cream.
  - The weather of June vs December is only different by a few degrees. Since it's not too drastic it would be fair to assume that other months wouldnt be too off as well. 
  - One other factor we might want to consider looking into would be the percipitation. While it might be warm people may not want to eat ice cream if it's raining. If we want to track this we can use the following queries for June & July: 
    - session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==6).all()
    - session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==12).all()
