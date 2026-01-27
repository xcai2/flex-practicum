# Earnings Call Transcript Collection Guide

## Overview

This guide provides strategies and resources for collecting earnings call transcripts for the five companies in the Flex Practicum project: Jabil, Celestica, Benchmark, Sanmina, and Flex.

## Free Public Sources

### 1. Investing.com
- **URL**: https://www.investing.com/news/transcripts/
- **Pros**: 
  - Free access to full transcripts
  - Well-formatted content
  - Recent earnings calls (2024-2025)
  - Includes summary, key takeaways, and full transcript
- **Cons**: 
  - May not have older transcripts (pre-2024)
  - Coverage varies by company
- **How to Access**: 
  - Search for "[Company Name] earnings call transcript"
  - Navigate directly to transcripts section

### 2. Company Investor Relations Pages
- **Pros**: 
  - Official source
  - Audio recordings available (MP3 format)
  - Supporting materials (presentations, press releases)
  - Complete historical archive
- **Cons**: 
  - Audio files require transcription
  - Text transcripts not always provided
- **Company IR Pages**:
  - Jabil: https://investors.jabil.com/events-and-presentations/
  - Celestica: https://corporate.celestica.com/events-and-presentations
  - Benchmark: https://ir.bench.com/events-and-presentations
  - Sanmina: https://investor.sanmina.com/events-and-presentations
  - Flex: https://investors.flex.com/events-and-presentations

### 3. SEC EDGAR Filings
- **URL**: https://www.sec.gov/edgar/searchedgar/companysearch.html
- **Pros**: 
  - Free and official
  - Complete historical data
  - Includes 8-K filings with earnings information
- **Cons**: 
  - Does not include full transcripts
  - Only financial statements and management commentary
- **Useful Filings**:
  - 10-K (Annual Report)
  - 10-Q (Quarterly Report)
  - 8-K (Current Report - earnings announcements)

## Subscription-Based Sources (Require Payment or Trial)

### 1. Seeking Alpha
- **URL**: https://seekingalpha.com/
- **Cost**: Free tier (limited articles/month), Premium ($239/year)
- **Coverage**: Extensive transcript library
- **Quality**: High-quality, well-formatted transcripts

### 2. GuruFocus
- **URL**: https://www.gurufocus.com/
- **Cost**: 7-day free trial, then $599/year
- **Coverage**: Good historical coverage
- **Quality**: Complete transcripts with speaker identification

### 3. MarketScreener
- **URL**: https://www.marketscreener.com/
- **Cost**: Subscription required
- **Coverage**: International coverage
- **Quality**: Professional transcripts

### 4. AlphaSense / Bloomberg Terminal
- **Access**: Usually through university or corporate subscriptions
- **Coverage**: Most comprehensive
- **Quality**: Highest quality, searchable

## Audio Transcription Method

If only audio files are available from company IR pages:

### Using manus-speech-to-text Utility

```bash
# Download audio file from company IR page
wget [audio_file_url] -O earnings_call.mp3

# Transcribe using the pre-installed utility
manus-speech-to-text earnings_call.mp3 > transcript.txt
```

### Alternative: Python with OpenAI Whisper

```python
import openai
from openai import OpenAI

client = OpenAI()  # API key pre-configured

# Transcribe audio file
with open("earnings_call.mp3", "rb") as audio_file:
    transcript = client.audio.transcriptions.create(
        model="whisper-1",
        file=audio_file,
        response_format="text"
    )
    
with open("transcript.txt", "w") as f:
    f.write(transcript)
```

## Recommended Collection Strategy

### Phase 1: Recent Transcripts (2024-2025)
1. Check Investing.com first (free and complete)
2. If not available, check company IR page for audio
3. Transcribe audio using manus-speech-to-text

### Phase 2: Historical Transcripts (2022-2023)
1. Try Seeking Alpha free tier
2. Use GuruFocus 7-day free trial
3. Download audio from company IR and transcribe
4. Use SEC filings as supplementary source

### Phase 3: Comprehensive Collection
1. Consider subscription if many transcripts needed
2. Check university library for database access
3. Contact company IR directly for older transcripts

## Data Organization

Store transcripts in the following structure:

```
data/raw/
├── jabil/
│   └── earnings_calls/
│       ├── jabil_q1_2024_transcript.md
│       ├── jabil_q2_2024_transcript.md
│       └── transcript_sources.md
├── celestica/
│   └── earnings_calls/
│       ├── celestica_q3_2025_transcript.md
│       └── transcript_sources.md
├── benchmark/
│   └── earnings_calls/
├── sanmina/
│   └── earnings_calls/
└── flex/
    └── earnings_calls/
```

## Quality Checklist

For each transcript collected, verify:
- [ ] Complete transcript (not just summary)
- [ ] Speaker identification (CEO, CFO, analysts)
- [ ] Q&A section included
- [ ] Date and quarter clearly identified
- [ ] Source URL documented
- [ ] Saved in markdown format with proper formatting

## Legal and Ethical Considerations

- Earnings call transcripts are generally considered public information
- Always cite the source
- Respect copyright and terms of service
- For academic use, fair use typically applies
- When in doubt, use official company sources

## Troubleshooting

### Problem: Transcript behind paywall
**Solution**: Try audio transcription from company IR page

### Problem: Audio quality poor
**Solution**: Check if company provides higher quality version or try different quarter

### Problem: Old transcripts not available
**Solution**: Use SEC filings (10-K, 10-Q) which contain similar management commentary

### Problem: Company doesn't provide audio
**Solution**: Contact IR department directly or use subscription service

## Next Steps for Practicum Project

1. **Priority**: Collect Q3 2024 and Q4 2024 transcripts for all 5 companies
2. **Historical**: Collect Q2 2023 transcripts (for comparison baseline)
3. **Focus**: Look for mentions of AI, data center, CapEx, and strategic investments
4. **Tools**: Prepare NLP pipeline for analyzing collected transcripts
