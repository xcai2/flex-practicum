# News Releases Collection Guide

**Project:** Flex Practicum - Competitor CapEx Analysis  
**Created:** January 28, 2026  
**Purpose:** Guide for collecting news releases from 5 EMS companies (2022-2026)

---

## Collection Objectives

Focus on news releases related to:
1. **Capital Expenditure (CapEx)** - facility expansions, equipment purchases, manufacturing capacity
2. **AI/Data Center Infrastructure** - investments in AI servers, networking, cooling solutions
3. **Strategic Investments** - acquisitions, partnerships, joint ventures
4. **Technology Platforms** - new product launches, R&D centers
5. **Major Contracts** - hyperscaler partnerships, large customer wins

**Time Range:** 2022 Q1 - 2026 Q1 (approximately 4 years)

---

## Company 1: Celestica Inc. (CLS)

### News Sources
- **Primary:** https://corporate.celestica.com/newsroom
- **Investor Relations:** https://www.celestica.com/investors
- **SEC 8-K Filings:** https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0001000623

### Folder Location
`/home/ubuntu/flex-practicum/data/raw/celestica/news_releases/`

### Key Topics to Track
- Hardware Platform Solutions (HPS) product launches
- Hyperscaler partnerships and wins
- Data center infrastructure investments
- Facility expansions (especially Thailand operations)
- AI networking products (400G, 800G, 1.6T switches)
- Proprietary compute platforms

### Recent Relevant News (2025-2026)
1. **Nov 17, 2025** - Celestica Introduces the SD6300 Platform for Enterprise and AI Applications
2. **Nov 12, 2025** - Spark Partner Program™ Launch
3. **Oct 24, 2025** - From 800G to 1.6T: Re-Architecting Hyperscale Networks
4. **Dec 11, 2025** - The Synergistic Role of 1.6T and AI Networking
5. **Nov 13, 2025** - SD6300 Revolutionizes Data Storage for AI

### Collection Status
- ✅ Folder created
- ✅ Initial summary created
- ⏳ Need to collect full text of 2022-2024 releases
- ⏳ Need to download PDFs of key announcements

---

## Company 2: Jabil Inc. (JBL)

### News Sources
- **Primary:** https://investors.jabil.com/news/default.aspx
- **Press Releases:** https://investors.jabil.com/news-and-events/press-releases
- **SEC 8-K Filings:** https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0000898293

### Folder Location
`/home/ubuntu/flex-practicum/data/raw/jabil/news_releases/`

### Key Topics to Track
- Data center expansion and investments
- AI infrastructure capabilities
- Semiconductor manufacturing investments
- Facility openings/expansions
- Cloud computing partnerships
- Healthcare and automotive diversification

### Recent Relevant News (2026)
1. **Jan 5, 2026** - Jabil Acquires Hanley Energy Group to Support AI Data Center Power Management ⭐
2. **Jan 20, 2026** - Jabil Invests in EHT Semi for Semiconductor Manufacturing ⭐
3. **Jan 15, 2026** - $1 Billion Senior Notes Issuance (potential CapEx funding) ⭐

### Collection Status
- ✅ Folder created
- ✅ Initial summary created
- ⏳ Need to collect 2022-2025 releases
- ⏳ Download full text of key acquisitions and investments

### Notes
- Jabil has made significant AI/data center moves in early 2026
- Focus on power management and semiconductor capabilities
- $1B financing likely for expansion projects

---

## Company 3: Benchmark Electronics, Inc. (BHE)

### News Sources
- **Primary:** https://ir.bench.com/news-releases
- **Investor Relations:** https://ir.bench.com
- **SEC 8-K Filings:** https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0000925036

### Folder Location
`/home/ubuntu/flex-practicum/data/raw/benchmark/news_releases/`

### Key Topics to Track
- High-performance computing (HPC) investments
- Medical device manufacturing balance
- Aerospace and defense programs
- Facility expansions
- Technology acquisitions
- Customer diversification strategy

### Collection Status
- ✅ Folder created
- ⏳ Need to collect news releases (2022-2026)
- ⏳ Website access may require manual navigation

### Notes
- Benchmark focuses on portfolio balance between HPC and traditional sectors
- Smaller company, may have fewer press releases
- Check quarterly earnings releases for CapEx announcements

---

## Company 4: Sanmina Corporation (SANM)

### News Sources
- **Primary:** https://investor.sanmina.com/news-releases (URL may vary)
- **Investor Relations:** https://investor.sanmina.com
- **SEC 8-K Filings:** https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0001068686

### Folder Location
`/home/ubuntu/flex-practicum/data/raw/sanmina/news_releases/`

### Key Topics to Track
- Server ecosystem investments
- AI server manufacturing
- Vertical integration initiatives
- Data center infrastructure
- Cloud infrastructure partnerships
- Facility expansions

### Collection Status
- ✅ Folder created
- ⏳ Need to verify correct investor relations URL
- ⏳ Need to collect news releases (2022-2026)

### Notes
- Sanmina has been aggressive in server ecosystem
- Focus on vertical integration strategy
- May have significant AI server announcements

---

## Company 5: Flex Ltd. (FLEX) - Control Group

### News Sources
- **Primary:** https://investors.flex.com/news-releases
- **Investor Relations:** https://investors.flex.com
- **SEC 8-K Filings:** https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0000866374

### Folder Location
`/home/ubuntu/flex-practicum/data/raw/flex/news_releases/`

### Key Topics to Track
- AI/data center vs. traditional manufacturing balance
- Strategic positioning announcements
- Facility investments
- Technology partnerships
- Business segment performance
- Diversification initiatives

### Collection Status
- ✅ Folder created
- ⏳ Need to collect news releases (2022-2026)

### Notes
- Flex serves as control/benchmark group
- Important to track their strategic positioning
- Compare their CapEx allocation vs. competitors

---

## Collection Methodology

### Approach 1: Manual Browser Collection (Recommended for Quality)
1. Navigate to each company's news page
2. Filter by year (2022, 2023, 2024, 2025, 2026)
3. Identify relevant releases based on keywords
4. Download full text or save as markdown
5. Create metadata file with date, title, URL, relevance tags

### Approach 2: SEC 8-K Filings (Reliable but Limited)
1. Access SEC EDGAR for each company
2. Download 8-K filings (material events)
3. Extract press releases from exhibits
4. Focus on Item 8.01 (Other Events) and Item 2.02 (Results of Operations)

### Approach 3: Automated Scraping (Technical, May Be Blocked)
1. Use Python with requests/BeautifulSoup
2. Implement rate limiting and respectful scraping
3. Handle anti-bot protections (may require Selenium)
4. Parse HTML structure (varies by company)

### Recommended Hybrid Approach
1. Use SEC 8-K filings for major announcements
2. Manual browser collection for company news pages
3. Cross-reference with earnings call transcripts
4. Focus on 10-15 most relevant releases per company

---

## Keyword Filter List

### Primary Keywords (High Priority)
- CapEx, capital expenditure, capital investment
- Facility, plant, manufacturing site, expansion
- AI, artificial intelligence, machine learning
- Data center, hyperscale, cloud infrastructure
- Acquisition, acquires, merger
- Partnership, collaboration, joint venture
- Investment, invests in

### Secondary Keywords (Medium Priority)
- Server, networking, compute, storage
- Semiconductor, chip, silicon
- Power management, cooling, thermal
- Capacity expansion, production increase
- Technology platform, product launch
- R&D center, innovation hub
- Customer win, contract award

### Sector-Specific Keywords
- Hyperscaler (AWS, Google, Microsoft, Meta)
- GPU, TPU, accelerator
- 400G, 800G, 1.6T (networking speeds)
- Liquid cooling, immersion cooling
- Rack integration, full-rack solution
- HPS (Hardware Platform Solutions)

---

## File Naming Convention

### Format
`{company}_{YYYY_MM_DD}_{short_description}.md`

### Examples
- `celestica_2025_11_17_sd6300_platform_launch.md`
- `jabil_2026_01_05_hanley_energy_acquisition.md`
- `benchmark_2024_03_15_facility_expansion_texas.md`

### Metadata Template (JSON)
```json
{
  "company": "Celestica Inc.",
  "ticker": "CLS",
  "date": "2025-11-17",
  "title": "Celestica Introduces the SD6300 Platform",
  "url": "https://corporate.celestica.com/newsroom/...",
  "type": "Product Launch",
  "relevance": "high",
  "tags": ["AI", "data center", "storage", "product launch"],
  "capex_related": true,
  "ai_related": true,
  "summary": "Launch of SD6300 storage platform targeting enterprise and AI applications"
}
```

---

## Priority Collection List

### High Priority (Collect First)
1. **Jabil** - AI data center acquisitions and investments (2025-2026)
2. **Celestica** - HPS product launches and hyperscaler wins (2024-2025)
3. **All Companies** - Facility expansion announcements (2022-2026)
4. **All Companies** - Major acquisitions related to AI/data center (2022-2026)

### Medium Priority
1. Technology partnership announcements
2. Customer win press releases (if hyperscaler-related)
3. Quarterly earnings press releases (for CapEx guidance)
4. R&D investment announcements

### Lower Priority
1. Executive appointments (unless strategic significance)
2. Dividend announcements
3. General corporate news
4. Industry awards and recognitions

---

## Data Quality Checklist

For each company, aim to collect:
- [ ] At least 20-30 relevant news releases (2022-2026)
- [ ] All major CapEx announcements
- [ ] All AI/data center related announcements
- [ ] All significant acquisitions
- [ ] Key facility expansion news
- [ ] Major customer wins (if disclosed)

---

## Next Steps

1. **Week 1:** Collect Jabil and Celestica news releases (highest AI activity)
2. **Week 2:** Collect Sanmina, Benchmark, and Flex news releases
3. **Week 3:** Cross-reference with SEC 8-K filings
4. **Week 4:** Create analysis summary and extract key metrics

---

## Tools and Resources

### Recommended Tools
- **Browser:** For manual collection with good formatting
- **Python Libraries:** requests, BeautifulSoup4, selenium
- **PDF Tools:** pdfplumber, PyPDF2 (for downloading PDFs)
- **SEC EDGAR:** sec-edgar-downloader Python package

### Useful Commands
```bash
# Create all necessary folders
cd /home/ubuntu/flex-practicum/data/raw
mkdir -p {celestica,jabil,benchmark,sanmina,flex}/news_releases

# Download SEC 8-K filings (example)
python3 -c "
from sec_edgar_downloader import Downloader
dl = Downloader('YourName', 'your.email@example.com')
dl.get('8-K', 'JBL', after='2022-01-01', before='2026-01-31')
"
```

---

## Contact and Support

For questions or issues with data collection:
- Check company investor relations pages first
- Review SEC EDGAR for official filings
- Cross-reference with earnings call transcripts
- Consult project documentation in `/docs` folder

---

## Appendix: Company Comparison Matrix

| Company | AI Focus | CapEx Intensity | Data Center Exposure | Collection Difficulty |
|---------|----------|-----------------|---------------------|----------------------|
| Celestica | High | High | Very High | Medium |
| Jabil | High | High | High | Medium |
| Benchmark | Medium | Medium | Medium | Medium |
| Sanmina | High | High | High | Medium |
| Flex | Medium | Medium | Medium | Medium |

---

**Last Updated:** January 28, 2026  
**Status:** Initial guide created, collection in progress
