# FlexPracticum 项目详细执行计划

## 项目概览
本项目旨在为Flex公司开发一个AI驱动的竞争情报分析系统,通过NLP技术分析合同制造业竞争对手的资本支出策略,特别关注AI/数据中心投资与传统业务的平衡。

---

## 整体项目时间线和阶段划分

### 阶段1: 数据聚合与清理 (Data Aggregation & Cleaning)
**预计时间**: 2-3周

### 阶段2: NLP管道开发 (NLP Pipeline Development)
**预计时间**: 3-4周

### 阶段3: 应用程序构建 (Application Construction)
**预计时间**: 3-4周

### 阶段4: 战略分析与报告 (Strategic Analysis & Reporting)
**预计时间**: 2周

---

## 阶段1详细步骤: 数据聚合与清理

### 1.1 数据收集准备工作
**任务清单**:
- [ ] 确定五家公司的股票代码和官方网站
- [ ] 识别主要数据源(SEC EDGAR、公司投资者关系页面、金融数据平台)
- [ ] 设置数据存储结构和命名规范
- [ ] 准备数据收集工具和脚本

### 1.2 财报电话会议记录收集
**目标**: 每家公司过去12个季度(3年)的记录

**数据源**:
- Seeking Alpha (免费部分记录)
- 公司官方投资者关系页面
- SEC 8-K文件附件
- 金融数据API (如Alpha Vantage, Financial Modeling Prep)

**收集内容**:
- 完整的会议记录文本
- 日期和季度信息
- 管理层准备发言部分
- Q&A环节记录
- 参与的分析师和高管名单

**数据格式**: 
- 原始格式: PDF/HTML
- 处理后格式: JSON/CSV + 纯文本

### 1.3 投资者日演示文稿收集
**数据源**:
- 公司投资者关系页面
- SEC 8-K文件
- 投资者会议网站

**收集内容**:
- 演示文稿PDF
- 视频记录(如有)
- 配套新闻稿

### 1.4 SEC文件收集
**目标文件类型**:
- **10-K** (年度报告): 过去3年
- **10-Q** (季度报告): 过去12个季度
- **8-K** (重大事件报告): 过去3年相关的

**重点提取部分**:
- Item 1: Business (业务描述)
- Item 1A: Risk Factors (风险因素)
- Item 7: MD&A (管理层讨论与分析)
- Item 8: Financial Statements (财务报表 - 特别是CapEx数据)
- 重大公告和新闻稿

**数据源**: SEC EDGAR系统 (https://www.sec.gov/edgar)

### 1.5 新闻稿和公告收集
**关注主题**:
- 新工厂开业或扩建
- 重大设备采购
- 并购活动(M&A)
- 战略合作伙伴关系
- 技术投资和研发中心
- 液冷技术、AI基础设施相关投资

**数据源**:
- 公司新闻中心
- PR Newswire
- Business Wire
- Google News搜索

### 1.6 分析师报告收集(可选)
**数据源**:
- 大学图书馆数据库访问
- 免费分析师报告网站
- 投资平台(如Seeking Alpha)

### 1.7 数据清理和标准化
**清理任务**:
1. **文本提取**: 从PDF/HTML提取纯文本
2. **格式标准化**: 统一日期格式、公司名称、货币单位
3. **去重**: 删除重复内容
4. **结构化**: 将非结构化文本转换为结构化JSON格式
5. **元数据添加**: 添加公司名称、文档类型、日期、来源等元数据
6. **质量检查**: 验证数据完整性和准确性

**输出格式示例**:
```json
{
  "company": "Jabil Inc.",
  "document_type": "earnings_call",
  "date": "2024-Q3",
  "quarter": "Q3",
  "fiscal_year": 2024,
  "source_url": "https://...",
  "sections": {
    "prepared_remarks": "...",
    "qa_session": "...",
    "participants": ["CEO Name", "CFO Name"]
  },
  "raw_text": "...",
  "metadata": {
    "word_count": 5000,
    "collection_date": "2025-01-25"
  }
}
```

---

## 阶段2详细步骤: NLP管道开发

### 2.1 环境设置
**技术栈**:
- Python 3.9+
- LangChain / LlamaIndex (RAG框架)
- OpenAI API / Anthropic Claude / Llama
- spaCy / NLTK (文本预处理)
- Pandas (数据处理)

### 2.2 实体提取开发
**目标实体类型**:
- 公司名称和子公司
- 地理位置(工厂、数据中心位置)
- 技术类型(液冷、AI芯片、服务器等)
- 财务数字(投资金额、CapEx数字)
- 时间表达式(项目时间线)
- 合作伙伴名称

**方法**:
- 使用预训练NER模型
- 开发自定义提示词用于LLM提取
- 建立实体识别规则库

### 2.3 CapEx事件提取
**事件类型定义**:
1. **工厂开业/扩建** (Factory Opening/Expansion)
2. **设备采购** (Equipment Purchase)
3. **并购活动** (M&A Activity)
4. **研发投资** (R&D Investment)
5. **技术升级** (Technology Upgrade)
6. **合作伙伴关系** (Partnership)

**提取信息**:
- 事件类型
- 投资金额
- 地理位置
- 时间线
- 业务领域(AI/数据中心 vs 传统)
- 相关技术

### 2.4 投资分类系统
**分类维度1: 业务类型**
- **AI/数据中心**: 
  - 超大规模数据中心
  - AI训练/推理基础设施
  - 液冷技术
  - 高性能计算(HPC)
  - GPU/AI加速器制造
  
- **传统/非AI**:
  - 医疗设备制造
  - 汽车电子
  - 工业自动化
  - 航空航天
  - 消费电子

**分类维度2: 投资类型**
- 资本密集型(CapEx)
- 运营投资(OpEx)
- 战略投资

### 2.5 情感分析
**分析目标**:
- 管理层对AI/数据中心业务的乐观程度
- 对传统业务的信心水平
- 风险和担忧的表达
- 竞争压力的感知

**方法**:
- 使用LLM进行上下文情感分析
- 开发特定领域的情感词典
- 量化情感得分(-1到+1)

### 2.6 提示词工程
**开发专用提示词模板**:
1. CapEx事件提取提示词
2. 投资分类提示词
3. 情感分析提示词
4. 战略意图识别提示词
5. 风险因素提取提示词

### 2.7 管道测试和验证
- 在样本数据上测试管道
- 人工验证提取准确性
- 迭代改进提示词和规则
- 建立质量指标(准确率、召回率)

---

## 阶段3详细步骤: 应用程序构建

### 3.1 技术架构设计
**系统组件**:
1. **数据存储层**: 向量数据库 + 关系数据库
2. **NLP处理层**: LLM API集成
3. **RAG引擎**: 检索和生成系统
4. **Web应用层**: 用户界面
5. **API层**: 后端服务

**技术选择**:
- **向量数据库**: Pinecone / Weaviate / ChromaDB / FAISS
- **关系数据库**: PostgreSQL / SQLite
- **后端框架**: FastAPI / Flask
- **前端框架**: React / Streamlit / Gradio
- **部署**: Docker + 云服务(AWS/Azure/GCP) 或本地

### 3.2 向量数据库实现
**步骤**:
1. 选择嵌入模型(OpenAI embeddings / Sentence Transformers)
2. 文档分块策略(chunk size, overlap)
3. 创建文档索引
4. 实现语义搜索功能
5. 优化检索性能

**索引结构**:
- 按公司分区
- 按文档类型分区
- 按时间范围分区
- 元数据过滤

### 3.3 RAG系统开发
**检索策略**:
- 语义相似度搜索
- 混合搜索(语义+关键词)
- 重排序(Re-ranking)
- 上下文窗口优化

**生成策略**:
- 引用来源
- 多文档综合
- 置信度评分
- 答案验证

### 3.4 聊天机器人界面开发
**功能需求**:
1. 自然语言查询输入
2. 实时响应生成
3. 来源引用显示
4. 对话历史管理
5. 查询建议和自动完成
6. 结果导出功能

**示例查询**:
- "哪些竞争对手正在北美建设液冷能力?"
- "Jabil在过去两年在AI数据中心上投资了多少?"
- "比较Celestica和Sanmina的CapEx分配策略"
- "识别所有公司在医疗设备领域的投资趋势"

### 3.5 可视化仪表板
**可视化组件**:
1. **投资分布饼图**: AI vs 传统业务
2. **时间序列图**: CapEx趋势
3. **地理热图**: 投资地理分布
4. **竞争对手比较**: 并排对比
5. **风险矩阵**: AI依赖度评估

### 3.6 用户认证和权限
- 基本登录系统
- 查询日志记录
- 使用分析

### 3.7 测试和部署
- 单元测试
- 集成测试
- 用户验收测试
- 性能测试
- 部署到生产环境

---

## 阶段4详细步骤: 战略分析与报告

### 4.1 关键战略问题分析
**核心问题清单**:
1. 每个竞争对手在AI/数据中心vs传统业务的投资比例?
2. 谁在液冷技术上投资最激进?
3. 哪些地理区域是投资热点?
4. 竞争对手的合作伙伴网络如何?
5. 行业整体对AI增长的依赖程度?
6. 是否存在过度投资/泡沫风险?
7. Flex的"白色空间"机会在哪里?
8. 竞争对手的风险敞口如何?

### 4.2 使用RAG工具进行深度查询
- 对每个战略问题进行系统查询
- 收集和验证答案
- 交叉引用多个来源
- 量化发现

### 4.3 数据综合和洞察提取
**分析维度**:
1. **投资强度**: 绝对金额和相对比例
2. **战略方向**: 增长领域vs收缩领域
3. **时间趋势**: 投资加速或减速
4. **地理策略**: 区域扩张模式
5. **技术焦点**: 特定技术投资
6. **合作模式**: 战略联盟和伙伴关系

### 4.4 风险评估矩阵开发
**评估维度**:
- **X轴**: AI/数据中心投资占比
- **Y轴**: 投资增长率
- **气泡大小**: 总CapEx规模
- **颜色**: 风险等级

**风险分类**:
- 🟢 低风险: 平衡投资组合
- 🟡 中风险: 适度AI倾斜
- 🔴 高风险: 过度依赖AI增长

### 4.5 竞争格局报告撰写
**报告结构**:
1. **执行摘要**
   - 关键发现
   - 主要建议
   
2. **行业概览**
   - 市场趋势
   - 技术驱动因素
   
3. **竞争对手深度分析** (每家公司)
   - Jabil Inc.
   - Celestica
   - Benchmark Electronics
   - Sanmina Corporation
   - Flex (基准)
   
4. **比较分析**
   - 投资策略对比
   - 优势和劣势
   
5. **风险评估**
   - 市场过热风险
   - 个别公司风险敞口
   
6. **战略建议**
   - Flex的机会领域
   - 投资平衡建议
   - 风险缓解策略

### 4.6 演示文稿制作
**格式**: PowerPoint/Google Slides

**内容**:
- 视觉化数据
- 关键图表和图形
- 清晰的叙事线
- 可操作的建议

### 4.7 最终交付
**交付清单**:
- ✅ 功能性Web应用程序(本地或云端)
- ✅ 完整源代码仓库(GitHub)
- ✅ 技术文档和用户手册
- ✅ 战略格局报告(PDF)
- ✅ 演示文稿(PPT)
- ✅ 风险评估矩阵(可视化)
- ✅ 数据更新指南

---

## 项目文件夹结构

```
flex-practicum/
├── README.md                          # 项目概述和快速开始
├── docs/                              # 文档目录
│   ├── project_requirements.md        # 项目需求文档
│   ├── data_collection_guide.md       # 数据收集指南
│   ├── api_documentation.md           # API文档
│   └── user_manual.md                 # 用户手册
│
├── data/                              # 数据目录
│   ├── raw/                           # 原始数据
│   │   ├── jabil/                     # Jabil公司数据
│   │   │   ├── earnings_calls/       # 财报电话会议
│   │   │   ├── sec_filings/          # SEC文件
│   │   │   ├── investor_presentations/ # 投资者演示
│   │   │   └── news/                  # 新闻和公告
│   │   ├── celestica/
│   │   ├── benchmark/
│   │   ├── sanmina/
│   │   └── flex/
│   │
│   ├── processed/                     # 处理后的数据
│   │   ├── cleaned_text/              # 清理后的文本
│   │   ├── structured_json/           # 结构化JSON
│   │   └── embeddings/                # 向量嵌入
│   │
│   └── analysis/                      # 分析结果
│       ├── capex_events.csv           # CapEx事件提取
│       ├── investment_classification.csv # 投资分类
│       └── sentiment_scores.csv       # 情感分析结果
│
├── src/                               # 源代码
│   ├── data_collection/               # 数据收集脚本
│   │   ├── sec_scraper.py            # SEC文件爬虫
│   │   ├── earnings_call_scraper.py  # 财报会议爬虫
│   │   └── news_scraper.py           # 新闻爬虫
│   │
│   ├── data_processing/               # 数据处理
│   │   ├── text_cleaner.py           # 文本清理
│   │   ├── pdf_extractor.py          # PDF提取
│   │   └── data_normalizer.py        # 数据标准化
│   │
│   ├── nlp/                           # NLP管道
│   │   ├── entity_extraction.py      # 实体提取
│   │   ├── capex_event_detector.py   # CapEx事件检测
│   │   ├── investment_classifier.py  # 投资分类
│   │   └── sentiment_analyzer.py     # 情感分析
│   │
│   ├── rag/                           # RAG系统
│   │   ├── vector_store.py           # 向量数据库
│   │   ├── retriever.py              # 检索器
│   │   ├── generator.py              # 生成器
│   │   └── rag_pipeline.py           # RAG管道
│   │
│   ├── app/                           # Web应用
│   │   ├── backend/                  # 后端
│   │   │   ├── main.py               # FastAPI主文件
│   │   │   ├── api/                  # API路由
│   │   │   └── models/               # 数据模型
│   │   │
│   │   └── frontend/                 # 前端
│   │       ├── src/                  # React源码
│   │       ├── public/               # 静态资源
│   │       └── package.json
│   │
│   └── analysis/                      # 分析脚本
│       ├── strategic_analysis.py     # 战略分析
│       ├── risk_assessment.py        # 风险评估
│       └── visualization.py          # 可视化
│
├── notebooks/                         # Jupyter笔记本
│   ├── data_exploration.ipynb        # 数据探索
│   ├── nlp_experiments.ipynb         # NLP实验
│   └── analysis_visualization.ipynb  # 分析可视化
│
├── reports/                           # 报告输出
│   ├── strategic_landscape_report.pdf # 战略格局报告
│   ├── presentation.pptx             # 演示文稿
│   └── risk_assessment_matrix.png    # 风险矩阵
│
├── tests/                             # 测试
│   ├── test_data_processing.py
│   ├── test_nlp.py
│   └── test_rag.py
│
├── config/                            # 配置文件
│   ├── config.yaml                   # 主配置
│   └── prompts.yaml                  # 提示词模板
│
├── requirements.txt                   # Python依赖
├── .env.example                       # 环境变量示例
├── .gitignore
└── docker-compose.yml                 # Docker配置
```

---

## 今日任务: 五家公司数据收集

### 目标公司清单
1. **Jabil Inc.** (股票代码: JBL)
2. **Celestica Inc.** (股票代码: CLS)
3. **Benchmark Electronics** (股票代码: BHE)
4. **Sanmina Corporation** (股票代码: SANM)
5. **Flex Ltd.** (股票代码: FLEX)

### 今日收集重点
对每家公司收集以下信息:

#### 基本信息
- 公司全称
- 股票代码
- 官方网站
- 投资者关系页面URL
- 总部位置
- 业务概述

#### 财报电话会议记录
- 过去12个季度的记录(2022 Q1 - 2024 Q4)
- 来源链接
- 下载或保存记录

#### SEC文件
- 最近3份10-K年报(2021, 2022, 2023)
- 最近12份10-Q季报
- 相关8-K重大事件报告

#### 投资者演示
- 最近的投资者日演示文稿
- 季度业绩演示文稿

#### 新闻和公告
- 过去3年的重大新闻稿
- 关于CapEx、工厂扩建、技术投资的公告

---

## 数据收集最佳实践

### 1. 数据来源优先级
1. **官方来源** (最高优先级)
   - 公司投资者关系页面
   - SEC EDGAR
   
2. **可靠的第三方平台**
   - Seeking Alpha
   - Yahoo Finance
   - Financial Modeling Prep
   
3. **新闻聚合**
   - Google News
   - Business Wire
   - PR Newswire

### 2. 数据质量控制
- ✅ 验证数据来源可靠性
- ✅ 检查日期和版本
- ✅ 确保文本完整性
- ✅ 记录收集时间和方法
- ✅ 保留原始文件备份

### 3. 法律和道德考虑
- ✅ 仅使用公开可用的信息
- ✅ 遵守网站使用条款
- ✅ 尊重robots.txt
- ✅ 合理的爬取速率
- ✅ 适当引用来源

### 4. 组织和命名规范
**文件命名格式**:
- 财报会议: `{company}_{YYYY}_Q{Q}_earnings_call.txt`
- SEC文件: `{company}_{YYYY}_{filing_type}.pdf`
- 演示文稿: `{company}_{YYYY_MM_DD}_investor_presentation.pdf`
- 新闻: `{company}_{YYYY_MM_DD}_{topic}.txt`

**示例**:
- `jabil_2024_Q3_earnings_call.txt`
- `celestica_2023_10K.pdf`
- `benchmark_2024_06_15_investor_day.pdf`

---

## 技术工具和资源

### 数据收集工具
- **Python库**: requests, BeautifulSoup, Selenium, scrapy
- **SEC API**: sec-api.io, sec-edgar-downloader
- **财务数据API**: yfinance, Alpha Vantage, Financial Modeling Prep
- **PDF处理**: PyPDF2, pdfplumber, tabula-py

### 开发工具
- **IDE**: VS Code, PyCharm
- **版本控制**: Git, GitHub
- **环境管理**: conda, venv
- **笔记本**: Jupyter Lab

### NLP和ML工具
- **LLM API**: OpenAI, Anthropic, Llama
- **RAG框架**: LangChain, LlamaIndex
- **向量数据库**: Pinecone, Weaviate, ChromaDB
- **NLP库**: spaCy, NLTK, Hugging Face Transformers

---

## 项目成功指标

### 数据质量指标
- 数据完整性: >95%的目标文档收集
- 数据准确性: <5%的提取错误率
- 数据时效性: 涵盖过去3年

### NLP性能指标
- 实体提取准确率: >90%
- CapEx事件识别召回率: >85%
- 分类准确率: >90%

### 应用性能指标
- 查询响应时间: <5秒
- 答案准确性: >85%(人工评估)
- 来源引用率: 100%

### 业务价值指标
- 战略洞察质量(定性评估)
- 决策支持有效性
- 用户满意度

---

## 风险和缓解策略

### 数据收集风险
- **风险**: 数据不可用或访问受限
- **缓解**: 使用多个数据源,准备替代方案

### 技术风险
- **风险**: API限制或成本
- **缓解**: 使用开源替代方案,优化API调用

### 时间风险
- **风险**: 项目延期
- **缓解**: 分阶段交付,优先核心功能

### 质量风险
- **风险**: NLP准确性不足
- **缓解**: 迭代改进,人工验证关键发现

---

## 下一步行动

### 立即行动 (今日)
1. ✅ 创建GitHub仓库
2. ✅ 建立项目文件夹结构
3. ✅ 开始收集五家公司的基本信息
4. ✅ 收集SEC文件链接
5. ✅ 下载最近的财报会议记录

### 本周行动
1. 完成所有原始数据收集
2. 开始数据清理和标准化
3. 设置开发环境
4. 开始NLP管道原型开发

### 本月行动
1. 完成Phase 1和Phase 2
2. 开始RAG系统开发
3. 原型应用演示

---

## 联系和支持
- 项目文档: GitHub Wiki
- 问题追踪: GitHub Issues
- 代码审查: Pull Requests
