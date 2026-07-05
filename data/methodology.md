# Methodology

## AI Affordability Index

**Formula:** `AI Affordability Index = GDP per capita / Tokens per word (TPW)`

The index measures the combined burden of linguistic token cost and economic context. A higher index means AI is more affordable for speakers of that language in that country.

## Data sources

### Tokens per word (TPW)

TPW figures are based on modern tokenisers (primarily GPT-4o's o200k_base). Sources:

| Source | Coverage | Date |
|--------|----------|------|
| Petrov et al., NeurIPS 2023 | 17 tokenisers, FLORES-200 corpus | 2023 |
| Ahia et al., EMNLP 2023 | Cost analysis across languages | 2023 |
| Nayeem et al., arXiv:2510.09947 | 6 tokenisers, formal text | 2025 |
| Lundin et al., "The Token Tax", arXiv:2509.05486 | 16 African languages | 2025 |
| Microsoft GPT-4o Indic benchmarks | Indian languages, GPT-4o vs GPT-4 | 2024 |
| arXiv:2510.12389 | 200+ languages, infrastructure bias | 2025 |

### GDP per capita

- Source: World Bank, 2023 figures (current USD)
- Used as a proxy for purchasing power and affordability context

## Assumptions and limitations

1. **TPW varies by model and text type.** Figures represent reasonable central estimates for modern tokenisers on general text. Code, technical text, and poetry may differ.

2. **GDP per capita is a country average.** A software engineer in Bangalore has different purchasing power to a rural Hindi speaker in Bihar. The index captures country-level context only.

3. **Multilingual countries are simplified.** India has 22 official languages; the index shows major languages separately but assigns one GDP figure.

4. **The index measures access cost, not output quality.** Higher TPW also predicts lower accuracy (Lundin et al. 2025), a compounding penalty not captured here.

5. **API pricing vs subscription products differ.** The token penalty manifests differently across usage models.

## Baseline

USA English is used as the baseline (index = 59,091). The "vs USA" column shows how many times less affordable AI is compared to an English speaker in the United States.

## Updates

This dataset will be updated when:
- New tokeniser benchmarks are published (e.g. GPT-5, Llama 5)
- GDP figures are updated (annually)
- Community contributions correct or add language data
