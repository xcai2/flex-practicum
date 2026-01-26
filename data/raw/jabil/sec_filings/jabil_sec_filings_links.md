# Jabil Inc. SEC Filings Links

## Company Basic Information
- **CIK**: 0000898293
- **EIN**: 381886260
- **State of Incorporation**: Delaware (DE)
- **Fiscal Year End**: 08/31
- **SEC EDGAR Page**: https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0000898293

## 10-K Annual Reports

### FY2025 (As of2025years8月31日)
- **Filing Date**: Expected2025years10月
- **Direct Link**: https://www.sec.gov/Archives/edgar/data/898293/000162828025045293/jbl-20250831.htm
- **Status**: Filed

### FY2024 (As of2024years8月31日)
- **Filing Date**: 2024years10月28日
- **Direct Link**: https://www.sec.gov/Archives/edgar/data/898293/000162828024043960/jbl-20240831.htm
- **HTML Format**: Available
- **PDF Download**: Can be downloaded from SEC website

### FY2023 (As of2023years8月31日)
- **Filing Date**: 2023years10月20日
- **Direct Link**: Need to search from SEC EDGAR
- **Size**: 约1.1 MB

### FY2022 (As of2022years8月31日)
- **Filing Date**: 2022years10月
- **Direct Link**: https://www.sec.gov/Archives/edgar/data/898293/000119312522268383/d389587d10k.htm
- **HTML Format**: Available

### FY2021 (As of2021years8月31日)
- **Filing Date**: 2021years10月
- **Direct Link**: Need to search from SEC EDGAR

## 10-Q Quarterly Reports

### Q1 FY2026 (As of2025years11月30日)
- **Filing Date**: 2026years1月9日
- **Direct Link**: 需要从最新文件中查找
- **Size**: 约9.71 MB

### Q4 FY2025 (As of2025years8月31日)
- **注**: Q4Usually included in 10-K annual report

### Q3 FY2025 (As of2025years5月31日)
- **Filing Date**: 2025years7月
- **Direct Link**: Need to search from SEC EDGAR

### Q2 FY2025 (As of2025years2月28日)
- **Filing Date**: 2025years4月
- **Direct Link**: Need to search from SEC EDGAR

### Q1 FY2025 (As of2024years11月30日)
- **Filing Date**: 2025years1月
- **Direct Link**: Need to search from SEC EDGAR

### Q3 FY2024 (As of2024years5月31日)
- **Filing Date**: 2024years7月
- **Direct Link**: https://www.sec.gov/Archives/edgar/data/898293/000162828024031429/
- **Index page**: Available

### Q2 FY2024 (As of2024years2月29日)
- **Filing Date**: 2024years4月
- **Direct Link**: Need to search from SEC EDGAR

### Q1 FY2024 (As of2023years11月30日)
- **Filing Date**: 2024years1月
- **Direct Link**: Need to search from SEC EDGAR

### Q3 FY2023 (As of2023years5月31日)
- **Filing Date**: 2023years7月
- **Direct Link**: Need to search from SEC EDGAR

### Q2 FY2023 (As of2023years2月28日)
- **Filing Date**: 2023years4月
- **Direct Link**: Need to search from SEC EDGAR

### Q1 FY2023 (As of2022years11月30日)
- **Filing Date**: 2023years1月
- **Direct Link**: Need to search from SEC EDGAR

### Q3 FY2022 (As of2022years5月31日)
- **Filing Date**: 2022years7月
- **Direct Link**: Need to search from SEC EDGAR

### Q2 FY2022 (As of2022years2月28日)
- **Filing Date**: 2022years4月
- **Direct Link**: Need to search from SEC EDGAR

### Q1 FY2022 (As of2021years11月30日)
- **Filing Date**: 2022years1月
- **Direct Link**: Need to search from SEC EDGAR

## 8-K Current Reports

### Recent 8-K Filings
- **2025years12月17日**: 财报发布
  - 链接: Need to search from SEC EDGAR
  - 大小: 约383 KB

### Key Events to Search in 8-K
- Earnings release announcement
- Major contract signing
- M&A activity
- Executive changes
- Factory opening/closing
- Major investment announcement

## Other Useful Resources

### Jabil Investor Relations Pages
- **SEC文件**: https://investors.jabil.com/financials/sec-filings/default.aspx
- **years度报告**: https://investors.jabil.com/financials/annual-reports/default.aspx

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

# Download 10-K (past3years)
dl.get("10-K", "JBL", after="2021-09-01", before="2025-12-31", 
       download_details=True)

# Download 10-Q (past12quarters)
dl.get("10-Q", "JBL", after="2022-01-01", before="2025-12-31",
       download_details=True)

# Download 8-K (past3years)
dl.get("8-K", "JBL", after="2022-01-01", before="2025-12-31",
       download_details=True)
```

### Manual Download
1. Visit SEC EDGAR: https://www.sec.gov/edgar/searchedgar/companysearch.html
2. Search CIK: 0000898293 or company name: Jabil Inc
3. Select file type and date range
4. 下载HTML或PDFformat

## Key Sections to Extract

### Key 10-K Sections
- **Item 1**: Business - Business description and strategy
- **Item 1A**: Risk Factors - Risk factors
- **Item 7**: MD&A - Management Discussion and Analysis
- **Item 8**: Financial Statements - Financial Statements(Pay special attention to CapEx)

### Key 10-Q Sections
- **Part I, Item 2**: MD&A - Quarterly management discussion
- **Part I, Item 1**: Financial Statements - 季度Financial Statements

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
