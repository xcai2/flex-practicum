# Data Collection Progress Report

**Report Date**: January 25, 2026  
**Project**: Flex Practicum - Strategic CapEx Intelligence in Contract Manufacturing  
**Phase**: Phase 1 - Data Aggregation & Cleaning

---

## Executive Summary

This report summarizes the initial data collection efforts for five target companies (Jabil, Celestica, Benchmark Electronics, Sanmina, Flex). We successfully identified and documented access paths to all companies' investor relations resources, earnings call transcripts, SEC filings, and relevant news releases.

---

## Data Collection Summary Table

| Company | Ticker | SEC CIK | Earnings Calls | 10-K | 10-Q | Presentations | News | Status |
|---------|--------|---------|----------------|------|------|---------------|------|--------|
| **Jabil Inc.** | NYSE:JBL | 0000898293 | 8/12 | 4/4 | 12/12 | 8 | 12 | ✅ Good |
| **Celestica Inc.** | NYSE:CLS | 0001030894 | 12/12 | 4/4 | 12/12 | 3 | 7 | ✅ Excellent |
| **Benchmark Electronics** | NYSE:BHE | 0000863436 | 12/12 | 4/4 | 8/12 | 10 | 9 | ⚠️ Partial |
| **Sanmina Corporation** | NASDAQ:SANM | 0000897723 | 12/12 | 4/4 | 8/12 | 10 | 3 | ⚠️ Partial |
| **Flex Ltd.** | NASDAQ:FLEX | 0000866374 | 12/12 | 4/4 | 11/12 | 15 | 7 | ✅ Good |

**Legend**:
- ✅ Excellent: All target data identified
- ✅ Good: Most data identified, minimal gaps
- ⚠️ Partial: Some data missing, requires supplementation

---

## Detailed Company Status

### 1. Jabil Inc. (JBL)

**Investor Relations**: https://investors.jabil.com/

**Data Collection Status**:
- ✅ Earnings Call Transcripts: 8/12 quarters identified with links
- ✅ 10-K Annual Reports: 4 reports (FY2022-FY2025) identified
- ✅ 10-Q Quarterly Reports: 12 reports identified
- ✅ Investor Presentations: 8 presentations identified
- ✅ News Releases: 12 relevant news items identified

**Key Findings**:
Jabil is undergoing a clear strategic pivot, divesting its Mobility business while aggressively investing in the high-growth AI and Data Center sector. Recent acquisitions (Hanley Energy Group, Mikros Technologies) and product launches (J-422G Servers, Silicon Photonics expansion) demonstrate a strong commitment to becoming a key player in AI infrastructure, particularly in power management and liquid cooling solutions.

**Data File Locations**:
- `/data/raw/jabil/jabil_data_summary.md`
- `/data/raw/jabil/earnings_calls/jabil_earnings_calls_links.md`
- `/data/raw/jabil/sec_filings/jabil_sec_filings_links.md`

---

### 2. Celestica Inc. (CLS)

**Investor Relations**: https://corporate.celestica.com/

**Data Collection Status**:
- ✅ Earnings Call Transcripts: 12/12 quarters identified with links
- ✅ 10-K Annual Reports: 4 reports (FY2021-FY2024) identified
- ✅ 10-Q Quarterly Reports: 12 reports identified
- ✅ Investor Presentations: 3 presentations identified
- ✅ News Releases: 7 relevant news items identified

**Key Findings**:
Celestica is experiencing a significant transformation, with growth focus clearly shifting toward the Connectivity and Cloud Solutions (CCS) segment, particularly AI/data center infrastructure. The company is actively launching products such as the SD6300 ultra-high-density storage system to meet hyperscale customers' demands for AI and machine learning workloads. This strategic shift has driven substantial stock price appreciation in 2025, with analysts citing its engineering capabilities and core position in the AI data center ecosystem as a strong "moat."

**Data File Locations**:
- `/data/raw/celestica/celestica_data_summary.md`

---

### 3. Benchmark Electronics, Inc. (BHE)

**Investor Relations**: https://ir.bench.com/overview/default.aspx

**Data Collection Status**:
- ✅ Earnings Call Transcripts: 12/12 quarters identified with links
- ✅ 10-K Annual Reports: 4 reports identified
- ⚠️ 10-Q Quarterly Reports: 8/12 reports identified (4 missing)
- ✅ Investor Presentations: 10 presentations identified
- ✅ News Releases: 9 relevant news items identified

**Key Findings**:
Benchmark Electronics' strategic focus clearly leans toward high-value, high-complexity manufacturing operations and global capacity expansion. The company conducted multiple factory expansions and new facility openings between 2023 and 2025, indicating substantial CapEx investment aimed at supporting its high-value customer base. Investments and partnerships in semiconductors, photonics packaging, and other areas demonstrate active positioning in emerging high-tech fields, with core business transitioning from traditional electronic manufacturing services toward more specialized high-value manufacturing solutions.

**Data File Locations**:
- `/data/raw/benchmark/benchmark_data_summary.md`

**To Be Supplemented**:
- 4 10-Q quarterly reports require further search

---

### 4. Sanmina Corporation (SANM)

**Investor Relations**: https://ir.sanmina.com/overview/default.aspx

**Data Collection Status**:
- ✅ Earnings Call Transcripts: 12/12 quarters identified with links
- ✅ 10-K Annual Reports: 4 reports identified
- ⚠️ 10-Q Quarterly Reports: 8/12 reports identified (4 missing)
- ✅ Investor Presentations: 10 presentations identified
- ⚠️ News Releases: Only 3 identified (more needed)

**Key Findings**:
Sanmina demonstrates clear strategic focus and investment in data center infrastructure and energy business. In 2025, the company significantly enhanced its AI/data center positioning through the acquisition of ZT Systems' data center infrastructure manufacturing business. Additionally, the company announced expansion of its Houston-based energy business facility, indicating continued CapEx investment to support high-growth vertical markets.

**Data File Locations**:
- `/data/raw/sanmina/sanmina_data_summary.md`

**To Be Supplemented**:
- 4 10-Q quarterly reports require further search
- More news releases need to be collected

---

### 5. Flex Ltd. (FLEX) - Control Group

**Investor Relations**: https://investors.flex.com/overview/default.aspx

**Data Collection Status**:
- ✅ Earnings Call Transcripts: 12/12 quarters identified with links
- ✅ 10-K Annual Reports: 4 reports identified
- ✅ 10-Q Quarterly Reports: 11/12 reports identified
- ✅ Investor Presentations: 15 presentations identified (most)
- ✅ News Releases: 7 relevant news items identified

**Key Findings**:
Flex is actively shifting its business focus toward high-value, high-growth areas, particularly data center and artificial intelligence (AI) infrastructure. Through its "Advanced Manufacturing" capabilities, the company focuses on providing complex manufacturing and supply chain solutions for AI and data center customers, including liquid cooling technology announcements prominently featured on the IR website. While Flex continues to support its traditional business, its strategy and capital expenditure allocation clearly favor technology-intensive high-end manufacturing areas to capture AI-driven hardware demand growth.

**Data File Locations**:
- `/data/raw/flex/flex_data_summary.md`

---

## Initial Strategic Insights

### AI/Data Center Investment Trends

Through initial data collection, we observe that all five companies are tilting toward AI/data center infrastructure to varying degrees:

**Aggressive Investors**:
1. **Celestica**: Most explicit AI/data center strategic transformation, with CCS segment becoming primary growth engine
2. **Sanmina**: Major entry into AI data center space through acquisition of ZT Systems business
3. **Jabil**: Active positioning in AI infrastructure through strategic acquisitions and product innovation

**Balanced Strategists**:
4. **Flex**: Strategically increasing AI/data center investment while maintaining traditional business
5. **Benchmark**: Maintaining relative balance between high-value manufacturing and traditional business

### Key Technology Focus Areas

All companies show investment interest in the following areas:
- **Liquid Cooling Technology**: Particularly prominent for Jabil and Flex
- **High-Density Storage**: Celestica's SD6300 system
- **AI Servers**: Jabil's J-422G, Sanmina's ZT Systems business
- **Power Management**: Jabil's Hanley Energy acquisition
- **Photonics/Advanced Semiconductors**: Benchmark's partnership projects

---

## Data Quality Assessment

### Strengths
- ✅ Basic information and investor relations channels confirmed for all companies
- ✅ High earnings call transcript coverage (average 11.2/12)
- ✅ Good 10-K annual report completeness (4/4 for all companies)
- ✅ Substantial investor presentations identified (average 9.2)

### Areas for Improvement
- ⚠️ Some companies' 10-Q quarterly reports need supplementation (Benchmark and Sanmina each missing 4)
- ⚠️ Sanmina news release collection relatively sparse, requires expanded search
- ⚠️ Some earnings call transcripts have links only, full text not yet downloaded

---

## Next Action Plan

### Short-term Tasks (This Week)

1. **Supplement Missing SEC Filings**
   - [ ] Download 4 missing 10-Q reports for Benchmark
   - [ ] Download 4 missing 10-Q reports for Sanmina
   - [ ] Download 1 missing 10-Q report for Flex

2. **Expand News Collection**
   - [ ] Collect more CapEx-related news for Sanmina (target: at least 10 items)
   - [ ] Search 8-K filings for material events for all companies

3. **Download Complete Documents**
   - [ ] Download all identified earnings call transcript PDFs/text
   - [ ] Download all 10-K and 10-Q filings
   - [ ] Download key investor presentations

4. **Data Cleaning and Standardization**
   - [ ] Extract text from PDFs
   - [ ] Standardize date formats
   - [ ] Create structured JSON metadata

### Medium-term Tasks (Next Week)

5. **Deep Content Analysis**
   - [ ] Extract CapEx-related discussions from earnings call transcripts
   - [ ] Extract CapEx figures and business segment breakdowns from 10-K/10-Q
   - [ ] Identify and tag all AI/data center mentions

6. **Establish Database**
   - [ ] Design database schema
   - [ ] Import cleaned data
   - [ ] Build indexes and query interface

---

## Technical Resources and Tools

### Tools Used
- **Search Engine**: For identifying company resources
- **Browser Automation**: Accessing investor relations pages
- **Parallel Processing**: Simultaneously collecting data for five companies

### Recommended Next-step Tools
- **sec-edgar-downloader**: Python library for batch downloading SEC filings
- **pdfplumber/PyPDF2**: PDF text extraction
- **BeautifulSoup/Selenium**: Web scraping
- **Pandas**: Data processing and cleaning

---

## Project File Structure

```
flex-practicum/
├── data/
│   ├── companies_info.md                      # Company basic information
│   ├── companies_data_collection_summary.csv  # Data collection summary (CSV)
│   ├── companies_data_collection_summary.json # Data collection summary (JSON)
│   ├── data_collection_progress_report.md     # This report
│   └── raw/
│       ├── jabil/
│       │   ├── jabil_data_summary.md
│       │   ├── earnings_calls/
│       │   │   └── jabil_earnings_calls_links.md
│       │   ├── sec_filings/
│       │   │   └── jabil_sec_filings_links.md
│       │   ├── investor_presentations/
│       │   └── news/
│       ├── celestica/
│       │   ├── celestica_data_summary.md
│       │   └── [same subfolder structure]
│       ├── benchmark/
│       │   ├── benchmark_data_summary.md
│       │   └── [same subfolder structure]
│       ├── sanmina/
│       │   ├── sanmina_data_summary.md
│       │   └── [same subfolder structure]
│       └── flex/
│           ├── flex_data_summary.md
│           └── [same subfolder structure]
```

---

## Risks and Challenges

### Identified Risks
1. **Data Access Restrictions**: Some earnings call transcripts may require paid access
2. **PDF Quality Issues**: Some PDFs may be scanned images requiring OCR processing
3. **Large Data Volume**: Total data volume expected to exceed 1GB, requiring adequate storage and processing capacity
4. **Time Constraints**: Complete collection and cleaning of all data may require 2-3 weeks

### Mitigation Strategies
- Prioritize free and publicly available data sources
- Prepare multiple PDF processing tools
- Use cloud storage and distributed processing
- Deliver in phases, completing core datasets first

---

## Conclusion

Phase 1 data collection work is progressing smoothly. We have successfully identified and documented primary data sources for the five target companies. Preliminary analysis shows that all companies are investing in AI/data center infrastructure to varying degrees, but investment intensity and strategic focus differ significantly.

Next work priorities:
1. Supplement missing documents
2. Download and clean complete datasets
3. Begin preparation for NLP pipeline development

Expected to complete all raw data download and preliminary cleaning by end of this week.

---

**Report Prepared By**: Manus AI Assistant  
**Review Status**: Pending user confirmation  
**Next Update**: February 1, 2026
