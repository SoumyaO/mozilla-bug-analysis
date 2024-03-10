# Mozilla Project Bug Analysis

[Code](https://github.com/SoumyaO/mozilla-bug-analysis/tree/main/code) | [Report](https://github.com/SoumyaO/mozilla-bug-analysis/blob/main/Report_final%20coursework_SMM695_Group%209.pdf) | [ERD](https://github.com/SoumyaO/mozilla-bug-analysis/blob/main/ERD.png)


### Contributors
[Linh Nguyen](https://github.com/jill-data)  
[Soumya Ogoti](https://github.com/SoumyaO)  
[Wenxu Tian](https://github.com/Wayne599)  
[Chuqiao Xiao](https://github.com/XShawn1)  
[Yuanheng Li](https://github.com/lyh1068)


## Description
The goal of this project was to store, manipulate and analyze bug data for the Mozilla project.

### Database design
PostgreSQL and Python were used to clean and structure the bug data into a well defined database. The database was structured to contain all the bug reports in a *reports* table which is the primary table containing essential infformation containing each bug from the dataset. Users were assigned to another *users* table . A *changes history* table was used to keep track of historical modifications made to the bug reports. A *customer fields* table allows for storage of additional customer fields related to specific bug reports. A *flags table* has information about various flags in the bug reports whereas the *comments* table stores the comments and discussions made on specific bug reports.

These other four tables including changes_history, customer_fields, flags, and comments have their foreign key constraints established to reference the primary key (bug_id) in the reports table.

### Descriptive statistics Analysis for insights

To gain insights into the Bugzilla bugs key metrics and enable informed decision-making for bug prioritisation, resource allocation and quality information, descriptive statistics analysis using **psycopg2** was performed and visualised using **matplotlib** & **seaborn** libraries. Analysis at bug level included quantifying and visualising the total number of bugs at product level, distribution of bugs by severity and priority per product, observing the average time of resolution of bugs at various levels (severity, priority,resolution time) and more. To understand the level of engagement, comment analysis was done such as number of comments per bug per product, comment vs. resolution time, count of comments per commenters, correlation between votes and comment count. To understand how bugs are dependant on each other, plotted the histogram of the number of dependencies for each bug. User analysis included studying different user roles and their relation to bugs(developer, QA, CC), ratio of developer in charge to bugs, temporal analysis of bug status changes(unconfirmed, resolved, verified..).
