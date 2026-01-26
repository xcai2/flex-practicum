# FlexPracticum Project Analysis Document

## Project Title
**Strategic CapEx Intelligence in Contract Manufacturing**  
Strategic Capital Expenditure Intelligence Analysis (Contract Manufacturing Industry)

## 1. Background of Flex
- **Company Name**: Flex (formerly Flextronics)  
- **Headquarters**: Austin, Texas, USA (registered office in Singapore)  
- **Scale**: Presence in 30 countries, approximately 160,000 employees  
- **Business**: Global leader in diversified manufacturing services and supply chain solutions  
- **Industry Transformation**: Transitioning from traditional EMS (Electronics Manufacturing Services) to "Sketch-to-Scale" solution provider  
- **Service Industries**: Automotive, Healthcare, Cloud/Data Centers, Industrial, etc.  
- **Strategic Focus**: Under the demand driven by generative AI infrastructure, expand the portfolio of power, computing, and liquid cooling technologies, while maintaining stability in traditional core businesses to reduce market volatility risk

## 2. Project Objectives
Develop a competitive intelligence tool based on Natural Language Processing (NLP) to map the capital expenditure (CapEx) landscape in the contract manufacturing industry.

### Key Objectives:
1. **Quantify Competitor Focus**: Identify the proportion of investment fund flows toward "AI/Data Center" programs versus "traditional" industries (healthcare, industrial, automotive)  
2. **Identify Risk Exposure**: Assess the industry's collective overexposure to AI spending trends, helping Flex identify whether competitors are over-leveraged in a potential bubble  
3. **Enable Natural Language Discovery**: Create an intuitive interface that allows the strategy team to pose complex questions (e.g., "Which competitors are building liquid cooling capacity in North America?") without manual data processing

## 3. Five Competitor Companies Analyzed

| Company Name | Analysis Focus |
|--------------|---------------|
| **Jabil Inc.** | Recent operational expansion and data center strategy |
| **Celestica** | Analysis of its shift toward "hardware platform solutions" and hyperscale partnerships |
| **Benchmark Electronics** | Examination of its portfolio across high-performance computing and traditional healthcare/aerospace business |
| **Sanmina Corporation** | Review of its vertical integration strategy and recent aggressive moves in the server ecosystem |
| **Flex (Control)** | Use of Flex’s own public communications to benchmark data accuracy and sentiment |

## 4. Four Phases of Project Execution

### Phase 1: Data Aggregation and Cleaning
- Scrape and compile earnings call transcripts for all 5 target companies over the past 12 quarters (looking for prepared remarks and Q&A)  
- Collect investor day presentations and available analyst reports  
- Clean and standardize text data for NLP ingestion

### Phase 2: NLP Pipeline Development
- Utilize off-the-shelf Large Language Model (LLM) APIs (such as OpenAI, Anthropic, or open source equivalents like Llama) to perform entity extraction and sentiment analysis  
- Develop specific prompts to extract "CapEx events" (e.g., facility openings, machinery purchases, M&A activity)  
- Categorize investments as "AI/Data Center" vs. "Non-AI/Traditional"

### Phase 3: Application Construction
- Build a retrieval-augmented generation (RAG) application  
- Implement vector database to store indexed industry data  
- Create user interface (chatbot style) that accepts natural language queries and returns referenced answers based on ingested documents

### Phase 4: Strategic Analysis and Reporting
- Use the developed tool to answer key strategic questions about competitor focus  
- Synthesize findings into a final strategic report providing Flex with investment balancing and potential market overheating risk recommendations

## 5. Project Deliverables

1. **Competitive Intelligence Application**: Functional local or cloud-hosted web application allowing Flex strategists to query the dataset using natural language  
2. **Source Code and Documentation**: Complete Python/code repository including documentation on how to update the dataset with future earnings call transcripts  
3. **Strategic Landscape Report**: Presentation summarizing investment postures of Jabil, Celestica, Benchmark, and Sanmina, highlighting Flex’s saturated areas and “white space” opportunities  
4. **Risk Assessment Matrix**: Comparative visualization showing each competitor’s estimated dependency on sustained AI growth rates

## 6. Data Requirements List

### Data to be collected for each company:
1. **Earnings Call Transcripts** (past 12 quarters, approximately 3 years)  
   - Management prepared remarks  
   - Q&A session transcripts  

2. **Investor Day Presentations**  
   - Strategic planning documents  
   - Future investment plans  

3. **Analyst Reports** (if available)  
   - Industry analysis  
   - Investment recommendations  

4. **Public Press Releases and Announcements**  
   - Facility openings/expansions  
   - Major equipment purchases  
   - M&A activity  
   - Strategic partnerships  

5. **Annual Reports and 10-K Filings**  
   - Detailed CapEx information  
   - Business segment breakdowns  
   - Risk factors disclosures  

6. **Quarterly Reports and 10-Q Filings**  
   - Quarterly financial data  
   - Management Discussion and Analysis (MD&A)