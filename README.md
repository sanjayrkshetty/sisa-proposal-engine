<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=180&section=header&text=Proposal%20Engine&fontSize=42&fontColor=fff&animation=twinkling&fontAlignY=38&desc=5-Agent%20AI%20Pre-Sales%20Pipeline%20%7C%20Discovery%20%E2%86%92%20Proposal%2C%20Automated&descAlignY=58&descSize=15" />
</p>

<p align="center">
  <a href="https://github.com/sanjayrkshetty"><img src="https://img.shields.io/badge/by-@sanjayrkshetty-7C3AED?style=flat-square&logo=github&logoColor=white" /></a>
  &nbsp;
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Groq%20API-F97316?style=flat-square" />
  <img src="https://img.shields.io/badge/Llama%203.3-7289DA?style=flat-square" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" />
</p>

---

Production 5-agent pipeline that automates the full pre-sales cycle — from discovery call notes to client-ready proposal. Built to replace 3–4 hours of manual proposal writing per SISA engagement.

## Architecture

```
DiscoveryAgent → ScopingAgent → PricingAgent → ProposalAgent
                                       ↑
                                  CriticAgent (adversarial review)
```

| Agent | Role |
|-------|------|
| **DiscoveryAgent** | Extracts BANT from discovery notes — budget, authority, timeline, trigger event |
| **ScopingAgent** | Maps requirements to SISA service lines (6 BUs, 22 services) |
| **PricingAgent** | Estimates effort and builds commercial structure |
| **CriticAgent** | Adversarial pass — challenges assumptions, flags scope creep risks before proposal |
| **ProposalAgent** | Synthesises all upstream output into client-facing proposal |

The CriticAgent runs between Pricing and Proposal — it's not a safety net, it's a mandatory commercial review that catches over-promises before they're committed.

## Service coverage

**Pen Testing**: network · web app · mobile · API · cloud · red team  
**Compliance**: PCI DSS v4.0 · ISO/IEC 27001 · SOC 2 · HIPAA  
**DFIR**: IR retainer · forensics · tabletop · threat hunting  
**VA&M**: full vulnerability management lifecycle

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Groq](https://img.shields.io/badge/Groq%20API-F97316?style=flat-square)
![Llama 3.3](https://img.shields.io/badge/Llama%203.3%2070b-7289DA?style=flat-square)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

- **AI**: Groq — `llama-3.3-70b-versatile` (open source, <1s per agent call)
- **Orchestration**: custom multi-agent pipeline — no framework overhead
- **UI**: Streamlit

## Setup

```bash
git clone https://github.com/sanjayrkshetty/proposal-engine
cd proposal-engine
pip install -r requirements.txt
cp .env.example .env   # add GROQ_API_KEY
streamlit run app.py
```

## Why Groq + Llama over OpenAI

Each agent call is <1s on Groq. A full 5-agent pipeline completes in ~4s — interactive, not a background job. Llama 3.3 70b matches GPT-4 class quality on structured extraction tasks at a fraction of the cost.

---

<p align="center">
  Part of <a href="https://github.com/sanjayrkshetty"><strong>@sanjayrkshetty</strong></a>'s AI security portfolio
</p>

<p align="center">
  <a href="https://sanjayrkshetty.vercel.app"><img src="https://img.shields.io/badge/Portfolio-Live-00d97e?style=flat-square&logo=vercel&logoColor=white" /></a>
  &nbsp;
  <a href="https://linkedin.com/in/sanjay-r-k-shetty-1048ba245"><img src="https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin&logoColor=white" /></a>
  &nbsp;
  <a href="https://github.com/sanjayrkshetty"><img src="https://img.shields.io/badge/GitHub-@sanjayrkshetty-181717?style=flat-square&logo=github&logoColor=white" /></a>
  &nbsp;
  <a href="mailto:sanjayrkshetty@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=80&section=footer" />
</p>
