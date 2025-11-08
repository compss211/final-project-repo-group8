# Consumer Sentiment Across E-Commerce Platforms  
### Amazon · eBay · Lazada · Shein  

**Course:** COMPS 211 Applied Statistics  
**Team:** Team 8 (Jenny Shi, Sihan Li, Zuhui Zhang, Yao Luo)  
**Dataset Source:**  
CSV file downloaded from Google Sheet (≈ 78.6 MB) [→ Original Sheet](https://docs.google.com/spreadsheets/d/1APEZJYJmdaVO0zVpLG-tYFkLP4EpKlPwrodWz2dbDhY/edit?usp=sharing)

---

## 📊 Dataset Overview
- **Total Reviews:** ≈ 315 000  
- **Platforms:** Amazon (99 000), eBay (121 500), Lazada (54 000), Shein (40 500)  
- **Columns:**  
  - `appName` – Platform name  
  - `reviewId` – Unique review identifier  
  - `content` – User review text  
  - `score` – Numeric rating (1–5)  
  - `thumbsUpCount` – Engagement metric  
  - `replyContent` – Seller reply (optional)  

---

## 🔍 Research Question
> How does consumer sentiment differ across major e-commerce platforms, and what themes dominate positive vs negative reviews?

### Sub-Questions
- Are certain platforms more prone to polarized sentiment?  
- Which factors (e.g., shipping, pricing, product quality) are most frequently mentioned?  
- Do negative reviews receive more “helpful” votes than positive ones?  

---

## 🧩 Methods Plan
| Stage | Goal | Methods & Tools | Key Metrics |
|:--|:--|:--|:--|
| 1. Data Cleaning | Remove duplicates, handle missing values | Python (regex), R | % missing resolved |
| 2. Sentiment Analysis | Assign sentiment polarity | NLP Analysis | Sentiment distribution |
| 3. Topic Identification | Detect themes | LDA / word embedding | Top topics per sentiment |
| 4. Cross-Platform Comparison | Compare averages | R (group_by, ANOVA) | Mean sentiment / variance |
| 5. Factor Association | Identify key drivers | Regression / Correlation | r / p-value |
| 6. Visualization | Communicate findings | R Markdown / Tableau | Plots & dashboards |

---

## 📈 Preliminary Findings
- **Amazon:** Lowest avg score (2.75) → highest negative review ratio (53 %)  
- **eBay & Shein:** Highest avg score (≈ 4.0)  
- **Lazada:** Mid score (3.26) but very high reply rate (42 %)  
- Platforms with more seller replies (Lazada, Shein) → fewer negative reviews → better trust  

---

## 🤝 Collaboration Workflow
- All members push code and analysis via GitHub (repo & LFS)  
- Weekly sync to review figures and scripts  
- Shared Google Drive for slides and drafts  

---

## 💡 How to Reproduce
```bash
# Clone project
git clone https://github.com/compss211/final-project-repo-group8.git
cd final-project-repo-group8
git lfs pull
# (Optional) Download raw data from Google Sheet
bash scripts/download_data.sh
