
## This all-in-one solution is designed to be ran by ANYONE.

**This is the local Report/Model Version. If looking for the version that leverages the Power BI Service and REST API across all Workspaces, check out here: https://github.com/chris1642/Power-BI-Backup-Impact-Analysis-Governance-Solution**

- Everything within the script is limited to your access within the Power BI environment.
- All computer requirements are at the user level and do not require admin privileges.
- There are ZERO pre-reqs. It's as simple as downloading this repo into C:\Power BI Backups, opening Powershell, and running the included 'Final PS Script'

# Power BI Governance & Impact Analysis Solution

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


### 1. Model Metadata Extract
- Saves exported models in a structured folder hierarchy based on model names.
- Leverages Tabular Editor 2 and C# to extract the metadata and output within an Excel File.
<img width="695" alt="image" src="https://github.com/user-attachments/assets/c3e021b8-6dfe-40c9-bfa5-b9d4471a8fa3">

### 2. Report Metadata Extract
- Leverages Tabular Editor 2 and C# to extract the Visual Object Layer metadata and output within an Excel File (credit to @m-kovalsky for initial work on this)
- <img width="554" alt="image" src="https://github.com/user-attachments/assets/cf88aac7-6f32-445a-96c7-6bc36fcab9aa">

### 3. Model Connection Details Metadata Extract
- Leverages Power BI REST API to gather all model connection details.
- Exports the extracted metadata into the same structured excel workbook as the Power BI Environment Information Extract
- You must have read permissions on the related model.

### 4. Final Power BI Governance Model
- Combines extracts into a Semantic Model to allow easy exploring, impact analysis, and governance of all Power BI Reports and Models.
- Works for anyone who runs the script and has at least 1 model and report.
- Public example (limited due to no filter pane): https://app.powerbi.com/view?r=eyJrIjoiNmMxYWQ2ZTItZDM4ZS00MGM1LTlhMDQtN2I1OTMwMzI0OTg2IiwidCI6ImUyY2Y4N2QyLTYxMjktNGExYS1iZTczLTEzOGQyY2Y5OGJlMiJ9

## Screenshots of Final Output
..
..

<img width="1235" alt="image" src="https://github.com/user-attachments/assets/805d3145-8290-4d84-8da2-bb27529bb050">
<img width="1259" alt="image" src="https://github.com/user-attachments/assets/54212360-8d0f-44c5-9337-db2cdd0fb5ee">
<img width="1259" alt="image" src="https://github.com/user-attachments/assets/9280e350-8714-40e5-8e09-d1de07faf5f5">
<img width="1221" alt="image" src="https://github.com/user-attachments/assets/e120c1bb-b52a-4197-aeb3-2a6ddbb67a9f">
<img width="1221" alt="image" src="https://github.com/user-attachments/assets/c9f5331d-8976-4f66-be76-5628e38e8d0f">
<img width="1241" alt="image" src="https://github.com/user-attachments/assets/9d814034-494d-478b-b231-f759d7eebeab">
