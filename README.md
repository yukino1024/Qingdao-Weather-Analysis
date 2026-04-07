# 📊 青岛天气数据分析项目 | Qingdao Weather Data Analysis

本项目是一个基于 Python 的端到端数据科学实践，涵盖了从数据爬取、清洗、多维度统计分析到数据库持久化的全流程。通过对青岛 2020-2023 年历史天气的深度挖掘，定量分析气温、风力及天气分布规律。

This is an end-to-end data science project based on Python, covering web scraping, data cleaning, multi-dimensional statistical analysis, and database persistence. It provides a quantitative analysis of temperature, wind, and weather patterns in Qingdao from 2020 to 2023.

---

## 🛠️ 技术栈 | Tech Stack

* **Data Acquisition**: `Requests`, `BeautifulSoup4`, `fake_useragent`.
* **Data Processing**: `Pandas`, `NumPy`.
* **Visualization**: `Matplotlib` (Time-series & Distribution charts).
* **Database**: `MySQL`, `PyMySQL` (CRUD operations), `DataGrip`.

---

## 🚀 核心功能 | Key Features

### 1. 自动化数据获取 | Automated Data Acquisition
* **动态爬取 (Dynamic Crawling)**: 自动遍历并获取 2020-2023 年共 48 个月的历史天气记录。
    * Automatically iterates through 48 months of historical weather records from 2020 to 2023.
* **鲁棒性设计 (Robustness)**: 内置随机 User-Agent 与重试机制，有效应对反爬限制。
    * Implements randomized User-Agents and retry logic to ensure stable data fetching.

### 2. 深度数据预处理 | Robust Data Preprocessing
* **特征工程 (Feature Engineering)**: 将原始字符串分割并转化为最高/最低气温、白天/夜间天气及风级等结构化数值。
    * Parses raw strings into structured fields such as Max/Min Temp, Day/Night Weather, and Wind Speed.
* **数据清洗 (Data Cleaning)**: 处理缺失值和异常值，利用天气的连续性特征进行逻辑填充。
    * Handles missing/outlier values using logical interpolation based on weather continuity.
* **指标量化 (Quantization)**: 将气温和风力划分为 5 个等级，提升统计分析的可读性。
    * Categorizes temperature and wind into 5 distinct levels for enhanced readability in statistics.

### 3. 可视化统计 | Statistical Visualization
* **宏观趋势 (Macro Trends)**: 生成年度天气分布、温差分布图和风向频率图。
    * Generates annual weather distributions, temperature gap analysis, and wind frequency charts.
* **微观观察 (Micro Observations)**: 绘制月度气温波动折线图，直观展现季节性变化趋势。
    * Plots daily temperature fluctuations to visualize seasonal shifts clearly.

### 4. 数据库持久化 | Database Persistence
* **CRUD 封装 (Encapsulated CRUD)**: 封装了完整的数据库操作类，支持对历史天气数据的增删改查。
    * Encapsulated Python classes for comprehensive MySQL operations (Create, Read, Update, Delete).
* **高效管理 (Data Management)**: 支持按年份、日期或特定关键字进行精准或模糊检索。
    * Supports efficient data management and queries by year, date, or weather keywords.

---

## 📈 项目结论 | Project Insights

* **宜居性评估 (Habitability)**: 青岛全年最高温极少超过 35°C，气候相对稳定，主要处于“舒适”和“偏凉”区间，是非常理想的宜居城市。
    * Qingdao's max temperature rarely exceeds 35°C. The climate is stable and mostly remains within "Comfortable" and "Cool" ranges, making it an ideal city to live in.
* **季节特征 (Seasonality)**: 冬季存在明显的寒冷期，年均零下天数通常在 30 天以上。
    * Winters have a distinct cold period, with an average of over 30 sub-zero days per year.

---

## 📄 报告详情 | Documentation
关于本项目的方法论及详细技术说明，请参阅课程报告：
For more technical details and methodology, please refer to:
2024春季《大学计算机》课程报告 (PDF)

---

## 📂 文件结构 | Project Structure

```text
├── GetData.py        # 爬虫模块 | Web scraper module
├── PertreatData.py   # 预处理模块 | Data cleaning & preprocessing
├── AnalyseData.py    # 分析与可视化 | Visualization & statistics
├── SaveData.py       # 数据库接口 | Database interface
├── Data/             # 原始及处理后的数据 | Raw and processed data
└── Report.pdf        # 课程项目报告 | Full Project Report

---

