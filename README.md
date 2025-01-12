
# Capstone Project: STIX Graph for Cyber Incidents

## Overview

This repository contains the code developed as part of a capstone project in collaboration with the National Security Agency (NSA). Our work builds on a previous semester's capstone project, which developed the website frontend and backend to display STIX graphs. This semester, we focused on extending the system by developing code to generate synthetic STIX-compatible data, stored as CSV files, which are displayed on the website to visualize cyber incidents.

## Key Features

- **STIX Data Generation**: Generates synthetic data for various STIX domains such as Campaigns, Groupings, Indicators, and Intrusion Sets.
- **Integration with MITRE Data**: Synthetic data generation is informed by real-world cyber threat intelligence from the MITRE framework.
- **Graph Visualization**: Output CSV files are compatible with the existing website for dynamic STIX graph visualization of cyber incidents.
- **Flexible Data Modeling**: Leverages LangChain and OpenAI to create detailed, structured threat intelligence data.

## Project Details

### Collaboration

- **Partners**: National Security Agency (NSA)
- **Team Structure**: Led by myself and one other co-leader, with weekly meetings involving the professor and NSA representatives.
- **Previous Work**: The prior semester developed the frontend and backend for the STIX graph visualization website.

### Technologies

- **Python Libraries**: `langchain`, `pandas`, `openai`
- **Data Formats**: STIX 2.1, CSV
- **Visualization**: Integration with a web application to display STIX graphs.

### Synthetic Data Generation

The synthetic data generation code focuses on four key STIX domains:
1. **Campaigns**: Represents coordinated cyber activities with attributes like objectives, aliases, and timelines.
2. **Groupings**: Organizes related objects under a unified context, such as threat reports or attack patterns.
3. **Indicators**: Defines patterns of malicious activity, such as IP addresses or domain names.
4. **Intrusion Sets**: Describes persistent adversaries and their tactics, techniques, and procedures (TTPs).

Generated data adheres to the STIX 2.1 standard and includes unique identifiers, timestamps, and detailed descriptions.

## Usage

1. **Installation**: Install required Python libraries:
   ```bash
   pip install -U langchain langchain_experimental openai pandas
   ```

2. **Set Up Environment Variables**:
   Add your OpenAI API key to your environment:
   ```python
   import os
   os.environ["OPENAI_API_KEY"] = "your_openai_api_key_here"
   ```

3. **Run the Code**:
   Execute the scripts to generate synthetic data. Each script outputs a CSV file:
   - `campaign_data.csv`
   - `grouping_data.csv`
   - `indicator_data.csv`
   - `intrusion_set.csv`

4. **Visualize the Data**:
   Upload the CSV files to the existing website to display STIX graphs.

## Repository Structure

```
├── campaigns.py       # Generates synthetic Campaign data
├── groupings.py       # Generates synthetic Grouping data
├── indicators.py      # Generates synthetic Indicator data
├── intrusion_sets.py  # Generates synthetic Intrusion Set data
├── requirements.txt   # Required Python packages
├── README.md          # Project documentation
```

## Example Outputs

Here’s a sample of generated STIX data for the `Campaign` domain:

| Type       | Name               | Description                                                                                 | First Seen             | Last Seen              |
|------------|--------------------|---------------------------------------------------------------------------------------------|------------------------|------------------------|
| campaign   | Emerald Typhoon    | A sophisticated cyber espionage operation focusing on geopolitical intelligence gathering.  | 2022-11-10T09:30:45Z  | 2023-01-20T11:45:30Z  |

## Future Work

- Enhance the data generation process with more advanced GPT models for improved realism.
- Expand the STIX domains supported in the system.
- Collaborate further with the NSA to refine threat intelligence insights.

## Acknowledgments

This project was supported by:
- The **National Security Agency (NSA)** for guidance and collaboration.
- Our **professor** for mentorship throughout the project.
- The prior semester’s capstone team for developing the frontend and backend of the STIX visualization system.
