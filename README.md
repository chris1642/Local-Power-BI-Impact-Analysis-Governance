
# Local Power BI Governance & Impact Analysis Solution

*This is the local Report/Model Version. If looking for the version that leverages the Power BI Service and REST API across all Workspaces, check out: https://github.com/chris1642/Power-BI-Backup-Impact-Analysis-Governance-Solution*

- All computer requirements are at the user level and do not require admin privileges.
- There are ZERO pre-reqs. It's as simple as downloading this repo into C:\Power BI Backups, placing your local files in the dedicated folder, opening Powershell, and running the included 'Final PS Script'

## What It Does
This provides a quick and automated way to identify where and how specific fields, measures, and tables are used across your local Power BI reports by analyzing the visual object layer. It also breaks down the details of your models and report for easy review, including full measure lineage, giving you an all-in-one **Power BI Governance** solution.

### Key Features:
- **Impact Analysis**: Fully understand the downstream impact of data model changes, ensuring you don’t accidentally break visuals or dashboards—especially when reports connected to a model span multiple workspaces.
- **User-Friendly Output**: Results are presented in a Power BI model, making them easy to explore, analyze, and share with your team.

     .

     .

## Instructions:

1. Create a new folder on your C: drive called 'Power BI Backups' (C:\Power BI Backups).
2. Download contents of this repo and place in C:\Power BI Backups folder. The contents of the Config folder should be at C:\Power BI Backups\Config
3. Place the PBIX files you're looking to break down and analyze within: C:\Power BI Backups\Local Reports and Models
4. Open PowerShell and run 'Final PS Script' (either via copy/paste or renaming the format from .txt to .ps1 and executing).
5. Once complete, open 'Local Power BI Governance Model.pbit' and the model will refresh with your data. All relationships, Visuals, and Measures are set up. Save as PBIX.


     .

     .

- ** If any modules are required within PowerShell, PowerShell will request to install (user level, no admin access required) **
- ** This includes the portable version of Tabular Editor 2 v2.25.0 (https://github.com/TabularEditor/TabularEditor - MIT License). This no longer requires having it preinstalled, as it will run from the portable version with no differences. ** 
- ** For users of the commercial/enterprise Tabular Editor 3, Tabular Editor 2 is still required. TE3 does not have a command line interface feature **
- ** If you see a refresh error in the Power BI Governance Model Template along the lines of "Query XXXXXX references other queries or steps, so it may not directly access a data source. Please rebuild this data combination", this is related to the privacy settings within Power BI Desktop. To resolve, go to: File -> Options and settings -> Options -> Privacy (under Global) -> change to EITHER "Combine data according to each file's Privacy Level settings" or "Always Ignore Privacy Level Settings". The template model file is set to ignore privacy settings for the excel files - but requires that the global privacy settings are either per file or always ignored. **


## Features


### 1. Model Metadata Extract - Measure Lineage, Used/Unused Objects
- Saves exported models in a structured folder hierarchy based on model names.
- Leverages Tabular Editor 2 and C# to extract the metadata and output within an Excel File.

### 2. Report Metadata Extract - Impact Analysis, Objects Usage - Where and How Often
- Leverages Tabular Editor 2 and C# to extract the Visual Object Layer metadata and output within an Excel File (credit to @m-kovalsky for initial work on this)

### 4. Final Power BI Governance Model
- Combines extracts into a Semantic Model to allow easy exploring, impact analysis, and governance of all Power BI Reports and Models.
- Works for anyone who runs the script and has at least 1 model and report.
- Public example (limited due to no filter pane): https://app.powerbi.com/view?r=eyJrIjoiMTA4YzFjYjctYjJjZC00Yjk5LWEwNGItODY4MjNlYTUyNWQwIiwidCI6ImUyY2Y4N2QyLTYxMjktNGExYS1iZTczLTEzOGQyY2Y5OGJlMiJ9

## Screenshots of Final Output
..
..

<img width="1235" alt="image" src="https://github.com/user-attachments/assets/cd3d736d-a56b-4ff0-a1af-475ac149bc79">
<img width="1259" alt="image" src="https://github.com/user-attachments/assets/89749b7a-a62a-4f89-94a9-2f922e66e47d">
<img width="1259" alt="image" src="https://github.com/user-attachments/assets/d015863b-3136-4caa-85ae-1026d90ef338">
<img width="1221" alt="image" src="https://github.com/user-attachments/assets/e683f8ec-2341-46d5-a93b-5511ec8bfb17">
<img width="1221" alt="image" src="https://github.com/user-attachments/assets/db909853-4d5c-4024-82dc-b9552a82082a">
