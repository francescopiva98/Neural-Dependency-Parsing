Project Overview
This project explores transition‑based dependency parsing using a modified version of the arc‑eager algorithm with a static oracle, a widely adopted syntactic representation in natural language processing thanks to its balance between linguistic expressivity, annotation cost, and computational efficiency.

The goal is to investigate how different neural architectures influence parsing performance when integrated into a transition‑based framework.

🔧 Methodology
The work is structured into several key components:
- Arc‑eager algorithm with static oracle: formal definition and handling of edge cases where the stack or buffer contain a single element.
- Baseline neural parser: a bi‑LSTM encoder extracts contextual features from input tokens.
- BERT‑based parser: replacement of the bi‑LSTM with transformer‑based contextual embeddings, comparing Multilingual Cased BERT and Latin‑BERT.
- Model comparison: evaluation against state‑of‑the‑art parsers under identical training conditions.
- Conclusions: analysis of strengths, limitations, and future directions.

In both architectures, the next transition is predicted using an MLP fed with the top elements of the stack and the first element of the buffer. Since arc‑eager configurations may lack one of these components, special cases are explicitly handled.

📊 Evaluation
Arc labels are discarded, and performance is measured using Unlabelled Attachment Score (UAS) to ensure a fair comparison across models and languages.

🎯 Repository Purpose
This repository was developed as part of a university NLP course, with the aim of experimenting with neural transition‑based dependency parsing and assessing the impact of contextual embeddings on parsing accuracy.