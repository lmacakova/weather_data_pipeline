# computer_infrastructure
## Lucia Macakova
## Overview

This repository contains my submission for assessment of  the Computer Infrastructure module. 
The assessment is divided into two key components:
1. **Tasks**
2. **Project**

## Tasks: 

### **Task 1: Create Directory Structure**
Create a 'data' directory at the root of the repository. Inside 'data', create two subdirectories: 'timestamps' and 'weather'.

### **Task 2: Timestamps**
In the 'data/timestamps' directory, create file 'now.txt' with 11 timestamps of current time.

### **Task 3: Formatting Timestamps**
In the 'data/timestamps' directory create a file 'formatted.txt' containing currrent date in YYYYmmdd_HHMMSS format.

### **Task 4: Create Timestamped Files**
In the 'data/timestamps' directory create an empty file named with a timestamp in the YYYYmmdd_HHMMSS.txt format.

### **Task 5: Download Today's Weather Data**
In the 'data/weather directory', download the latest weather data for the Athenry weather station in https://prodapi.metweb.ie/observations/athenry/today, and save it as 'weather.json'.

### **Task 6: Timestamp the Data**
Download data from  https://prodapi.metweb.ie/observations/athenry/today into a file with timestamped name, in the YYYYmmdd_HHMMSS.json format.

### **Task 7: Write the Script**
Write a Bash script, 'weather.sh', to automate the process of downloading and timestamping files from https://prodapi.metweb.ie/observations/athenry/today. Make it executable.

### **Task 8: Notebook**
Document your work in 'weather.ipynb', providing an explanation of each task. Describe methods and commands you used.

### **Task 9: pandas**
Using the `pandas` library, I loaded a weather data file with the `read_json()` function, summarized its contents, and described the dataset based on information from data.gov.ie.

---

## Project: Automating Weather Data Collection

### Steps:
1. **Create GitHub Actions Workflow**:  
   Added a `weather-data.yml` file under `.github/workflows/`.

2. **Schedule Workflow**:  
   Configured the workflow to run daily at 10am using the `schedule` event with `cron`. Added the `workflow_dispatch` event for manual testing.

3. **Use Linux Virtual Machine**:  
   Specified an Ubuntu virtual machine for the workflow.

4. **Clone Repository**:  
   Included a step to clone the repository in the workflow.

5. **Execute weather.sh Script**:  
   Configured the workflow to run `weather.sh`.

6. **Commit and Push Changes**:  
   Set up steps to commit new weather data and push changes back to the repository.

7. **Test the Workflow**:  
   Tested the workflow to ensure it ran as expected and confirmed new data was committed and pushed successfully.

---

## Learning Outcomes

Through this assessment, I demonstrated:
- **Command-Line Proficiency**: Navigating, scripting, and manipulating data in a CLI environment.
- **Automation**: Automating tasks using Bash scripts and GitHub Actions.
- **Data Handling**: Parsing and analyzing JSON data using Python and pandas.
- **Version Control**: Utilizing Git and GitHub to track and share progress.

---

## How to Run

1. Clone this repository:
   ```bash
   git clone <repository-url>
Navigate to the root directory:
bash
Kopírovať kód
cd <repository-directory>
Run the weather.sh script:
bash
Kopírovať kód
./weather.sh
View the notebook: Open weather.ipynb in Jupyter Notebook or another compatible viewer.
Contact
For any questions, feel free to reach out via GitHub or email.

rust
Kopírovať kód

This `README.md` serves as both a comprehensive guide for the assessment and a professional
