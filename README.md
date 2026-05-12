# BiasAware Dataset

A survey-based dataset capturing **mental health experiences, coping strategies, and perceptions of AI as an emotional support tool** — with a special focus on **bias in AI responses**. Responses were collected primarily from college students in India.

> ⚠️ **Content advisory:** This dataset contains sensitive personal accounts of depression, anxiety, panic attacks, self-harm, loneliness, and other mental health struggles. Please handle the data with care and use it responsibly.

---

## 📊 Overview

| | |
|---|---|
| **Format** | CSV (UTF-8) |
| **Records** | ~508 responses |
| **Collected** | September 2025 onwards |
| **Region** | Primarily India (multiple states & languages) |
| **Source** | Voluntary online survey |

---

## 🎯 Purpose

This dataset was created to study:

- How young adults experience and cope with mental health challenges
- The role of AI chatbots in providing emotional support
- **Bias in AI responses** — including gender stereotypes, insensitive replies, and lack of cultural/emotional understanding
- Gaps between AI-based support and human connection (friends, family, professionals)

It can be used for research in AI fairness, mental health informatics, NLP sentiment analysis, and human-AI interaction studies.

---

## 🗂️ Schema

The CSV contains the following columns:

**Demographics**
- `Timestamp` — submission time
- `Age`
- `Gender`
- `Occupation`
- `Home State`
- `Language`
- `School (If college student)`
- `Program enrolled`

**Mental Health Context**
- `Factors affecting mental health` — multi-select (semicolon-separated)
- `Areas of mental health concerns` — multi-select
- `Escape Hours: Your Safe Space` — open text
- `What's your mental health status?` — scale 1–10
- `How would you scale your sensitivity?` — scale 1–10
- `Biggest reason for feeling low` — open text
- `Kind of comfort or support wished for` — open text
- `Consulted a doctor / took medication or professional guidance` — yes/no/details
- `How did you look after yourself` — open text
- `Point of view about life after overcoming depressed phase` — open text
- `How you faced panic/anxiety/depression symptoms` — open text
- `Easy to share emotions with others?` — yes/maybe/no

**AI Interaction**
- `If you have used AI platforms to share breakdown moments, how did it respond?`
- `Effectiveness of AI vs friends/family/professionals`
- `Helpfulness of AI in managing stress/anxiety`
- `Experienced bias in AI responses (gender stereotypes, insensitivity, etc.)`
- `Suggested improvements — how AI should respond`

**Closing**
- `Few words to share to encourage others`

> Note: Multi-select fields use `;` as a separator. Some free-text fields contain non-ASCII characters (emojis, Devanagari, etc.). Read with `encoding='utf-8'` in pandas.

---

## 🚀 Quick Start

```python
import pandas as pd

df = pd.read_csv("BiasAware.csv", encoding="utf-8")
print(df.shape)
print(df.columns.tolist())

# Example: distribution of mental health status by gender
df.groupby("Gender")["What's your mental health status?"].mean()
```

---

## 🔒 Ethics & Responsible Use

- All responses were voluntarily submitted; no personally identifiable information (PII) such as names, emails, or phone numbers is included.
- **Do not attempt to re-identify respondents.**
- Treat all free-text responses with empathy; some describe traumatic experiences.
- If you build models using this data, please report on biases and limitations transparently.
- This dataset is **not** a clinical instrument and should not be used to diagnose individuals.

If you or someone you know is struggling, please reach out to a mental health professional or a helpline such as **iCall India: +91 9152987821** or **Vandrevala Foundation: 1860-2662-345**.

---

## 📚 Citation

If you use this dataset in your work, please cite it as:

```
[Your Name]. (2025). BiasAware Dataset: A Survey on Mental Health and AI Bias.
GitHub repository, https://github.com/hirakmaa/BiasAwareset
```

---

## 📝 License

This dataset is released under the **MIT License** (see `LICENSE` file).

If you would prefer a license more tailored to datasets, consider [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) — it requires attribution but allows wide reuse, including commercial.

---

## 🤝 Contributing

Found an issue or want to contribute analyses, models, or visualizations built on this dataset? Open an issue or pull request.

---

## 📬 Contact

For questions, collaboration, or removal requests, please open a GitHub issue.
