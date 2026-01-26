# Data Collection Guide

## Target Company Information

### 1. Jabil Inc. (JBL)
- **Official Website**: https://www.jabil.com
- **Investor Relations**: https://investors.jabil.com
- **SEC CIK**: 0000898293
- **Stock Ticker**: NYSE: JBL
- **Key Analysis Focus**: Operational expansion and data center strategy

### 2. Celestica Inc. (CLS)
- **Official Website**: https://www.celestica.com
- **Investor Relations**: https://www.celestica.com/investors
- **SEC CIK**: 0001000623
- **Stock Ticker**: NYSE: CLS, TSX: CLS
- **Key Analysis Focus**: Shift to hardware platform solutions and hyperscale partnerships

### 3. Benchmark Electronics, Inc. (BHE)
- **Official Website**: https://www.bench.com
- **Investor Relations**: https://ir.bench.com
- **SEC CIK**: 0000925036
- **Stock Ticker**: NYSE: BHE
- **Key Analysis Focus**: Portfolio of high-performance computing and traditional medical/aerospace businesses

### 4. Sanmina Corporation (SANM)
- **Official Website**: https://www.sanmina.com
- **Investor Relations**: https://investor.sanmina.com
- **SEC CIK**: 0001068686
- **Stock Ticker**: NASDAQ: SANM
- **Key Analysis Focus**: Vertical integration strategy and aggressive moves in the server ecosystem

### 5. Flex Ltd. (FLEX)
- **Official Website**: https://flex.com
- **Investor Relations**: https://investors.flex.com
- **SEC CIK**: 0000866374
- **Stock Ticker**: NASDAQ: FLEX
- **Key Analysis Focus**: Baseline group, benchmark data accuracy and sentiment

---

## Data Collection Checklist

### A. Earnings Call Transcripts

**Time Range**: past 12 quarters (2022 Q1 - 2024 Q4)

**Data Sources**:
1. **Company Investor Relations Page** (preferred)
   - Usually under "Events & Presentations" or "Quarterly Results"
   
2. **Seeking Alpha**
   - URL format: `https://seekingalpha.com/symbol/{TICKER}/earnings/transcripts`
   - Partial transcripts available for free
   
3. **The Motley Fool**
   - Provides some free transcripts
   
4. **SEC 8-K Filings**
   - Some companies attach transcripts as exhibits in 8-K filings

**Collection Items**:
- [ ] Full meeting transcript text
- [ ] Meeting date
- [ ] Fiscal years and quarters
- [ ] Prepared remarks by management
- [ ] Q&A session
- [ ] Participants list (executives and analysts)

**Save Format**:
- Filing name: `{company}_{YYYY}_Q{Q}_earnings_call.txt`
- Metadata: stored in JSON format in a same-named .json file

---

### B. SEC Filings

**SEC EDGAR Site**: https://www.sec.gov/edgar/searchedgar/companysearch.html

#### B1. 10-K Annual Reports
**Time Range**: 2021, 2022, 2023 (3 years)

**Key Sections**:
- Item 1: Business
- Item 1A: Risk Factors
- Item 7: Management's Discussion and Analysis (MD&A)
- Item 8: Financial Statements and Supplementary Data

**Key Notes**:
- Business segment breakdown
- Total and segmented CapEx
- Geographic distribution
- Strategic directions
- Risk factors (especially market risks)

#### B2. 10-Q Quarterly Reports
**Time Range**: past 12 quarters

**Key Sections**:
- Part I, Item 2: MD&A
- Part I, Item 1: Financial Statements

**Key Notes**:
- Quarterly CapEx
- Business segment performance
- Material events

#### B3. 8-K Material Event Reports
**Time Range**: past 3 years

**Key Event Types**:
- Item 1.01: Entry into Material Definitive Agreement
- Item 2.02: Results of Operations and Financial Condition
- Item 8.01: Other Events
- Major acquisitions, plant openings, strategic partnerships

**Collection Method**:
```python
from sec_edgar_downloader import Downloader

dl = Downloader("YourName", "your.email@example.com")

# Download 10-K
dl.get("10-K", "JBL", after="2021-01-01", before="2024-12-31")

# Download 10-Q
dl.get("10-Q", "JBL", after="2022-01-01", before="2024-12-31")

# Download 8-K
dl.get("8-K", "JBL", after="2022-01-01", before="2024-12-31")
```

---

### C. Investor Presentations

**Types**:
1. **Investor Day Presentations**
2. **Quarterly Earnings Presentations**
3. **Industry Conference Presentations**

**Data Sources**:
- Company Investor Relations Page
- SEC 8-K Attachments
- Investor conference websites

**Collection Items**:
- [ ] PDF presentation files
- [ ] Accompanying videos (if any)
- [ ] Press releases
- [ ] Presentation date and occasion

**Save Format**:
- Filing name: `{company}_{YYYY_MM_DD}_{event_type}.pdf`

---

### D. Press Releases and Announcements

**Key Topics**:
1. **CapEx Related**:
   - New plant openings/expansions
   - Major equipment purchases
   - Manufacturing capacity expansions
   
2. **Strategic Investments**:
   - M&A activity
   - Joint ventures
   - Strategic partnerships
   
3. **Technology Investments**:
   - R&D Centers
   - Technology platforms
   - Liquid cooling technology
   - AI infrastructure
   
4. **Customers and Contracts**:
   - Major customer contracts
   - Hyperscaler collaborations

**Data Sources**:
1. **Company News Hubs**
   - Jabil: https://www.jabil.com/news.html
   - Celestica: https://www.celestica.com/news-events
   - Benchmark: https://www.bench.com/news
   - Sanmina: https://www.sanmina.com/news
   - Flex: https://flex.com/news
   
2. **Newswire Platforms**:
   - PR Newswire: https://www.prnewswire.com
   - Business Wire: https://www.businesswire.com
   - GlobeNewswire: https://www.globenewswire.com

**Collection Method**:
- Use company website’s search functionality
- Google News search: `site:jabil.com "data center" OR "AI" OR "CapEx"`
- Collect in reverse chronological order

**Save Format**:
- Filing name: `{company}_{YYYY_MM_DD}_{topic_keyword}.txt`
- Includes: title, date, full text, source URL

---

### E. Analyst Reports (Optional)

**Data Sources**:
1. **University Library Databases**:
   - Bloomberg Terminal
   - FactSet
   - S&P Capital IQ
   
2. **Free Resources**:
   - Seeking Alpha analyst articles
   - Yahoo Finance analyst ratings
   - TipRanks

**Collection Items**:
- [ ] Analyst ratings and target prices
- [ ] Industry analysis reports
- [ ] CapEx forecasts
- [ ] Strategic analysis

---

## Data Collection Workflow

### Step 1: Setup Environment
```bash
cd flex-practicum
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Step 2: Configure SEC Access
Edit `.env` file:
```
SEC_API_USER_AGENT=YourName your.email@example.com
```

### Step 3: Run SEC Filings Download Script
```bash
python src/data_collection/sec_scraper.py --company JBL --years 3
```

### Step 4: Collect Earnings Call Transcripts
```bash
python src/data_collection/earnings_call_scraper.py --company JBL
```

### Step 5: Collect News and Announcements
```bash
python src/data_collection/news_scraper.py --company JBL --start-date 2022-01-01
```

### Step 6: Manually Collect Investor Presentations
- Visit company Investor Relations page
- Download PDF files into corresponding folders
- Maintain transcript metadata

### Step 7: Data Validation
```bash
python src/data_processing/validate_data.py
```

---

## Data Quality Checklist

For each company:
- [ ] At least 10 quarters of earnings call transcripts
- [ ] 3 annual 10-K reports
- [ ] 12 quarterly 10-Q reports
- [ ] At least 20 related 8-K filings
- [ ] At least 5 investor presentations
- [ ] At least 30 press releases
- [ ] All filings have corresponding metadata
- [ ] Text extraction complete without garbling
- [ ] Consistent date format
- [ ] Uniform filing name conventions

---

## Legal and Ethical Notes

1. **Use only publicly available information**
   - All data must be publicly accessible
   - No use of internal or confidential information
   
2. **Comply with Usage Terms**
   - Respect websites’ robots.txt
   - Follow API usage limits
   - Use reasonable scraping rates (avoid server overload)
   
3. **Cite sources**
   - Attribute all data sources for transcripts
   - Properly cite in reports
   
4. **Data Privacy**
   - Do not collect personally identifiable information
   - Focus only on publicly disclosed company-level information

---

## Data Collection Timeline

### Week 1
- [ ] Collect 10-K filings for all 5 companies (3 years)
- [ ] Collect 10-Q filings for all 5 companies (12 quarters)
- [ ] Develop data collection scripts

### Week 2
- [ ] Collect all earnings call transcripts
- [ ] Collect investor presentations
- [ ] Collect related 8-K filings

### Week 3
- [ ] Collect press releases and announcements
- [ ] Data cleaning and standardization
- [ ] Quality checks and validation

---

## Troubleshooting

### Issue: SEC download failure
**Solutions**:
- Check User-Agent setting
- Verify CIK numbers
- Check network connection
- Try manual download for verification

### Issue: PDF text extraction garbling
**Solutions**:
- Try different PDF libraries (PyPDF2, pdfplumber, pdfminer)
- Check if PDF is a scanned image (OCR needed)
- Manually verify original PDF

### Issue: Website scraping blocked
**Solutions**:
- Lower request frequency
- Add User-Agent string
- Use Selenium to simulate browser behavior
- Consider using proxies

---

## Contact and Support

For data collection issues:
1. Check GitHub Issues
2. Refer to project documentation
3. Contact project maintainers