# Election Analysis

## Overview of Election Audit

### Purpose

###### The purpose of Module Three and the Election Analysis Challenge is to learn how to use the programming language, Python, in conjunction with the software, Microsoft Visual Studio Code.  By using Python and VS Code, it is my responsibility to confirm the winner of the election and analyze the data further to determine which county had the highest voter turnout.  The actual vote count and percentages were determined for each candidate and each county.  

### Election Audit Results

- **Total Votes:** 369,711 total votes were cast in this congressional election
- **Votes by County:** Jefferson: 10.5% (38,855); Denver: 82.8% (306,055); Arapahoe: 6.7% (24,801)
- **Largest County Turnout:** Denver County had the largest number of votes in this congressional election
- **Votes by Candidate:** Charles Casper Stockham: 23.0% (85,213); Diana DeGette: 73.8% (272,892); Raymon Anthony Doane: 3.1% (11,606)
- **Winner:** Diana DeGette 73.8% (272,892)


<img src="Resources/Election_Results.PNG" width="300">

### Election Audit Summary

###### It is my opinion, the Election Analysis script can be modified in at least two methods in order to be used for other elections.  Initially, in the file_to_load path, the filename will need to be updated from election_results.csv to the new filename for the other election files. Next in the first for loop of the script, the row index numbers for candidate_name and county_name will need to be adjusted to align with the new CSV file tied to the other elections. 

1. Update the filename from election_results.csv to the new filename for the other election files.

```
# Add a variable to load a file from a path.
file_to_load = os.path.join("Resources", "election_results.csv")
# Add a variable to save the file to a path.
file_to_save = os.path.join("analysis", "election_results.txt")
```
2. In the first for loop, the row index numbers for candidate_name and county_name will need to be adjusted to align with the new CSV file. 

```
# For each row in the CSV file.
    for row in reader:

        # Add to the total vote count
        total_votes = total_votes + 1

        # Get the candidate name from each row.
        candidate_name = row[2]

        # 3: Extract the county name from each row.
        county_name = row[1]

        # If the candidate does not match any existing candidate add it to
        # the candidate list
```