# 🚀 Smart Transportation

## 🌟 Overview
Smart Transportation is a data-driven solution designed to optimize and enhance transportation systems using advanced analytics and big data technologies. This project leverages tools such as Apache Spark and Redshift to process, analyze, and visualize large-scale transportation data, providing actionable insights for smarter decision-making.

## ✨ Features
- **Big Data Processing**: Efficiently process and analyze large transportation datasets using Apache Spark.
- **Database Integration**: Utilize AWS Redshift for scalable data storage and querying.
- **Containerized Deployment**: Simplify deployment with Docker Compose.
- **Configurable Jobs**: Modular and configurable Python scripts for various data processing tasks.

## 📂 File Structure
```
Smart-Transportation
├── LICENSE                 # Licensing information
├── README.md               # Project documentation
├── docker-compose.yml      # Docker setup for the project
├── redshift-query.sql      # SQL queries for Redshift database
├── requirements.txt        # Python dependencies
├── jobs/                   # Python scripts for data processing
│   ├── config.py           # Configuration file
│   ├── main.py             # Main job execution script
│   ├── spark-transporation.py  # Spark job for transportation data processing
│   └── __pycache__/        # Compiled Python cache files
└── .git/                   # Git repository metadata
```

## 🛠️ Technologies Used
- **Apache Spark**: For big data processing and analytics.
- **AWS Redshift**: For scalable database storage and querying.
- **Docker**: For containerization and simplified deployment.
- **Python**: For data processing scripts.
- **SQL**: For database querying and management.

## 📋 Prerequisites
To set up and run the project, ensure you have the following installed:
- 🐳 Docker
- 🐍 Python 3.11 or higher (Only this version is tested and compatible. Consider downgrading or upgrading to this version for smooth execution.)
- 🛢️ AWS Redshift (or equivalent database access)

## ⚙️ Installation

### 1. 🌐 Set up AWS Account
1. Create an AWS account by visiting [AWS Sign-Up](https://aws.amazon.com/free/).
2. Log in to your AWS Management Console.
3. Navigate to **IAM (Identity and Access Management)** to create a new user with programmatic access.
4. Attach the appropriate policies (e.g., AmazonRedshiftFullAccess).
5. Note down the **Access Key ID** and **Secret Access Key**.

### 2. 🛢️ Set up AWS Redshift
1. Go to the Redshift section in the AWS Management Console.
2. Click on **Create cluster** and configure the following:
   - **Cluster identifier**: A unique name for your cluster.
   - **Node type**: Choose the node size as per your dataset.
   - **Number of nodes**: For testing, you can start with 1.
   - **Database name**: Set the database name (e.g., `transportation_db`).
3. Wait for the cluster to be available.
4. Note down the **Endpoint** of your cluster (found in the cluster details page).
5. Configure your security group to allow connections from your machine by editing the inbound rules.

### 3. 🐳 Set up Docker
1. Install Docker by following instructions for your operating system from [Docker's website](https://www.docker.com/).
2. Verify the installation by running:
   ```bash
   docker --version
   ```

### 4. 📦 Clone the Repository
   ```bash
   git clone <repository-url>
   cd Smart-Transportation
   ```

### 5. 📋 Install Python Dependencies
   ```bash
   pip install -r requirements.txt
   ```

### 6. 🔧 Configure the Project
1. Open `jobs/config.py` and update the following fields:
   - AWS Access Key and Secret Key
   - Redshift cluster endpoint and database details
   - S3 bucket details (if using S3 for data input/output)

### 7. 🐳 Start the Docker Containers
   ```bash
   docker compose up -d
   ```

## 🚀 Usage

### ⚡ Running Spark Jobs
Run the main job script to process transportation data:
```bash
python jobs/main.py
```

### 🛢️ Querying Data
Use the `redshift-query.sql` script to query the processed data in AWS Redshift:
```sql
-- Example query
SELECT * FROM transportation_data LIMIT 10;
```

### 🐳 Docker Management
To bring up the Docker containers:
```bash
docker-compose up
```
To shut down the Docker containers:
```bash
docker-compose down
```

## 🤝 Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## 📜 License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## 📞 Contact
For any questions or support, please reach out to the contributors or open an issue in the repository.
