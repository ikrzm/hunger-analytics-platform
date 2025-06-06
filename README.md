# Hunger Analytics Platform

A scalable data engineering platform for analyzing hunger and food security trends across multiple regions. Currently supporting Sub-Saharan Africa with architecture designed for global expansion.

## 🌍 Project Overview

This project investigates hunger and starvation trends using free, authoritative data sources. We integrate multi-source data on nutrition, food security, conflict, and economic indicators to analyze correlations and trends.

### Current Focus: Sub-Saharan Africa
- **Duration**: 4-week Shape Up cycle
- **Data Sources**: 5 free APIs (FAO, World Bank, WHO, UN Data, ACLED)
- **Output**: Interactive dashboard with analytics capabilities

## 📊 Data Sources

| Source | Type | Data Provided | API Limits |
|--------|------|---------------|------------|
| FAO FAOSTAT | Free | Undernourishment, Food Insecurity | 1000/hour |
| World Bank Open Data | Free | GDP, Poverty rates | No strict limits |
| WHO Global Health | Free | Malnutrition rates | 1000/day |
| UN Data | Free | Health, nutrition indicators | Moderate |
| ACLED (Free) | Freemium | Conflict events | 2500 records/year |

## 🏗️ Architecture

```
hunger-analytics-platform/
├── config/               # Regional configurations
├── pipeline/            # ETL pipeline components
│   ├── extractors/      # Data source API clients
│   ├── transformers/    # Data cleaning and processing
│   └── loaders/         # Database and file loading
├── dashboard/           # Streamlit dashboard
├── data/               # Local data storage
└── deployment/         # Docker and cloud configs
```

## 🚀 Quick Start

### Prerequisites
- Python 3.9+
- PostgreSQL 12+
- Docker (optional but recommended)

### Setup
```bash
# Clone repository
git clone <your-repo-url>
cd hunger-analytics-platform

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys and database credentials

# Run initial setup
python setup.py
```

### Development Workflow

**Week 1: Foundation & Data Integration**
- [ ] API setup and testing
- [ ] Data extraction scripts
- [ ] Basic data cleaning

**Week 2: ETL Pipeline & Database**
- [ ] Complete ETL architecture
- [ ] PostgreSQL integration
- [ ] Docker containerization

**Week 3: Analytics & Dashboard**
- [ ] Correlation analysis
- [ ] Streamlit dashboard
- [ ] Interactive visualizations

**Week 4: Production Deployment**
- [ ] Cloud deployment
- [ ] Performance optimization
- [ ] Documentation

## 📈 Regional Expansion Plan

The platform is designed for easy expansion to new regions:

### Planned Regions
- **Phase 1**: Sub-Saharan Africa ✅ (Current)
- **Phase 2**: South Asia
- **Phase 3**: MENA (Middle East & North Africa)
- **Phase 4**: Latin America

### Adding New Regions
1. Create region config file in `config/regions/`
2. Update data source mappings
3. Test data extraction
4. Deploy regional dashboard

## 🛠️ Technology Stack

- **Language**: Python 3.9+
- **Database**: PostgreSQL 13+
- **Dashboard**: Streamlit
- **Deployment**: Google Cloud Run
- **Orchestration**: Simple cron jobs
- **Containerization**: Docker

## 📋 API Keys Required

Before starting development, obtain free API keys from:

1. **FAO FAOSTAT**: [Register here](http://www.fao.org/faostat/en/#data)
2. **World Bank**: [API info](https://datahelpdesk.worldbank.org/knowledgebase/articles/889392)
3. **WHO**: [Registration](https://www.who.int/data/gho)
4. **ACLED**: [Free registration](https://acleddata.com/curated-data-files/)

## 🤝 Contributing

This project follows Shape Up methodology:
- 4-week cycles
- Clear deliverables per week
- Circuit breaker if major issues arise

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## 📞 Contact

For questions about this project or collaboration opportunities, please open an issue or contact the development team.

---

**Current Status**: 🏗️ Week 1 - Foundation & Data Integration  
**Last Updated**: January 2025