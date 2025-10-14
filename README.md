<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Visualize data with QuickSight

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-analytics-quicksight)

**Author:** PATRICK ADDAI  
**Email:** patrickaddai1689@gmail.com

---

![Image](http://learn.nextwork.org/refreshed_amber_shy_cantaloupe/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Introducing Today's Project!

In this project, I will demonstrate how to use Amazon Quicksight to analyse data and generate visualization and insgights. I'm doing this project to learn how to use cloud data services for data analysis

### Tools and concepts

Services I used were QuickSight and S3. Key concepts I learnt include manifest.Json files, data visualisation techniques (e.g. charts, filters) and how to perform a data refresh in QuickSight.

### Project reflection

This project took me approximately2 hours including demo time. The most challenging part was understanding how manifest.json file works. It was most rewarding to generate a PDF of our finished visualisation.

After this project, I plan to work on day THREE of the beginners challenge. I will start this project tomorrow.

---

## Upload project files into S3

S3 is used in this project to store two files, which are manifest.json which tells Quicksight about the structure and format of the data that will be analysing and netflix_title.csv which is a raw data that is here to analyse.

I edited the manifest.json file by updated the S3 URL that correspond to the dataset file location. It’s important to edit this file because it help Quicksight to find and analyse the data. If I didn't update this file Quicksight wouldn't know the correct location of my dataset. This will cause error.

![Image](http://learn.nextwork.org/refreshed_amber_shy_cantaloupe/uploads/aws-analytics-quicksight_3c3cd85a)

---

## Create QuickSight account

Creating a QuickSight account cost $0 as account stay on for 30 days free trial. Make sure you unchecked an addon in the sign up side called picks on preference report so you don't get charge.

Creating an account took me about 5 mins including setting up my S3 bucket permissions.

![Image](http://learn.nextwork.org/refreshed_amber_shy_cantaloupe/uploads/aws-analytics-quicksight_f4ab4214)

---

## Download the Dataset

I connected the S3 bucket to QuickSight by visiting the Dataset page. There were so many options for data sources I could connect to (databasees and external tools/platforms like Salesforce), and I selected S3!

The manifest.json file was important in this step becaus it tells QuickSight how to read the data in this project. It tells  QuickSight that I am uploading a .CSV file (spreadsheet) and the delimiter (i.e. commas) so that QucikSight knows how to break up the data to analysis. Otherwise, QuickSight might get confused.

![Image](http://learn.nextwork.org/refreshed_amber_shy_cantaloupe/uploads/aws-analytics-quicksight_6f874996)

---

## My first visualization

To create visualizations on QuickSight, I simply have to click on Data fields e.g. release year and QucikSight will automatically generate a graphs that best suite the type of Data. You can also try  data labels into sections like 'Group' or X Axis to determine how our graphics should treat the data.


The chart/graph shown here is a breakdown of the Release year of the content inside Netflix i.e. how many TV shows or movies were release on xyz year. You can see that there is a total of 8800+ content  pieces and 2019 is the year with the most amount of content released. 

I created this by clicking the release year data label and changing automatically generated chart from bar chart to a donut chart.

![Image](http://learn.nextwork.org/refreshed_amber_shy_cantaloupe/uploads/aws-analytics-quicksight_aff3aad7)

---

## Using filters

Filters are useful for narrowing down my data to the subset that we want to focus on and in this case we could use filters to focus on the specific categories that I want to analyse. Filters are also used to only look at content with a released date from 2015 and beyond.

This visualization is a breakdown of TV shows and Movies that belong in one of three categories  - Action &Adventure, TV comedies and Thriller. Here I added a filter based on the 'listed on' data label i.e.  only these three categories could pass the filter.

![Image](http://learn.nextwork.org/refreshed_amber_shy_cantaloupe/uploads/aws-analytics-quicksight_c32248c5)

---

## Setting up a dashboard

As a finishing touch, I updated the titles of the chart in my dashboard so that they are easily readable. The default names would simply mention the data labels e.g released year but the new titles communicates the purpose of the chart.

Did you know you could export your dashboard as PDFs too? I did this by seleting publish and the generate PDF on the top right hand corner of my QuickSight analysis.

![Image](http://learn.nextwork.org/refreshed_amber_shy_cantaloupe/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Refreshing source data

In this project's extension, I downloaded fresh data that's different from my original dataset because it had rows of empty Country data. Analysing incomplete data brings the risk of generating an inaccurate insights which leads to the wrong business decisions that cost the company time, effort and money.

Once I downloaded new data, I had to update my S3 bucket because it is still storing the previous version of the data i.e. the one with country data missing. I also uploaded a new manifest.json file that.points to the updated dataset name. This makes sure the QuickSight is now pulling in data from the uploaded dataset and not the version with missing data.

I initally couldn't see my updated data in QuickSight, so I had to visit the Dataset in the Dataset page in QuickSight and perform a full refresh of my data.

![Image](http://learn.nextwork.org/refreshed_amber_shy_cantaloupe/uploads/aws-analytics-quicksight_86415f4e3)

---

---
