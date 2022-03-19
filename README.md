# ELECTION_ANALYSIS
Performing analyses on election_results data using python.
# Overview of the project
The project analyses election_results data and submits the election audit result to the election commission.
## purpose of the election audit:
This project aims to conduct an election audit for the colorado board of elections to find the total votes, total county votes, largest county turnout, winning candidates, and the total amount of votes he got and calculate the percentage of winning votes. 
# Election-audit results
The results of the election are as follows:

1. Total votes

 * The total number of votes cast in this congressional election is 369,711.
 
 Folllowing is the code to generate total votes:

 Print the final vote count (to terminal)
 
    election_results = (
        f"\nElection Results\n"
        f"-------------------------\n"
        f"Total Votes: {total_votes:,}\n"
        f"-------------------------\n\n"
        f"County Votes:\n")
    print(election_results, end="")


2. votes by county
  * Jefferson County had 38,855 voters and 10.5% of votes from each county out of total votes.
  
  * Denver county had 306,055 voters and 82.8% of votes from each county out of total votes.
  
  * Arapahoe county had 24,801 voters and 6.7% of votes from each county out of total votes
 
  Folllowing is the code to generate county votes:
  
     
  Write a for loop to get the county from the county dictionary.
    for county in county_list
    
        # 6b: Retrieve the county vote count.
        county_vote = county_votes.get(county)
        
        # 6c: Calculate the percentage of votes for the county.
        county_vote_percentage = float(county_vote) / float(total_votes) * 100

         # 6d: Print the county results to the terminal.
         county_results = (
            f"{county}: {county_vote_percentage:.1f}% ({county_votes:,})\n")
         #Print county results and percentage to the terminal.
         print(county_results)

  
  
3. largest county turnout
  * Denver county had the largest number of votes.
  
  Folllowing is thw code to generate largest county turnout :
  
 Write an if statement to determine the winning county and get its vote count.
 
         if (county_vote > largest_county_turnout_count) and (
             county_vote_percentage > largest_county_percentage):
             
             # determine winning counties, percentage and county won.
             largest_county_turnout_count = county_vote
             largest_county_percentage = county_vote_percentage
             largest_county_turnout = county
             
              
 Print the county with the largest turnout to the terminal.
 
    winiing_county_print = (
        f"-------------------------\n"
        f"largest county turnout: {largest_county_turnout}\n"
        f"-------------------------\n"
    )


  
4. Detailed results of total votes each candidate received

 * Charles Casper Stockham received 85,213 votes, 23.0% of votes out of the total votes.
 
 * Diana DeGette received 272,892 votes,73.8% of votes out of the total votes.
 
 * Raymond Anthony Doane received 11,606 votes, 3.1% of votes out of the total votes.

following is the code to generate vote count and percentage:

 Retrieve vote count and percentage
 
        votes = candidate_votes.get(candidate_name)
        vote_percentage = float(votes) / float(total_votes) * 100
        candidate_results = (
            f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")

        # Print each candidate's voter count and percentage to the
        # terminal.
        print(candidate_results)
 
 
  * Diane DeGette won the election with 272,892 votes and 73.8% of the total votes.

following is the code to generate winning vote count, winning percentage, and candidate  :
  
  
 Determine winning vote count, winning percentage, and candidate  
 
        if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage

  Print the winning candidate (to terminal)
  
    winning_candidate_summary = (
        f"-------------------------\n"
        f"Winner: {winning_candidate}\n"
        f"Winning Vote Count: {winning_count:,}\n"
        f"Winning Percentage: {winning_percentage:.1f}%\n"
        f"-------------------------\n")
    print(winning_candidate_summary)
    
    
    
    
    After running the code and saving it to the text file the ouput is shown in the image:
    
    <img width="393" alt="Screen Shot 2022-03-18 at 1 50 11 PM" src="https://user-images.githubusercontent.com/100738688/159105412-61adedfd-34b6-48b6-b1bc-0254edf41618.png">

           
# Election-audit summary
This script can be modified and used for other elections. The first example would be if it were for a federal congressional election, we could use the same script by changing counties to the state. The second example would be adding demographics such as age, sex, and ethnicity among the candidates to understand better which group they should focus on more.







  




