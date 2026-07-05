# AI Affordability Index

How much more do non-English speakers pay to use AI? This index quantifies the combined burden of linguistic token cost and economic context.

> **Live dashboard:** https://vadhoob90.github.io/ai-affordability-index/

## The formula

```
AI Affordability Index = GDP per capita / Tokens per word
```

An English speaker in the USA scores 59,091. A Tamil speaker in India scores 1,000. AI is 59× less affordable.

## Key findings

- **59 languages** across **30+ countries** measured
- Worst gap: **Tigrinya in Eritrea** (382× less affordable than English in USA)
- **Myanmar, Ethiopia, Cambodia** face 130-256× barriers
- Same language, different country: Tamil in Singapore (2.3×) vs Tamil in India (59×)
- The token premium is constant; the ability to absorb it is not

## Data

- `data/languages.csv`: all language-country pairs with TPW, GDP, and index values
- `data/methodology.md`: sources, assumptions, limitations

## Sources

| Source | What it provides |
|--------|-----------------|
| Petrov et al. (NeurIPS 2023) | Fertility ratios across 17 tokenisers |
| Ahia et al. (EMNLP 2023) | Cost analysis, economic inequality framing |
| Nayeem et al. (2025) | 6 tokenisers on formal text, Indian languages |
| Lundin et al. "The Token Tax" (2025) | African languages, quadratic cost scaling |
| Microsoft GPT-4o benchmarks (2024) | Indian language improvements |
| arXiv:2510.12389 (2025) | 200+ languages, infrastructure bias |
| World Bank (2023) | GDP per capita figures |

## Contributing

PRs welcome for:
- Correcting TPW figures with newer measurements
- Adding languages not yet covered
- Updating GDP figures
- Adding new tokeniser benchmark data

Please cite your source in the PR description.

## Licence

Data: [Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/)
Code: MIT

All views are my own.
