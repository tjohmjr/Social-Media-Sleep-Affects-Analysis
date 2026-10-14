# Social-Media-Sleep-Affects-Analysis
Which social media platform hurts student sleep most, and at which academic level? A Python analysis of 4,500 student survey responses using a custom Sleep Harm Index.

Approach
Data: 4,500 rows, with no missing values and no duplicate student IDs. Columns used: Academic_Level, Primary_Platform, Daily_Usage_Hours, Sleep_Duration_Hours, Sleep_Quality_Score, Late_Night_Usage.
Sleep Harm Index: a composite metric built from the z-scores of sleep duration, sleep quality and late-night usage. Duration and quality are flipped so that higher always means worse. An index of 0 is an average student.
Analysis steps:
Correlate daily usage with sleep duration and quality.
Compare platforms within each academic level, using only groups with n ≥ 30 to avoid misleading small samples.
Compare academic levels against each other.
Visualizations: scatter plots with trend lines, Sleep Harm Index by platform within each level, and a comparison of the levels.
Key Findings
Usage hours matter most. Daily social media hours correlate strongly with less sleep (r = −0.72) and worse sleep quality (r = −0.68). This is a stronger predictor than platform.
Worst platform differs by level. Instagram for high school, Reddit for undergraduates and YouTube for postgraduates. The margins are small, only a few hundredths of a standard deviation, so no platform clearly stands out.
High school students have the worst sleep overall. They have the shortest sleep (6.68 h), the lowest quality (2.44) and the highest harm index. The gap between levels is small, only about 4 minutes of sleep.
TikTok sits near average at every level.
Limitations

The data is a one-time, self-reported survey, so it shows association but not causation. Heavy scrolling may cost sleep, or poor sleepers may scroll more.

Tech Stack:
Python, pandas, NumPy, SciPy, matplotlib, seaborn, Jupyter Notebook

Repo structure:

├── Report1Analysis.ipynb                      # Full analysis notebook
├── Social_media_impact_on_life.csv            # Dataset (Kaggle)
└── SocialMediaSleepAnalysisReport_Travis_Ohm.docx   # Written report

Usage:

Download the dataset from Kaggle and put it in the same folder as the notebook, if it isn’t already included.
Install the dependencies: pip install pandas numpy scipy matplotlib seaborn jupyter
Open Report1Analysis.ipynb and run all cells.
