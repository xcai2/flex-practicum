# Jabil Inc. SEC文件链接

## 公司基本信息
- **CIK**: 0000898293
- **EIN**: 381886260
- **注册州**: Delaware (DE)
- **财年结束**: 08/31
- **SEC EDGAR页面**: https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0000898293

## 10-K 年度报告

### FY2025 (截至2025年8月31日)
- **文件日期**: 预计2025年10月
- **直接链接**: https://www.sec.gov/Archives/edgar/data/898293/000162828025045293/jbl-20250831.htm
- **状态**: 已提交

### FY2024 (截至2024年8月31日)
- **文件日期**: 2024年10月28日
- **直接链接**: https://www.sec.gov/Archives/edgar/data/898293/000162828024043960/jbl-20240831.htm
- **HTML格式**: 可用
- **PDF下载**: 可通过SEC网站下载

### FY2023 (截至2023年8月31日)
- **文件日期**: 2023年10月20日
- **直接链接**: 需要从SEC EDGAR搜索
- **大小**: 约1.1 MB

### FY2022 (截至2022年8月31日)
- **文件日期**: 2022年10月
- **直接链接**: https://www.sec.gov/Archives/edgar/data/898293/000119312522268383/d389587d10k.htm
- **HTML格式**: 可用

### FY2021 (截至2021年8月31日)
- **文件日期**: 2021年10月
- **直接链接**: 需要从SEC EDGAR搜索

## 10-Q 季度报告

### Q1 FY2026 (截至2025年11月30日)
- **文件日期**: 2026年1月9日
- **直接链接**: 需要从最新文件中查找
- **大小**: 约9.71 MB

### Q4 FY2025 (截至2025年8月31日)
- **注**: Q4通常包含在10-K年报中

### Q3 FY2025 (截至2025年5月31日)
- **文件日期**: 2025年7月
- **直接链接**: 需要从SEC EDGAR搜索

### Q2 FY2025 (截至2025年2月28日)
- **文件日期**: 2025年4月
- **直接链接**: 需要从SEC EDGAR搜索

### Q1 FY2025 (截至2024年11月30日)
- **文件日期**: 2025年1月
- **直接链接**: 需要从SEC EDGAR搜索

### Q3 FY2024 (截至2024年5月31日)
- **文件日期**: 2024年7月
- **直接链接**: https://www.sec.gov/Archives/edgar/data/898293/000162828024031429/
- **索引页面**: 可用

### Q2 FY2024 (截至2024年2月29日)
- **文件日期**: 2024年4月
- **直接链接**: 需要从SEC EDGAR搜索

### Q1 FY2024 (截至2023年11月30日)
- **文件日期**: 2024年1月
- **直接链接**: 需要从SEC EDGAR搜索

### Q3 FY2023 (截至2023年5月31日)
- **文件日期**: 2023年7月
- **直接链接**: 需要从SEC EDGAR搜索

### Q2 FY2023 (截至2023年2月28日)
- **文件日期**: 2023年4月
- **直接链接**: 需要从SEC EDGAR搜索

### Q1 FY2023 (截至2022年11月30日)
- **文件日期**: 2023年1月
- **直接链接**: 需要从SEC EDGAR搜索

### Q3 FY2022 (截至2022年5月31日)
- **文件日期**: 2022年7月
- **直接链接**: 需要从SEC EDGAR搜索

### Q2 FY2022 (截至2022年2月28日)
- **文件日期**: 2022年4月
- **直接链接**: 需要从SEC EDGAR搜索

### Q1 FY2022 (截至2021年11月30日)
- **文件日期**: 2022年1月
- **直接链接**: 需要从SEC EDGAR搜索

## 8-K 重大事件报告

### 最近的8-K文件
- **2025年12月17日**: 财报发布
  - 链接: 需要从SEC EDGAR搜索
  - 大小: 约383 KB

### 搜索8-K的关键事件
- 财报发布公告
- 重大合同签订
- 并购活动
- 高管变动
- 工厂开业/关闭
- 重大投资公告

## 其他有用资源

### Jabil投资者关系页面
- **SEC文件**: https://investors.jabil.com/financials/sec-filings/default.aspx
- **年度报告**: https://investors.jabil.com/financials/annual-reports/default.aspx

### 第三方数据库
- **SEC Database**: https://research.secdatabase.com/CIK/898293/Company-Name/JABIL-INC/Symbol/JBL
- **AnnualReports.com**: https://www.annualreports.com/Company/jabil-circuit-inc
- **StockLight**: https://stocklight.com/stocks/us/nyse-jbl/jabil-circuit/annual-reports

## 下载方法

### 使用Python下载
```python
from sec_edgar_downloader import Downloader

# 设置下载器
dl = Downloader("YourName", "your.email@example.com")

# 下载10-K (过去3年)
dl.get("10-K", "JBL", after="2021-09-01", before="2025-12-31", 
       download_details=True)

# 下载10-Q (过去12个季度)
dl.get("10-Q", "JBL", after="2022-01-01", before="2025-12-31",
       download_details=True)

# 下载8-K (过去3年)
dl.get("8-K", "JBL", after="2022-01-01", before="2025-12-31",
       download_details=True)
```

### 手动下载
1. 访问SEC EDGAR: https://www.sec.gov/edgar/searchedgar/companysearch.html
2. 搜索CIK: 0000898293 或公司名: Jabil Inc
3. 选择文件类型和日期范围
4. 下载HTML或PDF格式

## 重点提取章节

### 10-K重点章节
- **Item 1**: Business - 业务描述和战略
- **Item 1A**: Risk Factors - 风险因素
- **Item 7**: MD&A - 管理层讨论与分析
- **Item 8**: Financial Statements - 财务报表(特别关注CapEx)

### 10-Q重点章节
- **Part I, Item 2**: MD&A - 季度管理层讨论
- **Part I, Item 1**: Financial Statements - 季度财务报表

## 数据收集状态
- [ ] 10-K FY2025
- [ ] 10-K FY2024
- [ ] 10-K FY2023
- [ ] 10-K FY2022
- [ ] 10-Q Q1-Q3 FY2025
- [ ] 10-Q Q1-Q3 FY2024
- [ ] 10-Q Q1-Q3 FY2023
- [ ] 10-Q Q1-Q3 FY2022
- [ ] 相关8-K文件
