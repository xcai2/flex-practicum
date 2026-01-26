# 数据收集指南

## 目标公司信息

### 1. Jabil Inc. (JBL)
- **官方网站**: https://www.jabil.com
- **投资者关系**: https://investors.jabil.com
- **SEC CIK**: 0000898293
- **股票代码**: NYSE: JBL
- **分析重点**: 运营扩张和数据中心战略

### 2. Celestica Inc. (CLS)
- **官方网站**: https://www.celestica.com
- **投资者关系**: https://www.celestica.com/investors
- **SEC CIK**: 0001000623
- **股票代码**: NYSE: CLS, TSX: CLS
- **分析重点**: 向硬件平台解决方案的转变和超大规模合作伙伴关系

### 3. Benchmark Electronics, Inc. (BHE)
- **官方网站**: https://www.bench.com
- **投资者关系**: https://ir.bench.com
- **SEC CIK**: 0000925036
- **股票代码**: NYSE: BHE
- **分析重点**: 高性能计算与传统医疗/航空航天业务的投资组合

### 4. Sanmina Corporation (SANM)
- **官方网站**: https://www.sanmina.com
- **投资者关系**: https://investor.sanmina.com
- **SEC CIK**: 0001068686
- **股票代码**: NASDAQ: SANM
- **分析重点**: 垂直整合战略和服务器生态系统中的激进举措

### 5. Flex Ltd. (FLEX)
- **官方网站**: https://flex.com
- **投资者关系**: https://investors.flex.com
- **SEC CIK**: 0000866374
- **股票代码**: NASDAQ: FLEX
- **分析重点**: 作为对照组,基准数据准确性和情绪

---

## 数据收集清单

### A. 财报电话会议Transcript (Earnings Call Transcripts)

**时间范围**: past12个quarters (2022 Q1 - 2024 Q4)

**数据源**:
1. **公司Investor Relations Page** (首选)
   - 通常在 "Events & Presentations" 或 "Quarterly Results" 部分
   
2. **Seeking Alpha**
   - URLformat: `https://seekingalpha.com/symbol/{TICKER}/earnings/transcripts`
   - 免费Visit部分Transcript
   
3. **The Motley Fool**
   - 提供部分免费Transcript
   
4. **SEC 8-Kfilings**
   - 有些公司将Transcript作为8-K的附件

**收集内容**:
- [ ] 完整会议Transcript文本
- [ ] 会议Date
- [ ] 财years和quarters
- [ ] 管理层准备发言
- [ ] Q&A环节
- [ ] 参与者名单(高管和分析师)

**保存format**:
- filings名: `{company}_{YYYY}_Q{Q}_earnings_call.txt`
- 元数据: JSONformat保存在同名.jsonfilings中

---

### B. SECfilings (SEC Filings)

**SEC EDGARVisit**: https://www.sec.gov/edgar/searchedgar/companysearch.html

#### B1. 10-K years度报告
**时间范围**: 2021, 2022, 2023 (3years)

**Key Sections**:
- Item 1: Business
- Item 1A: Risk Factors
- Item 7: Management's Discussion and Analysis (MD&A)
- Item 8: Financial Statements and Supplementary Data

**关Note信息**:
- 业务部门细分
- CapEx总额和细分
- 地理分布
- 战略方向
- Risk factors(特别是市场风险)

#### B2. 10-Q quarters报告
**时间范围**: past12个quarters

**Key Sections**:
- Part I, Item 2: MD&A
- Part I, Item 1: Financial Statements

**关Note信息**:
- quartersCapEx
- 业务部门表现
- 重大事件

#### B3. 8-K 重大事件报告
**时间范围**: past3years

**关Note事件类型**:
- Item 1.01: Entry into Material Agreement
- Item 2.02: Results of Operations and Financial Condition
- Item 8.01: Other Events
- 重大收购、工厂开业、战略合作

**收集方法**:
```python
from sec_edgar_downloader import Downloader

dl = Downloader("YourName", "your.email@example.com")

# Download10-K
dl.get("10-K", "JBL", after="2021-01-01", before="2024-12-31")

# Download10-Q
dl.get("10-Q", "JBL", after="2022-01-01", before="2024-12-31")

# Download8-K
dl.get("8-K", "JBL", after="2022-01-01", before="2024-12-31")
```

---

### C. 投资者演示文稿 (Investor Presentations)

**类型**:
1. **投资者日演示** (Investor Day)
2. **quarters业绩演示** (Quarterly Earnings Presentations)
3. **行业会议演示** (Industry Conference Presentations)

**数据源**:
- 公司Investor Relations Page
- SEC 8-K附件
- 投资者会议网站

**收集内容**:
- [ ] PDF演示文稿
- [ ] 配套视频(如有)
- [ ] Press Release
- [ ] 演示Date和场合

**保存format**:
- filings名: `{company}_{YYYY_MM_DD}_{event_type}.pdf`

---

### D. Press Release和公告 (Press Releases)

**关Note主题**:
1. **CapExRelated**:
   - 新工厂开业/扩建
   - 重大设备采购
   - 制造能力扩展
   
2. **战略投资**:
   - M&A Activity(M&A)
   - 合资企业
   - 战略合作伙伴关系
   
3. **技术投资**:
   - 研发中心
   - 技术平台
   - 液冷技术
   - AI基础设施
   
4. **客户和合同**:
   - 重大客户合同
   - 超大规模客户(Hyperscaler)合作

**数据源**:
1. **公司新闻中心**
   - Jabil: https://www.jabil.com/news.html
   - Celestica: https://www.celestica.com/news-events
   - Benchmark: https://www.bench.com/news
   - Sanmina: https://www.sanmina.com/news
   - Flex: https://flex.com/news
   
2. **新闻发布平台**:
   - PR Newswire: https://www.prnewswire.com
   - Business Wire: https://www.businesswire.com
   - GlobeNewswire: https://www.globenewswire.com

**收集方法**:
- 使用公司网站Search功能
- Google NewsSearch: `site:jabil.com "data center" OR "AI" OR "CapEx"`
- 按时间倒序收集

**保存format**:
- filings名: `{company}_{YYYY_MM_DD}_{topic_keyword}.txt`
- 包含: 标题、Date、完整正文、来源URL

---

### E. 分析师报告 (Analyst Reports) - 可选

**数据源**:
1. **大学图书馆数据库**:
   - Bloomberg Terminal
   - FactSet
   - S&P Capital IQ
   
2. **免费资源**:
   - Seeking Alpha分析文章
   - Yahoo Finance分析师评级
   - TipRanks

**收集内容**:
- [ ] 分析师评级和目标价
- [ ] 行业分析报告
- [ ] CapEx预测
- [ ] 战略分析

---

## 数据收集工作流程

### 第一步: 设置环境
```bash
cd flex-practicum
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### 第二步: 配置SECVisit
编辑 `.env` filings:
```
SEC_API_USER_AGENT=YourName your.email@example.com
```

### 第三步: 运行SECfilingsDownload脚本
```bash
python src/data_collection/sec_scraper.py --company JBL --years 3
```

### 第四步: 收集财报会议Transcript
```bash
python src/data_collection/earnings_call_scraper.py --company JBL
```

### 第五步: 收集新闻和公告
```bash
python src/data_collection/news_scraper.py --company JBL --start-date 2022-01-01
```

### 第六步: 手动收集投资者演示
- Visit公司Investor Relations Page
- DownloadPDFfilings到对应filings夹
- Transcript元数据

### 第七步: 数据验证
```bash
python src/data_processing/validate_data.py
```

---

## 数据质量检查清单

对每家公司:
- [ ] 至少10个quarters的财报会议Transcript
- [ ] 3份10-Kyears报
- [ ] 12份10-Q季报
- [ ] 至少20份Related8-Kfilings
- [ ] 至少5份投资者演示文稿
- [ ] 至少30条Press Release
- [ ] 所有filings都有对应的元数据
- [ ] 文本提取完整无乱码
- [ ] Dateformat统一
- [ ] filings命名规范一致

---

## 法律和道德Note意事项

1. **仅使用公开信息**
   - 所有数据必须是公开可获得的
   - 不使用任何内部或机密信息
   
2. **遵守使用条款**
   - 尊重网站的robots.txt
   - 遵守API使用限制
   - 合理的爬取速率(避免过载服务器)
   
3. **引用来源**
   - Transcript所有数据来源
   - 在报告中适当引用
   
4. **数据隐私**
   - 不收集个人身份信息
   - 仅关Note公司层面的公开信息

---

## 数据收集时间表

### 第1周
- [ ] 收集所有5家公司的SEC 10-Kfilings(3years)
- [ ] 收集所有5家公司的SEC 10-Qfilings(12quarters)
- [ ] 建立数据收集脚本

### 第2周
- [ ] 收集所有财报会议Transcript
- [ ] 收集投资者演示文稿
- [ ] 收集Related8-Kfilings

### 第3周
- [ ] 收集Press Release和公告
- [ ] 数据清理和标准化
- [ ] 质量检查和验证

---

## 故障排除

### 问题: SECDownload失败
**解决方案**:
- 检查User-Agent设置
- 验证CIK号码
- 检查网络连接
- 尝试手动Download验证

### 问题: PDF文本提取乱码
**解决方案**:
- 尝试不同的PDF库(PyPDF2, pdfplumber, pdfminer)
- 检查PDF是否为扫描件(需要OCR)
- 手动验证原始PDF

### 问题: 网站爬取被阻止
**解决方案**:
- 降低请求频率
- 添加User-Agent
- 使用Selenium模拟浏览器
- 考虑使用代理

---

## 联系和支持

如有数据收集问题:
1. 查看GitHub Issues
2. 参考项目文档
3. 联系项目维护者
