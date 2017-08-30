# U.S Air and Drone Strikes in the 21st Century

This group project for INFO 3300: "Data-Drives Web Applications" used data from the Bureau of Investigate Journalism in order to track air strikes in Pakistan, Yemen, Somalia, and Afghanistan over the past 15 years. Group members include Vinisha Mittal and Chaneil Hall.

# Process

Part of this project included cleaning up data from four different datasets (one per country) in order to extract the exact numbers that were relevant to this project. We needed to manually go in and add an administrative district section (called “Region”) for every strike across all four datasets, because we needed to properly map them to regions specified in the JSON files. Thus we had to research the location of every single strike.

Additionally, we had to search for 4 different JSON files representing the shape of Afghanistan, Pakistan, Somalia, and Yemen - with the appropriate divisions that we wanted. Every country except Pakistan was divided into its first-level administrative divisions, but Pakistan had a lot of strikes concentrated in one area, so we wanted to draw attention to even smaller regions in that area - using its second-level administrative divisions . This was grabbed from mapzen.

We also considered showing relative locations of each strike (one location associated with each region) in the form of red and blue circles. Red represented strikes under the Bush administration, and blue represented strikes under the Obama administration. While we did implement this for a while (going in and adding in “X” and “Y” columns to the datasets, which gave pixel descriptions of the circles), we ultimately decided to take it out for a number of reasons. While it did give another layer of complexity to our visualization, we decided it might be too confusing to an outside user, who wouldn’t know what exactly they were looking at or looking for. 

We ended up supplementing this visualization with a chart-like visualization that was unique to each country. Since we wanted to get an understanding of how the amount of civilian deaths may or may not have changed over time, we included a “side panel” chart that appeared on expanding a specific map. This gave us the estimated range of deaths due to strikes in a particular region during a specific year, allowing the user to easily compare across regions and years.

Time was also a variable we wanted to consider. We decided to implement a slider that would give the previously mentioned data, subject to year. We also developed an “automatic” visualization, that would let the user click a button and smoothly see how the map data changes over 15 years. This can be done on both the 4 map view and individual maps. This was given alongside the option of manually moving the slider and seeing the changes.

# Installation

- Clone this repo to your computer.
- Navigate to the folder using "cd usa-dronestrikes"
- Type the command "python -m SimpleHTTPServer"
- Open up a webpage and navigate to "localhost:8000"

