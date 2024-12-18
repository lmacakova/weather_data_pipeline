# computer_infrastructure
## Overview

This repository contains my submission for the Computer Infrastructure module assessment. It demonstrates my ability to utilize, configure, and script in a command-line environment, manipulate and move data using the command line, compare software infrastructures and architectures, and select appropriate computational infrastructure for specific tasks.

The assessment is divided into two key components:
2. **Tasks**: A series of command-line tasks (40%).
3. **Project**: Automation using GitHub Actions (40%).

---

## Repository Structure

. ├── data/ │ ├── timestamps/ │ ├── weather/ ├── .github/ │ └── workflows/ │ └── weather-data.yml ├── weather.sh ├── weather.ipynb └── README.md

markdown
Kopírovať kód

---

## Tasks

### **Task 1: Create Directory Structure**
Using the command line, I created a `data` directory at the root of the repository. Inside `data`, I added two subdirectories: `timestamps` and `weather`.

### **Task 2: Timestamps**
In the `data/timestamps` directory, I used the `date` command to output the current date and time into `now.txt`. By repeating this process ten times and using the `>>` operator, I ensured that new entries were appended rather than overwriting the file. The `more` command was then used to verify the contents.

### **Task 3: Formatting Timestamps**
I formatted the `date` output into the `YYYYmmdd_HHMMSS` format and appended it to a new file called `formatted.txt`. This required referring to the `man date` documentation for formatting options.

### **Task 4: Create Timestamped Files**
I used the `touch` command with an embedded `date` command to create empty files named with a timestamp in the `YYYYmmdd_HHMMSS.txt` format.

### **Task 5: Download Today's Weather Data**
In the `data/weather` directory, I downloaded the latest weather data for the Athenry weather station using `wget` with the `-O` option to save it as `weather.json`.

### **Task 6: Timestamp the Data**
I modified the `wget` command to include a timestamped filename in the `YYYYmmdd_HHMMSS.json` format, ensuring that data downloads were uniquely named.

### **Task 7: Write the Script**
I wrote a Bash script, `weather.sh`, to automate the process of downloading and timestamping the weather data. The script was made executable using `chmod +x weather.sh`.

### **Task 8: Notebook**
I documented my work in `weather.ipynb`, providing an explanation of each task. The notebook also demonstrates the use of the `pandas` library to read and analyze a weather data file.

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
