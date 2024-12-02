# SUMMARY    
#### 0. Understand the POWER of Data
> #### 0.1 What's the point ?
> #### 0.2 A gold mine

#### 1. Project Overview
> #### 1.1 Objective
> #### 1.2 Usage
> #### 1.3 Durability
> #### 1.4 Current progress
> #### 1.5 Dashboards
> #### 1.6 Indices (list of databases)

#### 2. Accessibility
> #### 2.1 Who can access to Dashboards ?
> #### 2.2 What are your rules as a dashboard user ?
> #### 2.3 Who can access to the code ?

#### 3. Technical Development
> #### 3.1 How it works ?
> #### 3.2 Data structured: How and Why ?
> #### 3.3 Tech Stack
> > #### 3.3.1 Data pipeline (Extract, Transform, Load) :
> > #### 3.3.2 Containerization :
> > #### 3.3.3 Automation :
> > #### 3.3.4 Code versionning :
> > #### 3.3.5 Project management & documentation :
> > #### 3.3.6 VPS :
> > #### 3.3.7 Project management & Documentation :
> #### 3.4 Data sources and extraction frequency
> #### 3.5 What happens if a datasource is down/stop delivering data?

#### 4. Server
> #### 4.1 Current config
> #### 4.2 Current machine capacity

#### 5. Future improvements
> #### 5.1 [DATA] Add new data sources
> #### 5.2 [DASHBOARD] Add new dashboards
> #### 5.3 [DevOps] Security & Robustness:
> > ##### 5.3.1 HTTPS / SSL Certificate
> > ##### 5.3.2 Export <iframe> dashboard
> > ##### 5.3.3 : Elasticsearch cluster with high availability
> #### 5.4 Tech Documentation
> #### 5.5 Automate snapshots
> #### 5.6 Any proposal from community
#### 6. Team
#### 7. Funding
#### 8. Conclusion

----
# [QDashboard](http://84.247.141.158:5601/s/qubic--public-/app/dashboards#/list?_g=(filters:!(),refreshInterval:(pause:!t,value:60000),time:(from:'2024-04-01T00:00:00.000Z',to:now)))
----

## 0. Understand the POWER of Data
### 0.1 What's the point ?
Data is a demanding field, built on several essential pillars:
- Understanding real needs,
- Rigorous data collection to ensure its quality and relevance,
- Structuring the data to make it exploitable at the most granular level possible.  

This approach helps demystify what may seem unquantifiable, especially when dealing with a mass of complex information.  
Imagine looking at the night sky, attempting to count each visible star. The task feels impossible.  
However, with **data visualization**, after prior data processing, you could create a detailed map of the sky, categorizing stars by brightness, distance, temperature, constellation, chemical composition, etc.  
This map would even allow zooming into specific sections of the sky for more detail, transforming chaos into actionable insights.

### 0.2 A gold mine
Well-used data is a treasure for smart decisions :  
The earlier data is collected, the more experience is accumulated, allowing for better anticipation and understanding of future challenges.  
Data acts as the fuel for decision-making engines.  

In big companies, there is a dedicated data hub that synthesizes and analyzes complex datasets, providing a global vision, identifying trends, and supporting optimal decision-making.  
For Qubic, data serves a strategic purpose:
- **For investors and the community**: it enables in-depth analysis, offering greater transparency and insights.
- **For marketing teams**: it helps evaluate what works (or doesn’t) and refine strategies to maximize effectiveness.
<p align="center" width="100%">
    <img width="80%" src="https://github.com/user-attachments/assets/9354a27b-8d79-4f7e-873b-238b2ec838ac">
</p>

## 1. Project Overview
### 1.1 Objective
The primary goal of **QDashboard** is to provide the community and stakeholders with clear, intuitive visualizations of key data, improving decision-making for **investors** and **marketing teams** while promoting **transparency**.

### 1.2 Usage
url: [qdashboard.org](http://84.247.141.158:5601/s/qubic--public-/app/dashboards#/list?_g=(filters:!(),refreshInterval:(pause:!t,value:60000),time:(from:'2024-04-01T00:00:00.000Z',to:now)))  
To use the Kibana dashboards effectively:
1. **Timeframe**: The displayed data adapts to the selected timeframe. Filters can also apply specific time restrictions on visualizations.  
    <img width="262" alt="image" src="https://github.com/user-attachments/assets/afe7f0ec-664b-49ee-a9af-f64d2a1bd28a">

2. **Filters**: Filters directly affect charts, allowing users to dive deeper into analyses. Filters are temporary and apply only to individual sessions.   
    <img width="700" alt="image" src="https://github.com/user-attachments/assets/420499ba-10f5-4bca-b0a7-90eeb9f62da0">

3. **Interaction**: Users can interact with charts by clicking items to apply global filters, which can be removed from the top left.  
    <img width="173" alt="image" src="https://github.com/user-attachments/assets/71532d03-d5c5-4435-be25-496eae521642">  

### 1.3 Durability
QDashboard is designed for autonomy and resilience, ensuring longevity.  
In critical failure scenarios, documentation enables quick interventions by myself or others.

Databases have different scalability profiles:
- Relational databases (e.g., MySQL/PostgreSQL) require adding servers for horizontal scaling, which is labor-intensive and costly.
- NoSQL databases (e.g., **Elasticsearch**) allow for **vertical scaling**, increasing server capacity with minimal effort and expense.

<p align="center" width="100%">
    <img width="33%" src="https://github.com/user-attachments/assets/6334519b-5835-40e5-8998-8b90f3306a38">
</p>

### 1.4 Current progress
This project stands out because much of the work has already been completed:
```
Data Pipelines (ETL)       ██████████████████░░░░░░░   70.00%
Dashboards                 ████████████████░░░░░░░░░   60.00%
DevOps                     █████████████░░░░░░░░░░░░   50.00%
```
- **Data Pipelines (ETL)**: 70% complete, but new data sources need to be integrated.
- **Dashboards**: New data sources will require new metrics and dashboards. Plan to embed dashboards in Qubic’s website using `<iframe>`.
- **DevOps**: Currently running on a single node, the solution needs high-availability clustering for robustness and better uptime.

### 1.5 Dashboards
<img width="969" alt="image" src="https://github.com/user-attachments/assets/d1ca7221-3e23-4232-8ffc-0407f1208c5e">

#### 1.5.1 [QUBIC] Documentation
> This dashboard serves as a user guide for anyone accessing QDashboard, ensuring that users can fully understand and utilize its features.  
It explains :
> - How to apply and adjust filters to focus on specific data subsets.
> - How to modify the analysis period, enabling users to examine trends over days, weeks, or months.
> - Terms and metrics used throughout the dashboards, ensuring accessibility even to those unfamiliar with blockchain or data visualization.

#### 1.5.2 [QUBIC] Global Info
> A high-level overview of Qubic's performance and metrics, offering a comprehensive snapshot of the ecosystem.  
Key data displayed:
> - **Price History**: Tracks the historical performance of Qubic's token (QU), enabling users to identify price trends and volatility.
> - **Events**: Highlights significant milestones, including token launches, partnerships, or market shifts.
> - **Burned Tokens**: Visualizes the total and recent quantity of burned tokens, reflecting Qubic's commitment to supply reduction.
> - **Performance Trends**: Combines financial and ecosystem metrics to show overall health and progress.

#### 1.5.3 [QUBIC] Richlist
> This dashboard provides insights into major investors and their activities, offering transparency and accountability in Qubic’s ecosystem.  
Key features:
> - **Major Wallets**: Tracks wallets holding over 1,000 QUs, categorized as significant investors.  
> - **Wealth Distribution**: Analyzes the concentration of QU among large wallets, helping identify potential risks (e.g., whale influence).  
> - **Weekly Updates**: The dashboard is updated weekly, ensuring fresh and relevant insights.  

#### 1.5.4 [QUBIC] Transactions
> Focused on blockchain activity, this dashboard tracks real-time and historical Qubic transactions.  
Key features:
> - **Advanced Filtering**: Users can filter transactions by specific wallet addresses, transaction amounts, or entity types.
> - **Real-Time Updates**: Displays live transaction data for instant analysis.
> - **Fraud Detection**: Advanced users can analyze suspicious patterns, helping maintain ecosystem integrity.

#### 1.5.5 [QUBIC] Community
> Measures the engagement and activity of Qubic’s community across various platforms.  
Key data sources and metrics:
> - **Search Metrics**: Analyzes search volume and queries related to Qubic on platforms like Google Trends.
> - **Discord Activity**: Tracks messages, server growth, and user engagement trends over time.

#### 1.5.6 [QUBIC] CFB Airdrop
> Provides a detailed summary of the CFB token airdrop, conducted in May 2024.  
Key feature:
> - **Distribution Metrics**: Shows how many tokens


### 1.6 Indices (=databases)
The solution currently integrates 9 databases, powered by various sources for a comprehensive data view:
1. **coinmarketcap & LiveCoinWatch**: Financial data for cryptocurrencies, including historical data.
2. **discord_stats**: Statistics on server activity from Discord.
3. **eligible_cfb**: List of users eligible for CFB token drops.
4. **finance**: General financial data from yfinance.  
5. **gtrends_queries**: Google trends by query.
6. **gtrends_regions**: Google trends region.
7. **qubic_latest_stat**: Latest statistics on Qubic.
8. **qubic_richlist**: Information on the top Qubic wallets.
9. **qubic_txs**: Detailed tracking of Qubic transactions.
For certain indexes like transactions, richlist, and coinmarketcap, scripts have been developed to retrieve historical data and ensure continuous updates for new data.

## 2. Access & Rules
### 2.1 Who can access to Dashboards ?
Everyone. QDashboard upholds cryptocurrency values:
1. **Decentralization**: Open-source and modifiable.
2. **Transparency**: All Qubic-related data is exposed.
3. **Accessibility**: No private data; open to all.
4. **Autonomy**: Designed for low maintenance.
5. **Control**: Users can analyze blockchain data to track trends and evaluate investor activity.

### 2.2 What are your rules as a dashboard user ?
An anonymous account have been created which serve to everyone.  
This public account no need connection and have basic rules:
- read, interact and apply filters (only related to your local session)
- can't add password or modify dashboards to avoid sabotage and maintain the platform's integrity.

## 3. Technical Development
### 3.1 How it works ?
Data pipelines have been developed to run at specified frequencies. Whether in streaming, every 10 minutes, every hour, at the beginning of each new epoch, or on the first of every month, pipelines are triggered to fetch data, clean it, transform it, adapt it, and structure it before sending it to the Elasticsearch data warehouse.  
You can then use Kibana dashboards, which will pull data from the Elasticsearch databases.  
The pipelines are designed to be autonomous over time. This ensures the project lasts long, requires minimal maintenance.
<p align="center" width="100%">
    <img width="1482" alt="image" src="https://github.com/user-attachments/assets/08c36ce3-2da7-4acc-bb7c-5519f7bb87f9">
</p>

### 3.2 Data structured : How and Why ?
To make informed decisions based on visualizations, it's crucial to know what data to display. But more importantly, the data needs to be structured in a way that makes this easy and efficient.  
The key to this is granularity and denormalization. By structuring data this way, we can cover a broad range of analysis needs without overcomplicating things. This approach allows us to create flexible dashboards quickly.  
For example, if I’m asked to generate a new visualization tomorrow, I can do so immediately, without needing to write new code or spend excessive time setting up pipelines. Instead, I can go directly to the dashboard playground, use the existing data, and create the dashboard, delivering results in no time.  
This means no delays, no extra cost for development time, just fast and reliable insights for everyone in the community.

### 3.3 Tech Stack
#### 3.3.1 Data pipeline (Extract, Transform / Manipulate, Upload) :
- ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=white): Python offering flexibility and power for manipulating and analyzing data. It is perfectly suited to our use case, enabling the automation of data processing tasks with ease.  
- ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white): Pandas is the key library for handling data in DataFrames. It is through Pandas that we structure and transform data.  

#### 3.3.2 Containerization :
- ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white): Docker allows us to run containers for Elasticsearch and Kibana while managing their predefined configurations, ensuring a fast and stable setup. It also enables us to containerize Python scripts and run them with auto-restart functionality, ensuring reliability and automation of data processing tasks.  

#### 3.3.3 Automation :
- ![Crontab](https://img.shields.io/badge/Crontab-17181B?logo=brain&logoColor=fff&style=for-the-badge): Crontab is used for scheduling the automatic execution of Python scripts at regular intervals, allowing for task automation without manual intervention.  

#### 3.3.4 Code versionning :
- ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white): GitHub is used for version control and collaborative code management, allowing us to track the project's evolution, collaborate effectively, and manage deployments.  

#### 3.3.5 Project management & Documentation :
- ![Elasticsearch Badge](https://img.shields.io/badge/Elasticsearch-005571?logo=elasticsearch&logoColor=fff&style=for-the-badge): Elasticsearch is used for indexing and real-time search across large data sets. It allows fast and efficient querying of data, which is crucial for real-time data analysis.  
- ![Kibana Badge](https://img.shields.io/badge/Kibana-005571?logo=kibana&logoColor=fff&style=for-the-badge): Kibana is the visualization tool that integrates with Elasticsearch to provide interactive dashboards and visual analysis, enabling us to track key metrics and make data-driven decisions.  

#### 3.3.6 VPS :
- ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white): Ubuntu serves as the operating system for deploying and running data processing tools, providing a stable and secure environment for all applications.  

#### 3.3.7 Project management & documentation :
- ![Jira](https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white): Jira is used for project management and task tracking. It helps organize workflows, assign responsibilities, and monitor project progress in real time.  
- ![Confluence](https://img.shields.io/badge/confluence-%23172BF4.svg?style=for-the-badge&logo=confluence&logoColor=white): Confluence is used for documentation and team collaboration, storing technical information and project resources to ensure effective coordination within the team.  


### 3.4 Data sources and extraction frequency
- **Qubic Transactions**: Live
- **Latest Qubic Stats**: Every 10 minutes
- **CoinMarketCap / Discord Data**: Every hour
- **Richlist**: Every Wednesday afternoon, as soon as the new epoch is released
- **Google Trends - By Region / Related Queries**: On the 1st of each month

Here are tables listing all the collected (and not yet collected) data, providing the following information:

| **Name**                     | **Type**  | **Source**     | **Collection Frequency** | **Definition**                                                                 | **Database (Index)** |
|------------------------------|-----------|----------------|---------------------------|---------------------------------------------------------------------------------|----------------------|

<details>
    
### Coinmarketcap/LiveCoinWatch API

| **Name**                     | **Type**  | **Source**     | **Collection Frequency** | **Definition**                                                                 | **Database (Index)** |
|------------------------------|-----------|----------------|---------------------------|---------------------------------------------------------------------------------|----------------------|
| symbol                       | keyword   | Coinmarketcap  | per hour                 | The symbol representing the cryptocurrency (e.g., BTC for Bitcoin, ETH for Ethereum) | coinmarketcap        |
| price                         | float     | Coinmarketcap  | per hour                 | The current real-time price of the cryptocurrency.                            | coinmarketcap        |
| cmc_rank                      | integer   | Coinmarketcap  | per hour                 | The current rank of the cryptocurrency based on its market capitalization.    | coinmarketcap        |
| marketcap                     | long      | Coinmarketcap  | per hour                 | The total market capitalization of the cryptocurrency.                        | coinmarketcap        |
| market_cap_dominance          | long      | Coinmarketcap  | per hour                 | The percentage of market dominance.                                           | coinmarketcap        |
| circulating_supply            | long      | Coinmarketcap  | per hour                 | The total number of tokens available in the market.                           | coinmarketcap        |
| total_supply                  | long      | Coinmarketcap  | per hour                 | The total number of tokens that exist, including those in circulation and locked. | coinmarketcap        |
| fully_diluted_market_cap      | long      | Coinmarketcap  | per hour                 | The market capitalization assuming all tokens are in circulation.            | coinmarketcap        |
| @timestamp                    | date      | Coinmarketcap  | per hour                 | The exact date and time when the data is collected, in the format YYYY-MM-DD HH:mm:ss. | coinmarketcap        |
| volume_1h (check if exist)    | long      | Coinmarketcap  | per hour                 | The total trading volume of the cryptocurrency over the last hour.           | coinmarketcap        |
| percent_change_1h             | float     | Coinmarketcap  | per hour                 | The percentage change in the cryptocurrency's price over the last hour.      | coinmarketcap        |

---

### Qubic Richlist (Qubic API)

| **Name**          | **Type**   | **Source** | **Collection Frequency** | **Definition**                                                | **Database (Index)** |
|-------------------|------------|------------|---------------------------|--------------------------------------------------------------|----------------------|
| @timestamp        | date       | Qubic API  | every Wednesday           | The exact date and time when the data is collected, in the format YYYY-MM-DD HH:mm. | qubic_richlist       |
| rank              | integer    | Qubic API  | every Wednesday           | Rank of wallets                                                | qubic_richlist       |
| address           | keyword    | Qubic API  | every Wednesday           | Wallet address                                                 | qubic_richlist       |
| qus               | long       | Qubic API  | every Wednesday           | Number of Qubic tokens                                         | qubic_richlist       |
| qus_change        | long       | Qubic API  | every Wednesday           | Difference of Qus less Qus from last week                     | qubic_richlist       |
| rate_qus_change   | float      | Qubic API  | every Wednesday           | Difference of Qus less Qus from last week (rate)              | qubic_richlist       |

---

### Qubic Transactions (Qubic API)

| **Name**        | **Type**   | **Source** | **Collection Frequency** | **Definition**                                               | **Database (Index)** |
|-----------------|------------|------------|---------------------------|-------------------------------------------------------------|----------------------|
| txid            | keyword    | Qubic API  | Real-time                 | Unique identifier of the transactions.                       | qubic_txs            |
| tick            | keyword    | Qubic API  | Real-time                 | Tick representing an identifier or sequence number for each transaction. | qubic_txs            |
| tx_timestamp    | integer    | Qubic API  | Real-time                 | The exact time when the transaction is collected.            | qubic_txs            |
| src             | keyword    | Qubic API  | Real-time                 | Source address involved in the transaction.                  | qubic_txs            |
| dest            | keyword    | Qubic API  | Real-time                 | Destination address receiving the funds from the transaction. | qubic_txs            |
| qus             | long       | Qubic API  | Real-time                 | Amount transferred in the transaction.                       | qubic_txs            |

---

### Financial Data (yFinance)

| **Name**         | **Type**   | **Source**  | **Collection Frequency** | **Definition**                                               | **Database (Index)** |
|------------------|------------|-------------|---------------------------|-------------------------------------------------------------|----------------------|
| @timestamp       | date       | yfinance    | never                     | The exact date and time when the data is collected, in the format YYYY-MM-DD HH:mm:ss. | finance              |
| price            | float      | yfinance    | never                     | Current price                                                | finance              |
| symbol           | keyword    | yfinance    | never                     | Financial and crypto symbol available                        | finance              |

---

### Google Trends Queries (Google Trends API)

| **Name**    | **Type**  | **Source**  | **Collection Frequency** | **Definition**                                           | **Database (Index)** |
|-------------|-----------|-------------|---------------------------|---------------------------------------------------------|----------------------|
| @timestamp  | date      | GT          | 1st day of month           | Month when the data was recorded, in yyyy-MM format.     | gtrends_queries      |
| keyword     | text      | GT          | 1st day of month           | Words that were written in organic search last month.   | gtrends_queries      |

### Gtrends Regions (Google Trends API)

| **Name**    | **Type**  | **Source** | **Collection Frequency** | **Definition**                                           | **Database (Index)** |
|-------------|-----------|------------|---------------------------|---------------------------------------------------------|----------------------|
| @timestamp  | date      | GT         | 1st day of month           | Month when the data was recorded, in yyyy-MM format.     | gtrends_region       |
| country     | keyword   | GT         | 1st day of month           | Name of the country                                      | gtrends_region       |
| iso_code    | keyword   | GT         | 1st day of month           | 2 letters code of the country (US, CH, FR, …)            | gtrends_region       |

---

### Count Discord Community (HTTP Request)

| **Name**                  | **Type**   | **Source**   | **Collection Frequency** | **Definition**                                             | **Database (Index)** |
|---------------------------|------------|--------------|---------------------------|-----------------------------------------------------------|----------------------|
| approximate_member_count   | integer    | http_request | per hour                 | Total of all members in the discord server                 | discord_stats        |
| approximate_presence_count | integer    | http_request | per hour                 | All online members                                          | discord_stats        |

---

### Financial Data (yFinance)

| **Name**         | **Type**   | **Source**  | **Collection Frequency** | **Definition**                                               | **Database (Index)** |
|------------------|------------|-------------|---------------------------|-------------------------------------------------------------|----------------------|
| @timestamp       | date       | yfinance    | never                     | The exact date and time when the data is collected, in the format YYYY-MM-DD HH:mm:ss. | finance              |
| price            | float      | yfinance    | never                     | Current price                                                | finance              |
| symbol           | keyword    | yfinance    | never                     | Financial and crypto symbol available                        | finance              |

---

### Google Analytics 4 API (Need Permission)

*Ask Qubic team to get API key (I can see the `<gtag>` in the HTML Qubic page)*

| **Name**         | **Type**   | **Source**  | **Collection Frequency** | **Definition**                                               | **Database (Index)** |
|------------------|------------|-------------|---------------------------|-------------------------------------------------------------|----------------------|
| sessions         | integer    | GA4         | -                         | Number of sessions on the website                            | ga4                  |
| users            | integer    | GA4         | -                         | Total users on the website                                  | ga4                  |
| new_users        | integer    | GA4         | -                         | Number of new users                                           | ga4                  |
| hits             | integer    | GA4         | -                         | Total hits or page views                                    | ga4                  |
| device_category  | keyword    | GA4         | -                         | Category of devices used (e.g., mobile, desktop)            | ga4                  |
| channel_grouping | keyword    | GA4         | -                         | The marketing channel grouping for the traffic               | ga4                  |
| engagement_rate  | float      | GA4         | -                         | Engagement rate on the website                              | ga4                  |
| bounce_rate      | float      | GA4         | -                         | Bounce rate (percentage of users who leave the site after viewing one page) | ga4                  |

---

### Google Search Console API (Need Permission)

| **Name**    | **Type**   | **Source** | **Collection Frequency** | **Definition**                                         | **Database (Index)** |
|-------------|------------|------------|---------------------------|-------------------------------------------------------|----------------------|
| domain      | keyword    | GSC        | -                         | Domain of the website                                  | gsc                  |
| site_url    | keyword    | GSC        | daily                     | URL of the site                                        | gsc                  |
| query       | text       | GSC        | daily                     | The search query used to find the site                 | gsc                  |
| clicks      | integer    | GSC        | daily                     | Number of clicks the site received                     | gsc                  |
| impressions | integer    | GSC        | daily                     | Number of times the site was shown in search results   | gsc                  |
| ctr         | float      | GSC        | daily                     | Click-through rate (CTR) of the site                   | gsc                  |
| position    | float      | GSC        | daily                     | Average search result position for the site            | gsc                  |
| @timestamp  | date       | GSC        | daily                     | The exact date and time when the data was recorded, in YYYY-MM-DD format. | gsc                  |

---

### Count Twitter Followers (Swagger UI)

| **Name**            | **Type**   | **Source** | **Collection Frequency** | **Definition**                                             | **Database (Index)** |
|---------------------|------------|------------|---------------------------|-----------------------------------------------------------|----------------------|
| twitter_followers    | integer    | ?          | per hour                 | Number of Twitter followers for the account                | qubic_members        |
| twitter_tweets       | integer    | ?          | per hour                 | Number of tweets made by the account                        | qubic_members        |
| twitter_likes        | integer    | ?          | per hour                 | Number of likes received by the account's tweets            | qubic_members        |

</details>



### 3.5 What happened if datasource is down / stop deliver data ?
It may happen that a data source stops providing data, or that we encounter sudden access issues or other disruptions. Once the problem is identified and analyzed, a solution will be implemented as quickly as possible. This will involve recovering any missing data and resuming the data collection process without delay.

## 4. Server
### 4.1 Current config

|            OS            |     CPU     |     RAM      |      Memory      |   Data transfer   |   Snapshot   |
|--------------------------|-------------|--------------|------------------|-------------------|--------------|
|   Ubuntu 20.04 (64 Bit)  |   6 vCPU    |   16 GO RAM   |  **400 GB SSD**  |   32 TB Traffic   |   Available  |

> [!NOTE]
> When the limit is nearing or latency is observed, the higher plan will be applied without any maintenance.

### 4.2 Current Machine capacity  
```
(19/11/2024):  
Used storage space     █░░░░░░░░░░░░░░░░░░░░░░░░   ~ 6 %
```

## 5. Future improvements
### 5.1 [DATA] Add new data sources :
- [Twitter](https://snowcait.github.io/twitter-swagger-ui/) : To analyze Twitter activity, including retweets, posts tagging 'Qubic', follower count, recent posts, likes, and gauge Qubic’s online presence and sentiment.
- [Google Analytics](https://developers.google.com/analytics/devguides/reporting/data/v1) : Collect data related to the Qubic.org website and its pages. This will allow tracking metrics like sessions, bounce rates, time spent on specific pages, and understanding user behavior. For example, if users spend only 2 seconds on the "whitepaper" page, this could indicate an issue with the content or other factors, as that page is meant to be read and is usually text-heavy.
- [Google Search Console](https://developers.google.com/webmaster-tools/v1/searchanalytics/query) : Identify the keywords driving traffic to the Qubic.org website. Additionally, it allows for geographic and device-based analysis, comparing performance across countries, devices (mobile, desktop), and pages.
- Aigarth : Once Aigarth is released, extracting its data will be valuable for further analysis, helping to refine Aigarth itself and track its progress.

### 5.2 [DASHBOARD] Add new dashboards :
- Create new visualizations with new sources of data

### 5.3 [DevOps] Security & Robustness :
#### 5.3.1 HTTPS / SSL Certificate
Secure the connection by switching from HTTP to HTTPS.

#### 5.3.2 Export <iframe> dashboard
- insert the `<iframe>` tag into the Qubic website's HTML code.
<img width="230" align="top" alt="image" src="https://github.com/user-attachments/assets/3edd5136-12c3-4e82-b09f-5d693664511a">
<img width="230" alt="image" src="https://github.com/user-attachments/assets/da5ecd21-b35b-4724-810a-1ffd3cca82c2">

### 5.3.3: High Availability Elasticsearch Cluster
#### Why a cluster ?  
Elasticsearch is a distributed search and analytics engine.   
For projects where data availability and fault tolerance are critical, a single node is insufficient.

A cluster provides:
- Load balancing to distribute requests across multiple nodes.
- Data redundancy through shards and replicas.
- Horizontal scalability, allowing additional nodes to be added as needed.

Risks without high availability (= without cluster):
- Loss of access to data in case of a node failure.

Proposed Architecture:
- A **3-node** Elasticsearch cluster.
- Each node will store a portion of the data and handle queries.
- Data replication will ensure fault tolerance, allowing continued access to data even if a node fails.

### 5.4 Tech Documentation
A technical documentation will be created so that any technician can intervene on the project.

### 5.5 Automate snapshots
Currently, server snapshots is created manually. However, the service cloud CLI provides the functionality to perform this operation automatically.

### 5.6 Any proposal from community
If you have any requests, whether it's to add a data source, modify the type of chart, etc., you can contact me directly on Discord or ping me in the channels (ID: **@iliamamara**)

## 6. Team
- Iliam AMARA: **Expert Python** & **Data Engineer**
  - [Portfolio](https://iliam-amara.com/)
  - [Linkedin](https://www.linkedin.com/in/iliam-amara/)
  - Discord: iliamamara | #928329541351522384

## 7. Funding
The total funding request is `$25,000`, split into two equal parts:
- `$12,500` **now**: This amount is to cover all the work already completed, including development, design, testing, and any groundwork that has brought the project to its current stage. This ensures recognition of the time, resources, and expertise invested so far to create a solid foundation.
- `$12,500` for **future improvements**: This second portion is essential for advancing the project to the next level. It will enable critical updates, new features, optimization, and long-term maintenance. These improvements are key to ensuring the project’s growth, functionality, and sustainability.

This approach allows for fair compensation for past efforts while securing the means to deliver on future goals and maximize the project’s potential.

## 8. Conclusion
This solution adds another strength to the project and enhances Qubic’s image by providing a highly useful tool. It makes the project more reliable and demonstrates our ability to build a new service—one that sets us apart from other projects. Through smart approaches, we are positioning ourselves to scale even higher and further.  

**QDashboard** offers comprehensive visibility and understanding of data, delivering significant value for decision-making, particularly for investors and the marketing team, thus driving the project’s growth. Both management and the community benefit from precise analysis, which serves as a strategic tool for resource optimization and swift adaptation to trends.

[**Build Different.**](http://84.247.141.158:5601/s/qubic--public-/app/dashboards#/list?_g=(filters:!(),refreshInterval:(pause:!t,value:60000),time:(from:'2024-04-01T00:00:00.000Z',to:now)))
