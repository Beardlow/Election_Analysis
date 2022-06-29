# Election_Analysis
## Analysis of Module 3 Election Results Audit

### Project Overview
  
  This project was brought to us by the local election commision who were looking for a way to summarize the election results from three counties. They wanted a way to quickly see who the winner and to see the county with the highest turnout of the three counties reported. This python script can be readily adapted to tally up future election results.
  
### Results

#### Code Used for Analysis

This analysis captures several key, and requested, metrics from the data file "election_results.csv" using a python script.

##### Total Votes Cast in the Precinct
```
for row in reader:

        # Add to the total vote count
        total_votes = total_votes + 1
```
##### Breakdown of Voter Turnout for Each County
```
if county_name not in counties:

            # 4b: Add the existing county to the list of counties.
            counties.append(county_name)

            # 4c: Begin tracking the county's vote count.
            counties_dict[county_name] = 0

        # 5: Add a vote to that county's vote count.
        counties_dict[county_name] += 1
```
As we can see below Denver county had the highest turnout with a total of 306,055 votes.

![County Results](https://github.com/Beardlow/Election_Analysis/blob/main/County_Results_in_Terminal.png)

