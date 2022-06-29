# Election_Analysis
## Analysis of Module 3 Election Results Audit

### Project Overview
  
  This project was brought to us by the local election commision who were looking for a way to summarize the election results from three counties. They wanted a way to quickly see who the winner and to see the county with the highest turnout of the three counties reported. This python script can be readily adapted to tally up future election results.
  
### Results

#### Code Used and Outputs for Analysis

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

##### Breakdown of Votes and Percentage of Votes Each Candidate Received

```
  # If the candidate does not match any existing candidate add it to the candidate list
  if candidate_name not in candidate_options:

      # Add the candidate name to the candidate list.
      candidate_options.append(candidate_name)

      # And begin tracking that candidate's voter count.
      candidate_votes[candidate_name] = 0

  # Add a vote to that candidate's count
  candidate_votes[candidate_name] += 1
  ```
  
  ![Candidate Results](https://github.com/Beardlow/Election_Analysis/blob/main/All_Candidates_in_Terminal.png)
  
  ##### Winning Candidate Results
  
  ```
        # Determine winning vote count, winning percentage, and candidate.
      if (votes > winning_count) and (vote_percentage > winning_percentage):
          winning_count = votes
          winning_candidate = candidate_name
          winning_percentage = vote_percentage

  # Print the winning candidate (to terminal)
  winning_candidate_summary = (
      f"-------------------------\n"
      f"Winner: {winning_candidate}\n"
      f"Winning Vote Count: {winning_count:,}\n"
      f"Winning Percentage: {winning_percentage:.1f}%\n"
      f"-------------------------\n")
  print(winning_candidate_summary)
  ```
  
  ![Winning Candidate Results](https://github.com/Beardlow/Election_Analysis/blob/main/Winning_Candidate_in_Terminal.png)
