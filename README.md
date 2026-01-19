 - https://ophelialabs.github.io/landscape/
 - https://landscape.cncf.io/
 - https://github.com/cncf/landscape2/blob/main/ADOPTERS.md

## 1. Framework Landscape
- Include relevant tools for the following frameworks(ie - spring/aspire/flask/cargo)
- Each framework should be its own category with a comprehensive list of the frameworks respective ecosystem
Java (J2EE, Spring, Flask, Server: Tomcat, UWSGI, etc)
.NET
Python
Rust
CMake
ROS
Q#
Julia

## 2. Tools Landscape
 - https://jupyterbook.org/stable/
 - https://plutojl.org/en/docs/plutopages/
 - https://raw.githubusercontent.com/ophelialabs/ophelialabs.github.io/refs/heads/main/pages/name/tools-list.html

# Unified Cloud Landscape

A comprehensive, unified landscape of major cloud providers (AWS, Azure, GCP, OCI, IBM Cloud) with 400+ services across 7 strategic categories, enabling multi-cloud comparison, migration planning, and cost optimization.

## Quick Start

### Installation

```bash
curl --proto '=https' --tlsv1.2 -LsSf https://github.com/cncf/landscape2/releases/download/v1.1.0/landscape2-installer.sh | sh
```

### Build the Landscape

```bash
cd unified-cloud-landscape
landscape2 build \
  --data-file data.yml \
  --settings-file settings.yml \
  --guide-file guide.yml \
  --logos-path logos \
  --output-dir build
```

### View the Landscape

```bash
landscape2 serve --landscape-dir build
```

Then open your browser to `http://localhost:8000`

## Structure

This unified landscape is designed for easy expansion with additional cloud providers.

### Adding a New Cloud Provider

To add a new cloud provider (e.g., Alibaba Cloud, Google Cloud):

1. **Update `data.yml`**: Add a new category with the provider's name
2. **Add 7 standard subcategories**:
   - Compute Services
   - Storage Services
   - Database Services
   - Analytics Services
   - AI/ML Services
   - Networking & Content Delivery
   - Data Integration & Migration
3. **List services** in each subcategory with descriptions and homepage URLs

This standardized structure ensures consistency across the landscape and enables meaningful cross-cloud comparisons.

### Example Format for New Provider

```yaml
- name: New Cloud Provider
  subcategories:
    - name: Compute Services
      items:
        - name: Service Name
          description: Service description
          homepage_url: https://example.com
          logo: provider.svg
          project: graduated
```

## Categories

### Cloud Providers (400+ Services)

| Cloud Provider | Total Services | Service Categories |
|---|---|---|
| **AWS** | 75+ | Compute, Storage, Database, Analytics, AI/ML, Networking & Content Delivery, Data Integration & Migration |
| **Microsoft Azure** | 90+ | Compute, Storage, Database, Analytics, AI/ML, Networking & Content Delivery, Data Integration & Migration |
| **Google Cloud Platform** | 130+ | Compute, Storage, Database, Analytics, AI/ML, Networking & Content Delivery, Data Integration & Migration |
| **Oracle Cloud Infrastructure** | 50+ | Compute, Storage, Database, Analytics, AI/ML, Networking & Content Delivery, Data Integration & Migration |
| **IBM Cloud** | 80+ | Compute, Storage, Database, Analytics, AI/ML, Networking & Content Delivery, Data Integration & Migration |

#### Service Details by Provider

**AWS (75+ Services)**
- **Compute Services** - EC2, Lambda, ECS, EKS, Lightsail, App Runner, Batch, Outposts, Wavelength, VMware on AWS
- **Storage Services** - S3, EBS, EFS, Glacier, Storage Gateway, FSx, DataSync, Backup, Snow Family
- **Database Services** - RDS, DynamoDB, Aurora, DocumentDB, Neptune, QLDB, Timestream, Redshift, DMS
- **Analytics Services** - Redshift, Athena, EMR, Kinesis, Glue, Lake Formation, QuickSight, DataBrew
- **AI/ML Services** - SageMaker, Rekognition, Comprehend, Lex, Polly, Forecast, Textract, Contact Lens
- **Networking & Content Delivery** - VPC, CloudFront, Route 53, ELB, Direct Connect, VPN, Shield, WAF
- **Data Integration & Migration** - DMS, DataSync, Transfer Family, AppFlow, Ground Station

**Microsoft Azure (90+ Services)**
- **Compute Services** - Virtual Machines, App Service, Functions, Container Instances, AKS, Batch, Service Fabric, VMware Solution
- **Storage Services** - Blob Storage, Managed Disks, File Shares, Data Lake Storage, NetApp Files, Archive Storage
- **Database Services** - SQL Database, Cosmos DB, MySQL, PostgreSQL, Redis Cache, SQL Managed Instance
- **Analytics Services** - Synapse Analytics, Data Factory, Stream Analytics, Databricks, HDInsight, Power BI, Purview
- **AI/ML Services** - Azure ML, Cognitive Services, Azure OpenAI, Bot Service, Computer Vision, Speech Services, Translator
- **Networking & Content Delivery** - Virtual Network, Load Balancer, Application Gateway, ExpressRoute, VPN Gateway, Firewall, Front Door
- **Data Integration & Migration** - Data Factory, Stream Analytics, Event Hubs, Service Bus, Synapse Link

**Google Cloud Platform (130+ Services)**
- **Compute Services** - Compute Engine, GKE, Cloud Run, App Engine, Cloud Functions, Bare Metal, VMware Engine
- **Storage Services** - Cloud Storage, Persistent Disk, Cloud Filestore, Local SSD
- **Database Services** - Cloud SQL, Firestore, BigQuery, Cloud Bigtable, Cloud Spanner, Cloud Memorystore
- **Analytics Services** - BigQuery (+ BI Engine, ML, GIS), Dataflow, Dataproc, Cloud Composer, Pub/Sub, Looker, Data Studio
- **AI/ML Services** - Vertex AI (+ 15+ components), AutoML, Speech-to-Text, Vision API, Document AI, Dialogflow, Contact Center AI
- **Networking & Content Delivery** - VPC, Cloud Load Balancing, Cloud CDN, Cloud Armor, Direct Peering, Cloud Interconnect, Cloud VPN
- **Data Integration & Migration** - Dataflow, Datastream, Cloud Data Fusion, Database Migration Service

**Oracle Cloud Infrastructure (50+ Services)**
- **Compute Services** - Compute Instances, Container Engine, Functions, Bare Metal, Exadata Cloud Service
- **Storage Services** - Object Storage, Block Volumes, File Storage, Archive Storage, Data Transfer Service
- **Database Services** - Autonomous Database, Autonomous Data Warehouse, MySQL Database, PostgreSQL Database, NoSQL
- **Analytics Services** - Big Data Service, Streaming, Analytics Cloud, Hadoop Distribution, Spark Clusters
- **AI/ML Services** - Generative AI Service, Data Science, Machine Learning, Vision AI, Language Processing, Digital Assistant
- **Networking & Content Delivery** - Virtual Cloud Network, Load Balancer, FastConnect, VPN Connect, CDN, Service Gateway
- **Data Integration & Migration** - GoldenGate, Data Pump, Dataflow, Event Streaming, Service Connector Hub

**IBM Cloud (80+ Services) - NEW**
- **Compute Services** - Virtual Servers, Cloud Functions, Code Engine, OpenShift, Bare Metal, Power Virtual Servers
- **Storage Services** - Cloud Object Storage, Block Storage, File Storage, Backup & Restore, Aspera
- **Database Services** - Db2, Cloudant, MongoDB, PostgreSQL, MySQL, Data Warehouse
- **Analytics Services** - Db2 Warehouse, Streaming Analytics, Watson Studio, Planning Analytics, Cognos Analytics
- **AI/ML Services** - Watson AI, Watson Machine Learning, NLU, Computer Vision, Speech Services, Assistant, OpenScale
- **Networking & Content Delivery** - VPC, Load Balancer, Direct Link, Transit Gateway, CDN, Internet Services
- **Data Integration & Migration** - Db2 Replication, Cloud Pak for Data, Event Streams, MQ

### Cross-Cloud Services
- **Multi-Cloud Networking** - VPCs, Load Balancing, DNS/CDN
- **Multi-Cloud Security** - IAM, Encryption, Compliance
- **Multi-Cloud Analytics** - Data Warehousing, Streaming, ML
- **Integration & DevOps** - CI/CD, IaC, Monitoring

## Features

✅ **Comprehensive Coverage** - 400+ services from 5 cloud providers (AWS, Azure, GCP, OCI, IBM Cloud)
✅ **7 Strategic Categories** - Compute, Storage, Database, Analytics, AI/ML, Networking, Data Integration
✅ **Complete Service Listings** - Includes advanced services like Vertex AI, BigQuery ML, Contact Center AI, Watson Studio, GoldenGate
✅ **Easy Expansion** - Add new providers by extending data.yml with the standard 7-category structure
✅ **Cross-Cloud View** - Highlights services available across platforms for multi-cloud strategies
✅ **Interactive Visualization** - Landscape2 provides filtering and search capabilities
✅ **Fully Documented** - Detailed guide for each provider, category, and service with URLs

## Design Philosophy

This unified landscape serves several purposes:

1. **Cloud Provider Comparison** - Understand available services across major clouds
2. **Multi-Cloud Strategy** - Identify services with consistent patterns across providers
3. **Migration Planning** - See equivalent services when moving between clouds
4. **Cost Optimization** - Compare offerings to choose the best provider per workload
5. **Extensibility** - Easily add new providers as cloud market evolves

## Resources

- [Landscape2 Documentation](https://github.com/cncf/landscape2)
- [AWS Services](https://aws.amazon.com/products/)
- [Azure Services](https://azure.microsoft.com/en-us/services/)
- [GCP Services](https://cloud.google.com/products)
- [OCI Services](https://www.oracle.com/cloud/services/)
- [IBM Cloud Services](https://www.ibm.com/cloud)

## Data Source

Service definitions are based on the comprehensive cloud service maps from [maf.net](https://github.com/ophelialabs/maf.net/blob/main/src/components/cloudscape/cloud-maps.tsx), ensuring accurate and up-to-date service coverage across all five major cloud providers.
