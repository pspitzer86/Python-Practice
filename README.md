# Python-Practice

The purpose of this challenge was to import and read various csv or text files, most of which were provided, and calculate certain values from the data to be printed in the terminal as well as an output text file.  There were two required challenges, called PyBank and PyPoll, as well as two extra ones, named PyBoss and PyParagraph.  Each of these four repositories had a main.py file were code was written and executed in VS Code, as well as a Resources folder where the csvs and text files were stored for import and an Analysis folder where our output text files were saved after each code had been run.

For the PyBank challenge, we imported a budget_data.csv with the columns, "Date" and "Profit/Losses".  We needed to analyze the data in order to find the total amount of months, the net total Profits/Losses, the average of the changes in Profits/Losses and the greatest increase/decrease in the profits as well as the month they occurred in.  The code for this looped through the data and during the loop added one to the total month count for each row found, added up each Profit/Losses value to find the net total, found the difference in Profit/Losses between each pair of adjacent months (change) and compared these differences against each other to find the month and value that had the greatest increase and decrease in profit.  The average change over the course of the data was calculated after the loop finished and all necessary values were printed in the terminal and an output file was created.

For the PyPoll challenge, a csv with election data was imported with columns, "Voter ID", "County", and "Candidate".  The code for this project needed to count the total number of votes, a list of all candidates that received at least one vote as well as their individual vote counts and the percentage of the total votes they received, and the overall winner of the election.  Two empty lists were created, one for the candidates and another to hold the votes for each candidate.  The code looped through the data and checked if a found candidate was in the appropriate list, if they weren't they were added to the list and a vote was added to the other list for that candidate.  If a found candidate was already in the list, the vote was added to that candidates count.  Every vote found was also added to the overall total of votes.  Another loop was made to go through the lists at each index in order to calculate the percentage of the total votes each candidate received as well as find the candidate with the most votes, and therefore the winner of the election.  The necessary calculations were printed in the terminal and an output file was created.

For the PyBoss challenge, a new HR system required us, as the boss, to change the way we organized our employees information.  A csv with the old format was imported with the columns, "Emp ID", "Name", "DOB", "SSN", and "State".  The new format required us to split the Name column into two separate columns for the employees First and Last Name, change the format for the DOB column from YYYY-MM-DD to MM/DD/YYYY, hide the first five digits of every employees SSN, and change the State names to their abbreviatons.  A pre-made dictionary with the US States and their associated abbreviations was used.  An empty list was made for every necessary column.  As we looped through the data, the Emp ID's were appended to the appropriate list, the Name data was split into first and last name and appended to the appropriate lists, the DOB data was split into its three parts and rearranged to fit the necessary format then appended to its list, the SSN data was split into its three parts and only the third part was concatenated with a string to hide the first five digits then added to its list, and the state abbreivation dictionary was called to replace the state name with their abbrviations and added to their list.  These lists were then zipped together and a new csv was created with the data in the new HR format necessary.

For the PyParagraph challenge, a text file of a paragraph of our choosing was analyzed to find the approximate word count, approximate sentence count, average letter count, and average sentence length.  Two sample paragraphs were provided for testing before our paragraph was run through the code.  A hint code using regular expressions was provided.  When testing the second sample paragraph, the hint code did not seem to be working as well as expected.  Due to this, the code created in the main.py file did not use regular expressions.  The paragraph text file was read and by splitting the file by period, the sentence count was calculated.  The average sentence length was found by taking the length of the resulting list from splitting the paragraph into sentences.  The paragraph was then sent through a loop to remove various kinds of punctuation.  The resulting data was then split by white space in order to find the word count.  The word count was also looped to split each word into its letters.  The length of the resulting leter list provided the letter count.  A collaboration with fellow classmate Kate Spitzer was done in order to figure out the use of the hint code using regular expressions which is in main2.py.  The hint code seemed to work much more smoothly on the first sample paragraph. The regular expression code split the imported paragraph text file into sentences by various punctuation.  The resulting sentences were sent through a loop that split them into their individual words.  The word count was calculated by finding the length of the list made by the word split.  This word split was also looped through to find the length of each word and add them all together to find the letter count.


Output Analysis Example for PyBank challenge:

Financial Analysis
--------------------------
Total Months: 86
Total: $38382578
Average Change: $-2315.12
Greatest Increase in Profits: Feb-2012 ($1926159)
Greatest Decrease in Profits: Sep-2013 ($-2196167)
