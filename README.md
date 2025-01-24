# NBADataLake
This repository contains a script which automates the creation of a data lake for NBA analytics using AWS services. The script integrates Amazon S3, AWS Glue, and Amazon Athena, and sets up the infrastructure needed to store and query NBA-related data.

# Overview
The setup_nba_data_lake.py script performs the following actions:
- Creates an Amazon S3 bucket to store raw and processed data.
- Uploads sample NBA data (JSON format) to the S3 bucket.
- Creates an AWS Glue database and an external table for querying the data.
- Configures Amazon Athena for querying data stored in the S3 bucket.

## Technical Architecture
![AWS](https://github.com/PreciousDipe/NBADataLake/blob/main/nba.drawio.svg)

# START HERE 
## 1. Clone Repository from GitHub

```bash
git clone https://github.com/PreciousDipe/NBADataLake.git
cd NBADataLake
```

## 2. Create and Activate a Virtual Environment

```bash
# Create a virtual environment named 'aws'
python3 -m venv aws

# Activate the virtual environment
source ./aws/bin/activate
```
## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

# Step 4: Create .env file
1. In the CLI (Command Line Interface), type
```bash
nano .env
```
2. paste the following line of code into your file, ensure you swap out with your API key
```bash
SPORTS_DATA_API_KEY=your_sportsdata_api_key
NBA_ENDPOINT=https://api.sportsdata.io/v3/nba/scores/json/Players
```

3. Press ^X to exit, press Y to save the file, press enter to confirm the file name 


# Step 5: Run the script
1. In the CLI type
```bash
python3 setup_nba_data_lake.py
```

### **What We Learned**
1. Securing AWS services with least privilege IAM policies.
2. Automating the creation of services with a script.
3. Integrating external APIs into cloud-based workflows.
