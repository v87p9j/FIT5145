java c
Faculty of Information Technology 
Semester 2, 2024 
FIT5145: Foundations of Data Science 
Assignment 4: Description 
Friday, Week 13 (October 25, 2024) 11:55 PM
Assessment Details: 
● Assessment Type: Individual Assignment
● Total marks: 40%
●   Due Date: Friday, Week 13 (October 25, 2024) 11:55 PM. Please note that we do not accept submissions after November 1, 2024 (i.e., 7 days after the due date).
Hand in Requirements: 
In this assignment, three files (PDF report, RMD file, and csv file) should be submitted.
1.   A report in PDF containing your (a) code, (b) answer, and (c) explanation used to answer each question. Please make sure that your answers to all the questions are numbered correspondingly.
(a) code: Make sure to include all the shell commands for Task A and the R codes for Tasks B-D in the PDF report. For the shell commands, please copy your codes and paste into Word or other word processing software (Please do NOT take the screenshots of your code).For the R codes, please directly convert the RMD file including your codes into the PDF file (Note: Please Knit RMD to HTML and print the HTML as pdf). If you want to use Microsoft Word or other word processing software to format your submission, please copy your codes from the RMD file and paste into Word (Please do NOT take the screenshots ofyour code).
You need to merge the shell PDF and R PDF files into a single pdf file.
(b) answer: Please make sure to include screenshots/images of the code outputs and written answers (not screenshot) for each question of Tasks A-D in PDF.
(c) explanation: Please explain how you answered each question (i.e., explaining your codes or summarising your work for each question).
Marks will be assigned to reports based on their correctness and clarity. For instance, higher marks will be given to reports containing graphs with appropriately labelled axes.
2.   The RMarkdown file: Please submit the RMarkdown file that contains your R codes for Tasks B-D of this assignment. Your file should contain all the codes, proper comments, and any instructions of libraries that need to be installed.
Notes: 
1.   Whenever a question asks for a certain value, your code should produce the value. For example, when a question asks for the number of rows contained in a table, your code should  print out the answer. Extraction of the answer manually will not earn any marks.
2.   Assignment should be submitted in three files (PDF report, RMD file and csv file): (a)  An RMD file that generates errors when running will not be considered
3. Please make sure that you can select and highlight texts in your PDF, as shown below then the turnitin score can be generated properly for your PDF file (we just need the Turnitin score for the PDF file, not the RMD file).
Task A:  Shell commands In   this   task,   you   are   required   to   explore   and   wrangle    the   data    in    the   file “covid19-cable-broadcast.csv”, which contains transcript. paragraphs that were collected from various programs aired in 2020 on cable and broadcast news networks, e.g., World News Tonight on ABC and Anderson Cooper 360 Degrees on CNN. These transcript. paragraphs have been manually annotated according to theirrelevance to COVID-19. The file contains different variables to describe each collected transcript. paragraph, as described below.
Column Name 
Description 
ID 
The ID of the paragraph 
network 
Cable and broadcast news networks such as ABC, CNN, FOX, etc. 
program Programs aired on cable and broadcast news networks, such as “worldnewstonight” (the program World News Tonight on ABC) 
date 
The date when the corresponding program and paragraph aired 
paragraph 
The textual content of the paragraph 
category The   categorical   label   provided by humans to   indicate a paragraph’s    relevance    to    COVID-19,    i.e., covid_direct, covid_indirect, and non_covid Please note that you are only allowed to use shell commands as you would run in Linux shell, Mac terminal, or Cygwin, to tackle this task. Using other utilities or tools such as PowerShell is NOT allowed.
1.   What is the date range of the collected paragraphs?
2.   We want to preprocess the ID and date columns.
a. Count lines with an id that is not a number of 6 digits long,i.e., id values that contain anything other than numbers OR are of a length more/less than 6.
b. Remove the lines mentioned in Q2-a and remove time values in the date column. For example, the date column will contain “29/04/2020”, instead of having “29/04/2020 23:13” .
c. Display the  first  3 lines of the dataset that was filtered in Question 2-b. Store the filtered  dataset  in  a  file  named  “filtered_covid.csv”  and use this file  for  the remaining questions in Task A. 
3.   When was the first and last mention of the term “Australia” in the column paragraph? Please note that the first and last mention of a term refers to the chronologically earliest and latest paragraph containing the term in the dataset and the term to be searched is case sensitive. 
4.  Let’s investigate theprogram column.
a.   How many unique values are there in theprogram column?
b.   Can you write commands to list the top 5 most frequent program values in the dataset (i.e., the top 5 programs with the largest number of paragraphs)?
5.   Let’s investigate the paragraph column.
a.   How many paragraphs contain both “ventilator” and “hospital”? (Note: Please ignore cases and consider variations.)
b.   How many paragraphs mention unemployment statistics? (Note: Please ignore cases and consider variations)
6.   In 代 写FIT5145: Foundations of Data Science Assignment 4: Description Semester 2, 2024R
代做程序编程语言 the   following,  please  generate  the  dataset  filtered  according  to  the  following conditions:
a.   Keep these columns: network,program, date, paragraph, and category 
b.   Keep the paragraphs satisfying the following conditions: (i) the date belongs to an odd month (e.g.: January, March,  … , November);  (ii)  the network is cbs  ; and  (iii) the category is covid_direct.
Then, print out the first and last date of the filtered dataset (Please include a header).
Task B:  Data Collection and Exploratory Data Analysis Using R There are many ways to collect data from different sources. One of them is web scraping. In this task, you are required to scrape data from websites, wrangle data scrapped if required, and visualise them.
Task B1:
Please extract the following table, “Historical rankings” from the web, ICC Men's T20I Team Rankings in Wikipedia  (Note: please extract the entire table).
(https://en.wikipedia.org/wiki/ICC_Men%27s_T20I_Team_Rankings).

Then, please print out the following summarised table. Note: You might need to pre-process the data that you extracted from the web.
Country 
Earliest_start 
Latest_end 
Average_duration 
Pakistan 
2017-11-01 
2020-04-30 
294.67 
Sri Lanka 
2012-09-29 
2016-02-11 
212.80 
India 
2014-03-28 
2024-10-03 
197.00 
New Zealand 
2016-05-04 
2018-01-27 
191.33 
England 
2011-10-24 
2022-02-20 
187.00 
Australia 
2020-05-01 
2020-11-30 
106.00 
South Africa 
2012-08-08 
2012-09-28 
21.00 
West Indies 
2016-01-10 
2016-01-30 
21.00 The  summarised  table  shows  the  earliest  start,  latest  end,  and  average  duration  for  each country.  (Note:  Please  replace  the  'Present'  value  in  India  with  the  current  date  you  are working with.)
Task  B2: Please  choose  a  different  website  that  you  are  interested  in  and  follow  the instructions below:
1.   Scrape data contained in table format in a website
2.   Wrangle data if required.
3.   Create a plot for the scraped data.
4.   Discuss the information or insights that can be drawn from the chart.
Task C:  Exploratory Data Analysis using R For Task C, you are required to visualise the relationship between the births, deaths, total  fertility rate (TFR), net overseas migration (Births) and net interstate migration (NIM) for the  different  Australian  states/territories,  and  gain  insights on how these relations and trends  change  over  time.  The  data  files  used  in  this  task were originally downloaded from the  Australian  Bureau  of  Statistics.  We  have  extracted  the  data  from  the  original  files  and  transformed them into a simpler format. Please download the data from Moodle:
● Births.csv - This file contains yearly data regarding the recorded number of births by Australian state/territory of registration between 1977 and 2016.
● Deaths.csv -This file contains yearly data regarding the recorded number of deaths by Australian state/territory of registration between 1977 and 2016.
● TFR.csv - This file contains yearly data on the recorded average number of births per woman over her lifetime by each state/territory between 1971 and 2016.
● NOM.csv - This data file (Net Oversea Migration) contains yearly data on the net gain or  loss  of  population   through immigration   (migrant arrivals) to  Australia   and emigration (migrant departures)from Australia, for the period between 1977 and 2016.
● NIM.csv- This data file (Net Interstate Migration) contains yearly data on the net gain or loss of population through the movement of people from one state or territory to another, for the period between 1977 and 2016.
B1. Investigating the Births, Deaths and TFR Data 
1.   Draw the number of births and deaths recorded in each state or territory over different years, and describe the plot.
2.  Next, plot the natural growth in Australia's population over different years. Describe the plot.
3.   Inspect  the  data  on  Total  Fertility  Rate  (TFR.csv)  for  Queensland  and  Northern Territory.
a.   What was the minimum value for TFR recorded in the dataset for Queensland and when did that occur?
b.   What was the  corresponding TFR value for Northern Territory in the same year?
4.   Identify two  additional variables  from external  sources that might affect the Total Fertility Rate (TFR) in New South Wales (NSW) and analyse the relationship between these  variables  and  the  TFR.  Marks will be awarded based on the depth of your investigation (including the analyses and discussions conducted) (Note: You need to provide the data source links)
B2. Investigating the Migration Data (NOM and NIM) 
1.   Let’s look at the Net Overseas Migration (NOM) data in different states over time.
a.   Use  R to plot the NOM to Victoria,  Tasmania and Western Australia over time. Explain and compare the trend in all three states (VIC, TAS and WA). What do you observe?
b.   Plot the NOM to Australia over time.
2.   Identify two additional variables from external sources that might affect the NOM in Australia and analyse the relationship between these variables and the NOM. Marks will be awarded based on the depth of your investigation (including the analyses and discussions conducted) (Note: You need to provide the data source links)
3.   Create a table to display the states with the highest and lowest total migration shifts for each year.
4.   Create a plot to show the proportion of total migration by each state for each year and provide a discussion of the plot.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
