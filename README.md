# Data Engineer Bootcamp - Data Warehouse (DWH) & Data Pipeline hackathon

## purpose
This hackathon is about realizing a small Data Warehouse (DWH) System on Azure Synapse.
- setup a DWH = a Azure Synapse instance called "lhdebootcamp2022PLACEHOLDERFORTEAMMEMBERS"
- setup required data pipelines
- integrate source data via data pipelines
    - Source Data Overview: https://opensky-network.org/ 
    - Data to integrate in the DWH https://opensky-network.org/datasets/flights_data5_develop_sample/
- Make some basic data analysis on historical data
- As showcase/outcome this data analysis should be presentable to the customer

## customer requirements

The customer wants to analyze historical flight data.
The DWH should enable the customer to answer example questions like the following:
- Which is the most frequently used flight connection to Belgium (airportofdeparture to airportofdestination)?
- Last_seen (=Departure), first_seen (=Arrival). Which aircraft had the longest stay at a specific airport (e.g. airport of Hamburg or airport of Brussels)?
- Point-in-time analysis: 
    - Which airport has the highest ranking according to the count of take-offs per day?
    - Aggregate/cumulated per 15th of September 2019: 
      How many take-offs took place per airport until the 15.09.2019? What differences according to airport ranking can be identified? 
    - How many take-offs took place per airport until today? Ranking Chart or Histogramm expected.

## tool stack
As target system your customer wishes to see the flight data in Azure Synapse. 
HINT: If Azure Synapse is not available please argue and suggest any other relational (Cloud-)database (MariaDB, MySQL, PostgreSQL).
Customer's preference: Database & corresponding infrastructure should be in a Cloud System.

## outcome
### 1x Software concept:
- Pre-Condition: Not more than 2 pages maximum / only bullet-points):
- Overview of the architecture (used systems: Source-system (External URL), Target-Sytem Azure Synapse, ...)
- A Logical Data Model (draw.io?, ...) as an Entity-Relationship Model (ERM)
- Used Data Pipeline (ETL) technology and short statement why compared to others.

### 1x Software outcome:
- Azure Synapse instance in your Azure Subscription
- A Datamodel consisting of some physical tables (and optional table views) in Azure Synapse.
- A Datapipeline which ingests the source data into Azure Synapse
- Sample Data Analysis in Azure Synapse (if not possible there then in e.g. jpyter-notebook or another tool suggestion)
-----------------------
ONLY OPTIONALS & HINTS:
- If Azure Synapse requires a pre-System (blob storage or something else)
- Technical user for your Database connection
- Usage of different permissions/roles 
    - e.g. only specific users should be allowed to view historical data VS. everyone should be able to view the current  data aggregations for today.

### ADD-ON Tasks (expected only when there is time left):
- Pre-Assumption: In case you used a specific / GUI oriented explicit Data Pipeline tool (Apache NiFi, Azure Data Factory, Azure DataBricks ...)
- Create a concept: What is needed to run your DataPipline / ETL as code only
- Try to implement your Data Pipeline as code (or create pseudo-code):
  - e.g. as python/java ETL script programm
  - e.g. as cmd/linux Data Ingestion programm
- Try to implement your Data Pipeline as Pod in Azure Kubernetes -> challenging = not expected.
- Try to implement a Data Pipeline Scheduler (e.g. cron trigger for your existing ETL "GUI" or ETL code-based job)  -> challenging = not expected.

## data
Data to be integrated in the DWH: https://opensky-network.org/datasets/flights_data5_develop_sample/
Please load all available September 2019 data. 
Hint: The customer can only check or compare your outcome gainst his current solution if you load the complete month.

## contributing
Only LHIND / Bootcamp users or participants should have access and contribute via pull/commit/push on master-branch.

### optional usage

```bash
git clone ...
```

For code based ETL or any packages (pip install) please use virtual enviroments and create a requirements.txt
```bash
python -m venv C:\Users\UXXXXXX\workspace\dataengineer_dwh_hackathon venv
```

Create the requirements.txt (with all libaries storage during coding in the venv folder)
cd Projekt_folder: cd ../workspace/dataengineer_dwh_hackathon

```bash
pip freeze > requirements.txt
```

### optional installation / reusing the code on different enviroments
Load the requirements.txt for used libraries
```bash
pip install -r requirements.txt
```

## license & wiki & sources
[LHIND Wiki: LHIND](https://confluence.lhind.de/) 

[Source data: opensky-network](https://opensky-network.org/)

