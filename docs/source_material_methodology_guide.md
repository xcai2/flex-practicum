# Source Material Methodology Guide

**Author**: Manus AI  
**Date**: January 27, 2026  
**Version**: 1.0

## 1. Introduction

This guide provides a methodology for using different types of source materials in the Flex Practicum project. It outlines the appropriate uses, limitations, and analytical techniques for each source type to ensure a rigorous and credible analysis of competitive CapEx strategies in the AI/data center market.

## 2. Source Material Categorization

We categorize source materials into two main types: **Primary Sources** and **Secondary Sources**. Each has a distinct role in the analysis.

### 2.1. Primary Sources (Official Company Materials)

Primary sources are the most authoritative and should be the foundation of your quantitative analysis and strategic assessments.

| Source Type | Description | Appropriate Uses | Limitations |
|---|---|---|---|
| **SEC Filings (10-K, 10-Q, 8-K)** | Official financial statements, management discussion & analysis (MD&A), and material event disclosures. | - Extracting official CapEx figures<br>- Financial statement analysis<br>- Identifying risk factors<br>- Verifying strategic initiatives | - Lags behind real-time events<br>- Formal language, lacks nuance<br>- CapEx data may not be segmented by business unit |
| **Earnings Call Transcripts** | Direct commentary from CEO, CFO, and other executives during quarterly earnings calls. | - Understanding management sentiment<br>- Identifying strategic priorities<br>- Clarifying financial results<br>- Q&A with analysts provides deeper insights | - Forward-looking statements are not guaranteed<br>- Management may present a biased view<br>- Requires careful interpretation |
| **Investor Presentations** | Official presentations used in investor days, conferences, and earnings calls. | - Visualizing strategic roadmaps<br>- Understanding market positioning<br>- Identifying key growth drivers<br>- Summarizing company strategy | - Highly curated, marketing-oriented<br>- May lack detailed financial data<br>- Focuses on positive aspects |
| **Official Press Releases** | Company-issued announcements on product launches, partnerships, and other events. | - Tracking key business developments<br>- Building a timeline of strategic moves<br>- Understanding product specifications<br>- Identifying new market entries | - Often promotional in tone<br>- May not provide financial details<br>- Limited to specific events |

### 2.2. Secondary Sources (News, Analyst Reports, Market Research)

Secondary sources provide external context, market sentiment, and third-party analysis. They are crucial for qualitative analysis and for validating trends observed in primary sources.

| Source Type | Description | Appropriate Uses | Limitations |
|---|---|---|---|
| **Financial News Articles** | Analysis and commentary from financial journalists (e.g., Yahoo Finance, Investors.com). | - Gauging market sentiment<br>- Understanding investor reactions<br>- Identifying competitive dynamics<br>- Contextualizing company announcements | - May contain factual errors<br>- Can be biased or speculative<br>- Represents a snapshot in time |
| **Analyst Reports & Commentary** | In-depth analysis from investment analysts (e.g., Seeking Alpha, Simply Wall St). | - Understanding valuation perspectives<br>- Identifying key investment theses<br>- Assessing competitive strengths/weaknesses<br>- Gaining expert opinions | - Often behind a paywall<br>- Analyst opinions can be subjective<br>- Models are based on assumptions |
| **Market Research Reports** | Industry-level analysis from firms like Gartner, IDC, or Mordor Intelligence. | - Understanding market size and growth<br>- Identifying industry trends<br>- Assessing market share dynamics<br>- Benchmarking against competitors | - Can be expensive<br>- Data may be aggregated<br>- Methodologies can vary |

## 3. Analytical Methodology

To ensure a robust analysis, use a multi-source triangulation approach. This involves cross-referencing information from different source types to validate findings and build a more complete picture.

### 3.1. Quantitative Analysis (CapEx Strategy)

1. **Data Extraction**: Use SEC filings (10-K, 10-Q) as the primary source for CapEx figures.
2. **Trend Analysis**: Analyze CapEx trends over time (e.g., quarterly, annually) for each company.
3. **Ratio Analysis**: Calculate CapEx as a percentage of revenue or operating cash flow to normalize for company size.
4. **Segmentation**: Use earnings call transcripts and investor presentations to infer how CapEx is allocated across business segments (e.g., CCS vs. ATS).
5. **Cross-Company Comparison**: Benchmark CapEx trends and ratios across all five companies.

### 3.2. Qualitative Analysis (Strategic Positioning)

1. **Thematic Analysis**: Use NLP techniques to identify key themes in earnings call transcripts and news articles (e.g., AI, data center, M&A).
2. **Sentiment Analysis**: Analyze the tone and sentiment of news articles and analyst reports to gauge market perception.
3. **Event Study**: Track the stock price reaction to major announcements (e.g., product launches, M&A) to assess market impact.
4. **Narrative Construction**: Build a strategic narrative for each company by combining information from all sources.

### 3.3. Multi-Source Triangulation Example

**Scenario**: Celestica announces a new AI-focused product (SD6300).

1. **Primary Source (Press Release)**: Extract product specifications, target markets, and official launch date.
2. **Primary Source (Earnings Call)**: Listen for management commentary on the product's expected revenue contribution and impact on CapEx.
3. **Secondary Source (News Article)**: Analyze how the market interprets the announcement and how it compares to competitors' offerings.
4. **Secondary Source (Analyst Report)**: Understand how analysts are factoring the new product into their valuation models and revenue forecasts.

By combining these perspectives, you can build a comprehensive assessment of the new product's strategic significance.

## 4. Data Organization and Citation

- **File Naming Convention**: Use a consistent naming convention for all extracted documents (e.g., `YYYY-MM-DD_source_topic.md`).
- **Data Directory Structure**: Organize files by company and source type in the `data/raw/` directory.
- **Citation**: Always cite the source URL and date for all extracted information. Use Markdown reference-style links for citations in your final report.

## 5. Conclusion

By systematically categorizing and analyzing different source materials, you can produce a credible and insightful report for the Flex Practicum project. Remember to prioritize primary sources for quantitative data and use secondary sources for context and qualitative analysis. Always cross-reference information to ensure accuracy and build a robust analytical framework.

---

### References

[1] Securities and Exchange Commission. "EDGAR Company Search." [https://www.sec.gov/edgar/searchedgar/companysearch.html](https://www.sec.gov/edgar/searchedgar/companysearch.html)

[2] Celestica Inc. "Investor Relations." [https://corporate.celestica.com/](https://corporate.celestica.com/)

[3] Yahoo Finance. [https://finance.yahoo.com/](https://finance.yahoo.com/)

[4] Seeking Alpha. [https://seekingalpha.com/](https://seekingalpha.com/)
