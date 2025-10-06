# Greetings visitor 🤘

a hardcore Logistician, with lots of love for Claude, Data and Analytics.

industrialEngineering background with an MSc in Logistics & Supply Chain Management

self taught on data exploration & analysis, as well as data visualization. 

bridging data & logistics to define business decisions and improve processes.

main hobby: options chains analysis and greeks exposure interpretation

it all started with Excel and PowerQuery&Pivot!

## 💻 Stamp Collection

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white)

![Polars](https://img.shields.io/badge/polars-%23CD792C.svg?style=for-the-badge&logo=polars&logoColor=white)
![Delta Lake](https://img.shields.io/badge/deltalake-00ADD4?style=for-the-badge&logo=databricks&logoColor=white)

![Streamlit](https://img.shields.io/badge/Streamlit-%23FE4B4B.svg?style=for-the-badge&logo=streamlit&logoColor=white)
![NiceGUI](https://img.shields.io/badge/NiceGUI-%234285F4.svg?style=for-the-badge&logo=python&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)
![Altair](https://img.shields.io/badge/Altair-%23006BA6.svg?style=for-the-badge&logo=altair&logoColor=white)

![Jira](https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white)

## 🌐 Socials
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ikiokpas)
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?style=for-the-badge&logo=Twitter&logoColor=white)](https://twitter.com/iGiannnis)

## 🎯 Random Quote
<div align="left">
<blockquote>
<h3><em>"Memento Mori"</em></h3>
<p><strong>the Stoics</strong></p>
</blockquote>
</div>


## 📂 Projects

### Interactive Brokers Websocket Connection
Engineered a production-grade real-time options data pipeline leveraging Python's asyncio and websockets for concurrent I/O operations, processing 50+ messages/sec from Interactive Brokers WebSocket API with intelligent contract filtering (3.5% ATM strike range, 3 nearest expirations). 

Architected a multi-worker message processing system (4 parallel workers with asyncio.Queue) implementing priority-based message routing, LRU caching (@lru_cache with 10K entry capacity) for field parsing optimization, and connection pooling (aiohttp sessions) for API efficiency. 

Data pipeline outputs structured time-series data to Polars DataFrames with explicit schema enforcement (17 typed columns: Greeks, IV, volume, OI, bid/ask), persisted incrementally to Parquet format (pyarrow) with 15-minute file rotation boundaries. 

Implemented comprehensive data quality controls including regex-compiled field cleaners, NaN handling, and automated schema validation. Performance monitoring includes real-time metrics tracking (msg/sec throughput, queue saturation, cache hit rates >90%, dropped message counts) with 30-second interval logging for operational observability.


### Automated Cryptocurrency Trading Bot for ByBit
Engineered an automated cryptocurrency trading system on ByBit leveraging Python with Polars for high-performance data transformations and Hidden Markov Models (HMM) via hmmlearn for probabilistic regime detection. 

Designed a multi-stage data pipeline integrating REST API data ingestion, real-time feature engineering (LDPM indicators, ATR, EMA), and Discord webhook-based approval workflows with asynchronous I/O. 

Implemented enterprise-grade risk controls including position sizing algorithms, trailing stop management, and exchange state synchronization, while maintaining comprehensive logging and error handling for production resilience.

  Ingestion Layer: ByBit REST API → JSON parsing → Schema validation
  
  Transformation Layer: Polars aggregations → Feature engineering → Statistical modeling
  
  Decision Layer: HMM inference → Signal scoring → Rule-based filtering
  
  Approval Layer: Discord webhook → Human confirmation → Event callback
  
  Execution Layer: Order placement → State sync → Position reconciliation
  
  Monitoring Layer: Logging, error handling, performance tracking

### Real-time Options Greeks Monitoring Dashboard ~ Unusual Whales data

• Real-Time Analytics Pipeline

  Built automated ETL workflows processing parquet-based market data using Polars lazy evaluation, 
  implementing complex window functions and aggregations to compute 30+ derived metrics for real-time trading analytics 

• Production Streamlit Dashboard

  Developed scalable BI application with modular data pipelines, auto-refresh capabilities, 
  and interactive Plotly visualizations supporting multiple data sources and configurable lookback periods
