# 📊 Grafana Transaction Monitoring

## 🔍 Overview
[Linkedin Video Link](https://www.linkedin.com/posts/dewasahu_grafana-aws-postgresql-activity-7295869490007871488-y85D?utm_source=share&utm_medium=member_desktop) 

This project integrates Grafana with an AWS RDS PostgreSQL database for monitoring real-time transactions. It includes a Python script that generates synthetic transaction data, applies simple fraud detection rules for understanding, and stores the data in a PostgreSQL database hosted on AWS.

## 🚀 Features

- 🔄 Generates synthetic financial transactions using `Faker`
- ⚠️ Applies simple fraud detection rules based on transaction attributes
- 🗄️ Stores transaction data in AWS RDS (PostgreSQL)
- 📊 Designed for integration with Grafana for visualization
- ⏳ Updates in real-time when new transaction data is added to the database

## 🛠️ Setup Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/dewasahu2003/grafana_testing.git
cd grafana_testing
```

### 2️⃣ Create a Virtual Environment

```bash
python3 -m venv venv
venv/Scripts/activate #source venv/bin/activate for mac,linux
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Configure AWS RDS Connection

- ☁️ Create an AWS RDS PostgreSQL instance.
- 🔑 Retrieve the **host endpoint** from AWS RDS.
- 📝 Ensure the connection settings in the script are updated with the correct host.

### 5️⃣ Run the Transaction Generator Script

```bash
run app.ipynb
```

**⚠️ Note**: The script runs continuously to generate fake transaction data. Stop it manually when testing is complete.

### 6️⃣ Set Up Grafana Dashboard

- 🏗️ Login to Grafana
- 🔗 Configure PostgreSQL as a data source.
- 📈 Create a dashboard to visualize transaction data.

## 🔎 Insights & Considerations

- 🔒 **Security**: Never expose your RDS credentials publicly.
- ⚡ **Performance**: Optimize indexing in PostgreSQL for faster queries.
- 🔔 **Alerting**: Use Grafana alerts for anomaly detection in transactions.
- 🎓 **Understanding**: The fraud detection rules in this project are basic and meant for learning purposes.
- ⏱️ **Real-time Updates**: Grafana will automatically update when new data is added to the database, ensuring live monitoring of transactions.

For more details, check the [Grafana documentation](https://grafana.com/docs/).

