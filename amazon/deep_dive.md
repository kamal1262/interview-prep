Here’s an **upgraded STAR-HR answer** for **Dive Deep**, weaving in your new technical details (MSK, S3, Glue/Athena, A/B testing) while keeping it tight and metrics-driven.

---

## Headline

I dove deep into our property search data at iProperty Group to uncover why **40% of queries (~4 M/month) failed**, then designed a two-phase fix—first rule-based, then ML—that **cut null searches by 50 %**, improved engagement, and reduced backend costs.  
Let me explain in more detail.

---

## S – Situation

In 2017, as a Data Engineer at iProperty Group (Malaysia), I noticed that many of the **~100 M monthly property searches** on our site were returning no results.  
Left unaddressed, this would frustrate **~300 K daily users**, increase compute waste, and harm revenue.

---

## T – Task

Although outside my formal remit, I took ownership to **diagnose the real causes** and build a **scalable, data-driven solution** that would permanently improve search relevance and customer experience.

---

## A – Action

- **Data deep dive.**
    
    - All raw search logs were **published to Amazon MSK and stored in S3 using dynamic partitioning**.
        
    - I queried and aggregated these logs with **AWS Glue and Athena**, surfacing detailed metrics that showed **~40–50 % of queries (~4 M/month) failed** due to typos, local abbreviations (e.g., “PJ” for Petaling Jaya), and inconsistent keywords.
        
- **Two-phase remediation.**
    
    1. **Quick fix (2 weeks):** Built a hard-coded mapping of the top 30–35 misspellings/short forms covering ~80 % of failed queries.
        
    2. **Long-term fix (1.5 months):** Designed and deployed a **machine-learning semantic search model** to handle unseen variations automatically.
        
- **Controlled rollout.**
    
    - Ran a **two-week A/B test**, comparing the ML model to the rule-based mapping.
        
    - When results consistently outperformed the baseline, I led the **full production cutover to the ML approach**.
        

---

## R – Result

- **Null search rate halved**, from ~4 M to ~2 M queries per month.
    
- **Customer experience improved:** users quickly found relevant properties and stayed on the site longer.
    
- **Operational efficiency increased:** fewer failed queries reduced backend compute and storage costs.
    
- Established a **scalable ML framework and streaming ingestion pattern** (MSK → S3 → Glue/Athena) that other teams later adopted.
    

---

## H – Reflection

This project reinforced that **Dive Deep means interrogating primary data with the right tools**.  
By analysing raw event streams and validating with a rigorous **A/B test**, I moved from symptoms to root cause and ensured the long-term solution would stand up in production.  
I now start every investigation by defining data pipelines and success metrics up front, so fixes are **both fast and durable**.

---

✅ **Key Amazon LP Hooks**

- **Dive Deep:** Hands-on log analysis with MSK/S3/Glue/Athena; precise metrics and root-cause isolation.
    
- **Deliver Results:** 50 % null-search reduction and lower infrastructure costs.
    
- **Bias for Action:** Two-week quick fix and decisive ML rollout once validated.
    

This tightened version shows both **technical depth and business impact**, exactly what Amazon looks for under **Dive Deep**.