Explanation of 15_days_of_learning_sql Query
Using Microsoft SQL server(MS SQL server)
dates_hackers-This is the table view which gives a count of submissions grouped by submission_date and hacker_id.
day1_hacker-To see the count of the users till any particular date starting from day 1 (2016-03-01).
min_max- To understand what are the first, last and no. of days of difference betweeen first and last dates of submissions by the hackers.
cumuCountLag- Table to get the cumulative number of days submitted by each hacker and also a lagged date (prevDay).
prevDay- Column to check the difference in days consecutively.
p1_interm-This is a derived table from the above tables by applying all the conditions.
p1-its own table (the left chunk) to finally join into the final output.
topHackers- This table view assigns ranks to hackers based on number of submissions in each day.
p2 - It’s own table, the right chunk to finally join

Output goals for 15_days_0f_learning_sql
  1)submission_date
  2) number of distinct hackers who made submissions each day
  3)hacker_id of hacker who made maximum number of submissions
  4)hacker name of 3
  order conditions for 3 and 4- maximum submissions and lowest hacker_id


Logic of sql_project_planning
Using MySQL
Select Start_Date not in the End_Date, and select End_Date not in Start_Date, and then cross join these two. 
Select Min(End_Date) and filter by Start_Date < End_Date and order by Datediff(,). 
Datediff takes only two expressions and separated by a comma, instead of a minus sign.

