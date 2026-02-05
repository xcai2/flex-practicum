# Jabil Inc. SEC Filings Links

## Company Basic Information
- **CIK**: 0000898293
- **EIN**: 381886260
- **State of Incorporation**: Delaware (DE)
- **Fiscal Year End**: 08/31
- **SEC EDGAR Page**: https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0000898293

## 10-K Annual Reports

### FY2025 (As of August 31, 2025)
- **Filing Date**: Expected October 2025
- **Direct Link**: https://www.sec.gov/Archives/edgar/data/898293/000162828025045293/jbl-20250831.htm
- **Status**: Filed

### FY2024 (As of August 31, 2024)
- **Filing Date**: October 28, 2024
- **Direct Link**: https://www.sec.gov/Archives/edgar/data/898293/000162828024043960/jbl-20240831.htm
- **HTML Format**: Available
- **PDF Download**: Can be downloaded from SEC website

### FY2023 (As of August 31, 2023)
- **Filing Date**: October 20, 2023
- **Direct Link**: Need to search from SEC EDGAR
- **Size**: Approximately 1.1 MB

### FY2022 (As of August 31, 2022)
- **Filing Date**: October 2022
- **Direct Link**: https://www.sec.gov/Archives/edgar/data/898293/000119312522268383/d389587d10k.htm
- **HTML Format**: Available

### FY2021 (As of August 31, 2021)
- **Filing Date**: October 2021
- **Direct Link**: Need to search from SEC EDGAR

## 10-Q Quarterly Reports

### Q1 FY2026 (As of November 30, 2025)
- **Filing Date**: January 9, 2026
- **Direct Link**: Need to find from latest filings
- **Size**: Approximately 9.71 MB

### Q4 FY2025 (As of August 31, 2025)
- **Note**: Q4 Usually included in 10-K annual report

### Q3 FY2025 (As of May 31, 2025)
- **Filing Date**: July 2025
- **Direct Link**: Need to search from SEC EDGAR

### Q2 FY2025 (As of February 28, 2025)
- **Filing Date**: April 2025
- **Direct Link**: Need to search from SEC EDGAR

### Q1 FY2025 (As of November 30, 2024)
- **Filing Date**: January 2025
- **Direct Link**: Need to search from SEC EDGAR

### Q3 FY2024 (As of May 31, 2024)
- **Filing Date**: July 2024
- **Direct Link**: https://www.sec.gov/Archives/edgar/data/898293/000162828024031429/
- **Index page**: Available

### Q2 FY2024 (As of February 29, 2024)
- **Filing Date**: April 2024
- **Direct Link**: Need to search from SEC EDGAR

### Q1 FY2024 (As of November 30, 2023)
- **Filing Date**: January 2024
- **Direct Link**: Need to search from SEC EDGAR

### Q3 FY2023 (As of May 31, 2023)
- **Filing Date**: July 2023
- **Direct Link**: Need to search from SEC EDGAR

### Q2 FY2023 (As of February 28, 2023)
- **Filing Date**: April 2023
- **Direct Link**: Need to search from SEC EDGAR

### Q1 FY2023 (As of November 30, 2022)
- **Filing Date**: January 2023
- **Direct Link**: Need to search from SEC EDGAR

### Q3 FY2022 (As of May 31, 2022)
- **Filing Date**: July 2022
- **Direct Link**: Need to search from SEC EDGAR

### Q2 FY2022 (As of February 28, 2022)
- **Filing Date**: April 2022
- **Direct Link**: Need to search from SEC EDGAR

### Q1 FY2022 (As of November 30, 2021)
- **Filing Date**: January 2022
- **Direct Link**: Need to search from SEC EDGAR

## 8-K Current Reports

### Recent 8-K Filings
- **December 17, 2025**: Earnings release
  - Link: Need to search from SEC EDGAR
  - Size: Approximately 383 KB

### Key Events to Search in 8-K
- Earnings release announcement
- Major contract signing
- M&A activity
- Executive changes
- Factory opening/closing
- Major investment announcement

## Other Useful Resources

### Jabil Investor Relations Pages
- **SEC Filings**: https://investors.jabil.com/financials/sec-filings/default.aspx
- **Annual Reports**: https://investors.jabil.com/financials/annual-reports/default.aspx

### Third-party Databases
- **SEC Database**: https://research.secdatabase.com/CIK/898293/Company-Name/JABIL-INC/Symbol/JBL
- **AnnualReports.com**: https://www.annualreports.com/Company/jabil-circuit-inc
- **StockLight**: https://stocklight.com/stocks/us/nyse-jbl/jabil-circuit/annual-reports

## Download Methods

### Download Using Python
```python
from sec_edgar_downloader import Downloader

# Setup downloader
dl = Downloader("YourName", "your.email@example.com")

# Download 10-K (past 3 years)
dl.get("10-K", "JBL", after="2021-09-01", before="2025-12-31", 
       download_details=True)

# Download 10-Q (past 12 quarters)
dl.get("10-Q", "JBL", after="2022-01-01", before="2025-12-31",
       download_details=True)

# Download 8-K (past 3 years)
dl.get("8-K", "JBL", after="2022-01-01", before="2025-12-31",
       download_details=True)
```

### Manual Download
1. Visit SEC EDGAR: https://www.sec.gov/edgar/searchedgar/companysearch.html
2. Search CIK: 0000898293 or company name: Jabil Inc
3. Select file type and date range
4. Download HTML or PDF format

## Key Sections to Extract

### Key 10-K Sections
- **Item 1**: Business - Business description and strategy
- **Item 1A**: Risk Factors - Risk factors
- **Item 7**: MD&A - Management Discussion and Analysis
- **Item 8**: Financial Statements - Financial Statements (Pay special attention to CapEx)

### Key 10-Q Sections
- **Part I, Item 2**: MD&A - Quarterly management discussion
- **Part I, Item 1**: Financial Statements - Quarterly Financial Statements

## Data Collection Status
- [ ] 10-K FY2025
- [ ] 10-K FY2024
- [ ] 10-K FY2023
- [ ] 10-K FY2022
- [ ] 10-Q Q1-Q3 FY2025
- [ ] 10-Q Q1-Q3 FY2024
- [ ] 10-Q Q1-Q3 FY2023
- [ ] 10-Q Q1-Q3 FY2022
- [ ] Related 8-K filings