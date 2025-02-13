# Grafana Transaction Monitoring

## Overview

This project integrates Grafana with an AWS RDS PostgreSQL database for monitoring real-time transactions. It includes a Python script that generates synthetic transaction data, applies simple fraud detection rules for understanding, and stores the data in a PostgreSQL database hosted on AWS.

## Features

- Generates synthetic financial transactions using `Faker`
- Applies simple fraud detection rules based on transaction attributes
- Stores transaction data in AWS RDS (PostgreSQL)
- Designed for integration with Grafana for visualization

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/dewasahu2003/grafana_testing.git
cd grafana_testing
```

### 2. Create a Virtual Environment

```bash
python3 -m venv venv
venv/Scripts/activate #source venv/bin/activate for mac,linux
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure AWS RDS Connection

- Create an AWS RDS PostgreSQL instance.
- Retrieve the **host endpoint** from AWS RDS.
- Ensure the connection settings in the script are updated with the correct host.

### 5. Run the Transaction Generator Script

```bash
run app.ipynb
```

**Note**: The script runs continuously to generate fake transaction data. Stop it manually when testing is complete.

### 6. Set Up Grafana Dashboard

- Install and start Grafana.
- Configure PostgreSQL as a data source.
- Create a dashboard to visualize transaction data.

## Insights & Considerations

- **Security**: Never expose your RDS credentials publicly.
- **Performance**: Optimize indexing in PostgreSQL for faster queries.
- **Alerting**: Use Grafana alerts for anomaly detection in transactions.
- **Understanding**: The fraud detection rules in this project are basic and meant for learning purposes.

For more details, check the [Grafana documentation](https://grafana.com/docs/).

