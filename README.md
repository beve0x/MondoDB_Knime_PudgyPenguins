# MongoDB_Knime_PudgyPenguins
# Pudgy Penguins Merchandise Impact Analysis
Analysis of Pudgy Penguins Merchandise Impact on NFT Sales
This repository contains a KNIME workflow that analyzes the impact of Pudgy Penguins merchandise launch on their NFT sales. The analysis is based on data extracted from a blockchain analytics platform, processed in KNIME, and visualized to interpret market trends.

## Workflow Version
KNIME Analytics Platform 5.1.2

# Description
Utilized the KNIME analytics platform to extract data from MongoDB, which is filled with data obtained from a blockchain analytics API. The workflow processes the data to derive insights and visualize the outcomes, revealing the influence of merchandise on NFT sales.


# Workflow Overview
Data Extraction:
The data was extracted using Flipside Crypto's API with SQL queries to retrieve NFT sales data. The dataset was then converted into a Pandas DataFrame and inserted into MongoDB for further processing in KNIME.

Multiple MongoDB Connector nodes connect to MongoDB, each targeting different datasets.
MongoDB Reader nodes fetch the data from MongoDB.
JSON to Table nodes convert the JSON data from MongoDB into a tabular format for further analysis.
Data Integration:

Joiner nodes merge the tables on specified keys to create a comprehensive dataset.
Data Cleaning:

Duplicate Row Filter removes any duplicate records to ensure data quality.
String to Date/Time node standardizes the format of date/time data.
Data Segregation:

Rule-based Row Splitter nodes split the data based on predefined rules, likely to compare datasets before and after the merchandise launch.
Data Analysis:

Grouping and aggregating data based on specific attributes using GroupBy nodes.
Identifying and separating high-level trade transactions using Top k Row Filter.
Visualization:

A variety of nodes, including Line Plot, Pie Chart, and Bar Chart nodes, to visualize different aspects of the data, such as sales volume, number of transactions, and individual trader activity.
# How to Run
Ensure you have the correct version of KNIME installed and that MongoDB is running and accessible.

Open the KNIME workflow.
Configure MongoDB connectors with appropriate connection details.
Execute the workflow step-by-step to retrieve, process, and analyze the data.
View or export the generated visualizations.
# Tools Used
KNIME Analytics Platform
MongoDB
Methodology
MongoDB Data Extraction
SQL - noSQL queries are constructed to retrieve the desired datasets from MongoDB.
Data is extracted in JSON format and then converted to tabular format for analysis.
# Data Analysis
The workflow segregates data based on the merchandise launch date for comparative analysis.
Key metrics such as trading volume, number of NFTs transacted, and average ETH price are computed.
Trends are identified to assess the impact of the merchandise launch on the sales of the NFTs.
# Data Visualization
Visual representations are created to better understand trends and patterns in the data.
These include line plots to show changes over time, pie charts for distribution analysis, and bar charts to highlight top trader activity.
# Results
The analysis showed a significant increase in trading volume and number of NFTs transacted post merchandise launch, indicating a possible positive impact of the merchandise on NFT sales.
# How to Run the Workflow
Ensure MongoDB is running and accessible.
Open the KNIME workflow and configure MongoDB connectors with appropriate connection details.
Execute the workflow step-by-step to retrieve, process, and analyze the data.
View visualizations generated within KNIME or export them for reporting purposes.
# Conclusion
This KNIME workflow demonstrates a structured approach to analyzing the influence of merchandise on digital collectibles' sales. Although increased trading activity around the launch suggests a correlation, further research is warranted to establish causation.
