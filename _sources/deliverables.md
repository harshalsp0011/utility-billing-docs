# Deliverables & Access

## Code Repository

**Main Repository**: [https://github.com/harshalsp0011/utility-billing-ai](https://github.com/harshalsp0011/utility-billing-ai)

Contains:
- All source code
- Docker configuration
- Database schemas
- Tests
- Documentation

## Live Dashboard

**URL**: [https://troyandbankprototype.streamlit.app/](https://troyandbankprototype.streamlit.app/)

**Dashboard Name**: "The Agentic Auditor"

Features:
- Upload PDF documents
- View processing status
- Download audit reports
- View anomalies

**Login**: Contact admin for credentials

## Access Instructions

### For End Users

1. Go to dashboard URL
2. Login with your credentials
3. Upload tariff or bill PDF
4. Wait for processing (1-2 minutes)
5. Review results and download report

### For Administrators

```bash
# SSH to server
ssh admin@your-server.com

# View logs
docker-compose logs -f

# Restart services
docker-compose restart
```

### For Developers

```bash
# Clone repo
git clone https://github.com/harshalsp0011/utility-billing-ai.git
cd utility-billing-ai

# Setup environment
cp .env.example .env
# Add your API keys to .env

# Start services
docker-compose up -d

# Access
# Dashboard: http://localhost:8501
# Airflow: http://localhost:8080
```

## Reports

Upload sample reports to `uploads/reports/`:
- Audit reports
- Anomaly reports
- Performance summaries

## Documentation

- **User Guide**: `uploads/docs/user_guide.pdf`
- **API Docs**: `uploads/docs/api_docs.pdf`
- **Admin Guide**: `uploads/docs/admin_guide.pdf`

## Support

- **Issues**: [GitHub Issues](https://github.com/harshalsp0011/utility-billing-ai/issues)
- **Email**: harshal.sanjivpatil2000@gmail.com
