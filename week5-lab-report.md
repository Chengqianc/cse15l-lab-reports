# Week 3 Lab Report

## find command

### find . -type d
```
chengqian@Chengs-MacBook-Air skill-demo1 % find . -type d
.
./lib
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
```
This command recursively searches for all the directories inside the current working directory and prints them all out one by one.

```
chengqian@Chengs-MacBook-Air skill-demo1 % find ./technical/government -type d
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
```
This command recursively searches for all the directories inside the direcory ./technical/government and prints them all out one by one.

```
chengqian@Chengs-MacBook-Air skill-demo1 % find ./technical -type d
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
```
This command recursively searches for all the direcotries inside the directory ./technical and prints them all out one by one.

### find . -type f -size -1024c
```
chengqian@Chengs-MacBook-Air skill-demo1 % find . -type f -size -1024c
./README.md
./test.sh
./start.sh
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
```
This command recursively searches for all files inside the curretn working directory that have less than 1024 characters and prints them all out one by one.

```
chengqian@Chengs-MacBook-Air skill-demo1 % find ./technical  -type f -size -1024c
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
```
This command recursively searches for all files inside the ./technical directory that have less than 1024 characters and prints them all out one by one.

```
chengqian@Chengs-MacBook-Air skill-demo1 % find ./technical  -type f -size -2048c
./technical/government/Media/Helping_Hands.txt
./technical/government/Media/Campaign_Pays.txt
./technical/government/Media/Fire_Victims_Sue.txt
./technical/government/Media/Court_Keeps_Judge_From.txt
./technical/government/Media/It_Pays_to_Know.txt
./technical/government/Media/Self-Help_Website.txt
./technical/government/Media/Justice_requests.txt
./technical/government/Media/Wilmington_lawyer.txt
./technical/government/Media/Lawyer_Web_Survey.txt
./technical/plos/pmed.0020048.txt
./technical/plos/pmed.0020028.txt
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
./technical/plos/pmed.0020192.txt
./technical/plos/pmed.0020157.txt
./technical/plos/pmed.0020082.txt
./technical/plos/pmed.0020120.txt
```
This command recursively searches for all files inside ./technical directory that have less than 2048 characters and prints them all out one by one.

### find ./technical/911report -name "*.txt"
```
chengqian@Chengs-MacBook-Air skill-demo1 % find ./technical/911report -name "*.txt"
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```
This command recursviely searches for files inside the ./technical/911report direcotry that have .txt extensions and prints them all out one by one.

```
chengqian@Chengs-MacBook-Air skill-demo1 % find ./technical/government/Alcohol_Problems  -name "*.txt" 
./technical/government/Alcohol_Problems/Session2-PDF.txt
./technical/government/Alcohol_Problems/Session3-PDF.txt
./technical/government/Alcohol_Problems/DraftRecom-PDF.txt
./technical/government/Alcohol_Problems/Session4-PDF.txt
```
This command recursively searches for files inside ./technical/government/Alcohol_Problems directory that have .txt extensions and prints them all out one by one.

```
chengqian@Chengs-MacBook-Air skill-demo1 % find .  -name "*.java" 
./DocSearchServer.java
./Server.java
./TestDocSearch.java
```
This command recursively searches for files inside current working directory that have .java extensions and prints them all out one by one.