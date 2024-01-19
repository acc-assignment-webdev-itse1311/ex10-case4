# NP HTML5, CSS3, and JavaScript 6e
# Tutorial 10, Case Problem 4

## Instructions:
```
1.  Use your editor to open the vw_election_txt.html and vw_results_txt.js files from the html10 c case4 folder. Enter your name and the date in the comment section of each file, and save them as vw_election.html and vw_results.js respectively.
2.  Go to the vw_election.html file in your editor. Directly above the closing </head> tag, insert script elements to link the page to the vw_congminn.js and vw_results.js files in that order. Defer the loading and running of both script files until after the page has loaded.
3.  Scroll down the file and, directly above the footer, insert an empty section element. You will write the HTML code of the election report in this element. Save your changes to the file.
4.  Open the vw_congminn.js file in your editor and study the contents. Note that the file contains the results of 8 congressional elections in Minnesota. The candidate information is stored in multidimensional arrays named candidate, party, and votes. Do not make any changes to this file.
5.  Go to the vw_results.js file in your editor. Declare a variable named reportHTML containing the following HTML text <h1>title</h1> where title is the value of the raceTitle variable stored in the vw_congminn.js file.
6.  Create a for loop that loops through the contents of the race array using i as the counter variable. Place the commands specified in Steps a through e within this program for loop:
    a.  Create a variable named totalVotes that will store the total votes cast in each race. Set its initial value to 0.
    b.  Calculate the total votes cast in the current race by applying the forEach() method to i th index of the votes array using the calcSum() function as the callback function.
    c.  Add the following HTML text to the value of the reportHTML variable to write the name of the current race in the program loop <table> <caption>race</caption> <tr><th>Candidate</th><th>Votes</th></tr> where race is the ith index of the race array.
    d.  Call the candidateRows() function (you will create this function shortly) using the counter variable i and the totalVotes variable as parameter values. Add the value returned by this function to the value of the reportHTML variable.
    e.  Add the text </table> to the value of the reportHTML variable.	
7.  After the for loop has completed, write the value of the reportHTML variable into the innerHTML of the first (and only) section element in the document.
8. Next, create the candidateRows() function. The purpose of this function is to write individual table rows for each candidate, showing the candidate's name, party affiliation, vote total, and vote percentage. The candidateRows() function has two parameters named raceNum and totalvotes. Place the commands in Steps a through c within this function.
   a. Declare a local variable named TOWHTML that will contain the HTML code for the table row. Set the initial value of this variable to an empty text string.
   Explore b. Create a for loop in which the counter variable j goes from 0 to 2 in steps of 1 unit. Within the for loop do the following:
   i.  Declare a variable named candidateName that retrieves the name of the current candidate and the current race. (Hint: Retrieve the candidate name from the multidimensional candidate array using the reference, candidate[raceNum][j].)
   ii.  Declare a variable named candidateParty that retrieves the party affiliation of the current candidate in the current race from the multidimensional party array.
   iii.  Declare a variable named candidatevotes that retrieves the votes cast for the current candidate in the current race from the multidimensional votes array.
   iv.  Declare a variable named candidatePercent equal to the value returned by the calcPercent() function, calculating the percentage of votes received by the current candidate in the loop. Use candidateVotes as the first parameter value and totalVotes as the second parameter value.
   v.  Add the following HTML code to the value of the rowHTML variable  <tr> <td>name (party)</td> <td>votes (percent)</td> </tr> where name is the value of candidateName, party is the value of candidateParty, votes is the value of candidateVotes, and percent is the value of candidatePercent. Apply the toLocaleString() method to votes in order to display the vote total with a thousands separator. Apply the toFixed(1) method to percent in order to display percentage values to 1 decimal place. c. Return the value of the rowHTML variable.
9. Save your changes to the file, and then load vw_election.html in your browser. Verify that the three candidate names, party affiliations, votes, and vote percentages are shown for each of the eight congressional races.
10.  Pam also wants the report to display the vote percentages as bar charts with the length of the bar corresponding to the percentage value. Return to the vw_results.js file in your editor. At the bottom of the file, create a function named createBar() with one parameter named partyType. Add the commands described in Steps a through b to the function:
     a. Declare a variable named barHTML and set its initial value to an empty text string.
     Explore b. Create a switch/case statement that tests the value of the partyType parameter. If partyType equal "D" set barHTML equal to: <td class='dem'></td> If partyType equals "R" set barHTML equal to: <td class='rep'></td> Finally, if partyType equals "I" set barHTML to: <td class='ind'></td>

11.  Return the value of barHTML. Next, add these empty data cells to the race results table, with one cell for every percentage point cast for the candidate.
12.  Scroll up to the candidateRows() function. Directly before the line that adds the HTML code </tr> to the value of the rowHTML variable, insert a for loop with a counter variable k that goes from 0 up to a value less than candidatePercent in increments of 1 unit. Each time through the loop call the createBar() function using candidateParty and candidatePercent as the parameter values.
13.  Add comments throughout the file with descriptive information about the variables and functions.
14.  Save your changes to the file, and then reload vw_election.html in your browser. Verify that each election table shows a bar chart with different the length of bars representing each candidate's vote percentage.
```


