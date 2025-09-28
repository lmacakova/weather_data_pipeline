![thunderstorm](https://images.pexels.com/photos/2258536/pexels-photo-2258536.jpeg)
# Weather Data Pipeline

---

## Overview
This project automates the collection of meteorological data and stores it in a repository. It uses Bash scripting[^1] and GitHub Actions[^2] to schedule and run the data pipeline, ensuring weather data is downloaded, timestamped, and version-controlled on a regular basis.

---

## Key Features

-  Automated Data Collection: Weather observations are fetched from Met Éireann’s API[^3].
-  Timestamps: All files are saved with timestamps (YYYYmmdd_HHMMSS) for tracking and reproducibility.
-  Data Organization: Collected data is stored under a directory structure (data/timestamps/ and data/weather/).
-  GitHub Actions Integration: A scheduled workflow runs the pipeline daily, commits new data, and pushes it back to the repository.
-  Exploration Notebook: A Jupyter notebook (weather_data_pipeline.ipynb) provides an overview of the workflow and demonstrates basic data exploration with pandas.

---

## Content:

1. Data Directories: Organized under data/ for timestamps and weather records.

2. Bash Script (weather.sh): Handles fetching and saving weather data with a timestamped filename.

3. GitHub Actions Workflow:

   -  Runs on a daily schedule via cron[^4].

   -  Executes weather.sh inside an Ubuntu[^5] VM.

   -  Commits and pushes new data back to the repository[^6].

4. Notebook Analysis: Loads a sample weather dataset with pandas, summarizes contents, and references metadata.

---

## Setup:
1. Clone the repository.
2. Make weather.sh executable:

`chmod +x weather.sh`

3. Test locally:

`./weather.sh`

4. Push changes to GitHub and verify the workflow runs as scheduled.

---

## Contact:
Lucia Macakova\
email: G00439449@atu.ie

---

## Resources:
[^1]: https://www.geeksforgeeks.org/bash-scripting-introduction-to-bash-and-bash-scripting/
[^2]: https://prodapi.metweb.ie/observations/athenry/today
[^3]: https://crontab.guru
[^4]: https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows#workflow_dispatch
[^5]: https://en.wikipedia.org/wiki/Ubuntu
[^6]: https://graphite.dev/guides/git-add-commit-push