# Flex Practicum: Strategic CapEx Intelligence in Contract Manufacturing

## 项目概述

本项目旨在为Flex公司开发一个基于自然语言处理(NLP)和检索增强生成(RAG)技术的竞争情报分析系统。该系统将分析合同制造业主要竞争对手的资本支出(CapEx)策略,特别关注AI/数据中心投资与传统业务的平衡,帮助Flex做出更明智的战略投资决策。

## 背景

Flex(原Flextronics)是全球领先的多元化制造服务和供应链解决方案提供商。随着生成式AI驱动的基础设施建设需求激增,Flex正在扩展其在电力、计算和液冷技术方面的投资组合。本项目通过分析竞争对手的投资模式,帮助Flex识别市场机会、评估风险敞口,并优化自身的投资策略。

## 分析目标公司

1. **Jabil Inc.** (JBL) - 关注运营扩张和数据中心战略
2. **Celestica Inc.** (CLS) - 分析向硬件平台解决方案的转变
3. **Benchmark Electronics** (BHE) - 调查高性能计算与传统业务的投资平衡
4. **Sanmina Corporation** (SANM) - 审查垂直整合战略和服务器生态系统投资
5. **Flex Ltd.** (FLEX) - 作为对照组进行基准比较

## 项目目标

1. **量化竞争对手焦点**: 确定投资资金流向"AI/数据中心"与"传统"行业的比例
2. **识别风险敞口**: 评估行业对AI支出趋势的集体过度敞口
3. **启用自然语言发现**: 创建直观的RAG应用,支持复杂的战略查询

## 项目阶段

### Phase 1: 数据聚合与清理 (当前阶段)
- 收集过去12个季度的财报电话会议记录
- 获取SEC文件(10-K, 10-Q, 8-K)
- 收集投资者演示文稿和新闻公告
- 清理和标准化文本数据

### Phase 2: NLP管道开发
- 实体提取和情感分析
- CapEx事件检测
- 投资分类(AI/数据中心 vs 传统业务)
- 提示词工程和模型优化

### Phase 3: 应用程序构建
- 实现向量数据库
- 开发RAG检索和生成系统
- 构建聊天机器人界面
- 创建可视化仪表板

### Phase 4: 战略分析与报告
- 使用RAG工具进行战略查询
- 生成竞争格局报告
- 创建风险评估矩阵
- 提供投资建议

## 项目交付成果

1. **竞争情报应用程序**: 功能性Web应用,支持自然语言查询
2. **源代码和文档**: 完整的Python代码仓库及使用文档
3. **战略格局报告**: 演示文稿,总结竞争对手投资态势
4. **风险评估矩阵**: 可视化展示各竞争对手的AI依赖度

## 技术栈

### 数据收集与处理
- Python 3.9+
- BeautifulSoup, Selenium (网页爬取)
- PyPDF2, pdfplumber (PDF处理)
- Pandas (数据处理)

### NLP与机器学习
- OpenAI API / Anthropic Claude
- LangChain / LlamaIndex (RAG框架)
- spaCy, NLTK (文本处理)
- Sentence Transformers (嵌入模型)

### 数据库与存储
- Pinecone / ChromaDB (向量数据库)
- PostgreSQL / SQLite (关系数据库)

### Web应用
- FastAPI (后端)
- React / Streamlit (前端)
- Docker (容器化)

## 项目结构

```
flex-practicum/
├── README.md                          # 项目概述
├── docs/                              # 文档
├── data/                              # 数据目录
│   ├── raw/                           # 原始数据(按公司分类)
│   ├── processed/                     # 处理后的数据
│   └── analysis/                      # 分析结果
├── src/                               # 源代码
│   ├── data_collection/               # 数据收集脚本
│   ├── data_processing/               # 数据处理
│   ├── nlp/                           # NLP管道
│   ├── rag/                           # RAG系统
│   ├── app/                           # Web应用
│   └── analysis/                      # 分析脚本
├── notebooks/                         # Jupyter笔记本
├── reports/                           # 报告输出
├── tests/                             # 测试
└── config/                            # 配置文件
```

## 快速开始

### 环境设置

```bash
# 克隆仓库
git clone https://github.com/xcai2/flex-practicum.git
cd flex-practicum

# 创建虚拟环境
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 安装依赖
pip install -r requirements.txt

# 配置环境变量
cp .env.example .env
# 编辑.env文件,添加API密钥
```

### 数据收集

```bash
# 运行数据收集脚本
python src/data_collection/sec_scraper.py
python src/data_collection/earnings_call_scraper.py
```

### 运行应用

```bash
# 启动后端
cd src/app/backend
uvicorn main:app --reload

# 启动前端(另一个终端)
cd src/app/frontend
npm install
npm start
```

## 数据来源

- **SEC EDGAR**: 官方财务文件
- **公司投资者关系页面**: 财报会议记录和演示文稿
- **Seeking Alpha**: 财报会议记录补充
- **Business Wire / PR Newswire**: 新闻公告

## 开发进度

- [x] 项目规划和需求分析
- [x] GitHub仓库创建和结构搭建
- [ ] Phase 1: 数据收集(进行中)
- [ ] Phase 2: NLP管道开发
- [ ] Phase 3: 应用程序构建
- [ ] Phase 4: 战略分析与报告

## 贡献指南

本项目为学术practicum项目。如需贡献:

1. Fork本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启Pull Request

## 许可证

本项目仅用于教育和研究目的。

## 联系方式

项目维护者: [您的名字]
项目链接: https://github.com/xcai2/flex-practicum

## 致谢

- Flex公司提供项目背景和需求
- 指导教师和同学的支持
- 开源社区的工具和资源
