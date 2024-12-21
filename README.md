# computer_infrastructure
## Lucia Macakova
## Overview

This repository contains my submission for assessment of  the Computer Infrastructure module.

Target is, with bash [^1], to create a  repository with requsted structure, requested files with requested content and  set up a github action that will be downloading data to repository from web page in scheduled time files with requsted name and requested content.
Assessment is devided into two sections:

1. **Tasks** - a series of task to create the repository
2. **Project** - the github action

## Tasks: 

#### **Task 1: Create Directory Structure**
Using the command line, create a directory (a folder) named 'data' at the root of repository. Inside 'data', create two subdirectories: 'timestamps' and 'weather'.

#### **Task 2: Timestamps**
Navigate to the data/timestamps directory. Use the 'date' command to output the current date and time, appending the output to a file named now.txt. Repeat this step ten times, then use the 'more' command to verify what is written in now.txt.

### **Task 3: Formatting Timestamps**
Use 'date' command to output date in format of YYYYmmdd_HHMMSS. Refer to the date 'man page' (using  command 'man date') to see formatting options. Append the formatted output to a file named 'formatted.txt'

### **Task 4: Create Timestamped Files**
Use the 'touch' command to create an empty file with a name in the 'YYYYmmdd_HHMMSS.txt' format.

### **Task 5: Download Today's Weather Data**
Change to the data/weather directory. Download the latest weather data for the Athenry weather station from https://prodapi.metweb.ie/observations/athenry/today using 'wget' command. Use the -O <filename> option to save the file as 'weather.json'.

### **Task 6: Timestamp the Data**
Modify the command from Task 5 to save the downloaded file with a timestamped name in the format 'YYYYmmdd_HHMMSS.json'.

### **Task 7: Write the Script**
Write a bash script called 'weather.sh' in the root of your repository. This script will automate the process from Task 6, saving the weather data to the data/weather directory. Make the script executable and test it by running it.

### **Task 8: Notebook**
Create a notebook called 'weather.ipynb' at the root of your repository. In this notebook, write a brief report explaining how you completed Tasks 1 to 7. Provide short descriptions of the commands used in each task and explain their role in completing the tasks.

### **Task 9: pandas**
In your 'weather.ipynb' notebook, use the 'pandas function read_json()' to load in any one of the weather data files you have downloaded with your script. Examine and summarize the data. Use the information provided data.gov.ie to write a short explanation of what the data set contains.

---

## Project

### Steps:
1. **Create GitHub Actions Workflow**:  
   Added a 'weather-data.yml' file under '.github/workflows'`.

2. **Schedule Workflow**:  
   Configured the workflow to run daily at time you choose, using the 'schedule' event with 'cron'[^2]. Added the 'workflow_dispatch'[^3] event for manual testing.

3. **Use Linux Virtual Machine**:  
   Specified an Ubuntu virtual machine[^4] for the workflow.

4. **Clone Repository**:  
   Included a step to clone[^5] the repository in the workflow.

5. **Execute weather.sh Script**:  
   Configured the workflow to run weather.sh [^6].

6. **Commit and Push Changes**:  
   Set up steps to commit new weather data and push changes back to the repository.

7. **Test the Workflow**:  
   Tested the workflow to ensure it ran as expected and confirmed new data was committed and pushed successfully.

---
Resources:
[^1]: https://www.geeksforgeeks.org/bash-scripting-introduction-to-bash-and-bash-scripting/
[^2]: https://crontab.guru
[^3]: https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows#workflow_dispatch
[^4]: https://en.wikipedia.org/wiki/Ubuntu
[^5]: https://github.com/actions/checkout
