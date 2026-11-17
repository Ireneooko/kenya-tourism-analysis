# Kenya Tourism Analysis, 1995–2025

![Python](https://img.shields.io/badge/Python-3.x-blue) ![Data](https://img.shields.io/badge/Data-KNBS%20%7C%20World%20Bank-green) ![Notebook](https://img.shields.io/badge/Notebook-Colab-orange)

An analysis of international visitor arrivals and tourism earnings in Kenya, covering the long run (1995–2019), the COVID-19 collapse and the recovery to 2025, with monthly seasonality through March 2026.

## Key findings
- **Arrivals recovered fully.** KNBS counted 2.55 million international arrivals in 2025: +6.2% on 2024 and +25.3% on 2019 (2.04 million). They fell 71.5% in 2020.
- **The mix has shifted.** Holiday travel was 63.3% of arrivals in 2019 and 47.8% in 2025. Business (25.2%) and "Other" (23.7%, including visiting friends and relatives) now carry much more weight.
- **Seasonality is stable.** Arrivals peak in July–August and again in December–January. March–May is the low season. Aug 2025 (277,155) was the busiest month and Mar 2025 (169,178) the quietest.
- **Arrivals and earnings move together but loosely** (correlation 0.70 for 1995–2019, World Bank data).
- **Earnings:** balance-of-payments travel receipts rose from KSh 141.6 bn (2021) to KSh 494.7 bn (2025), about US$1.3 bn to US$3.8 bn at average exchange rates.

## Charts
| | |
|---|---|
| ![Arrivals trend](charts/arrivals_trend.png) | ![Earnings trend](charts/earnings_trend.png) |
| ![Arrivals vs earnings](charts/arrivals_vs_earnings.png) | ![Visitors by purpose](charts/visitors_by_purpose.png) |
| ![Monthly seasonality](charts/monthly_seasonality.png) | ![Year-on-year growth](charts/yoy_growth.png) |

## Repository structure
```
kenya-tourism-analysis/
├── README.md
├── kenya_tourism_analysis.ipynb
├── data/
│   ├── arrivals.csv
│   ├── earnings.csv
│   ├── visitors_by_purpose.csv
│   └── monthly_arrivals.csv
└── charts/   (6 PNG files)
```

## Data sources
| File | Source |
|---|---|
| `arrivals.csv` | World Bank WDI `ST.INT.ARVL` (Kenya, 1995–2019); KNBS Economic Survey 2026, Table 12.2 (2015–2025) |
| `earnings.csv` | World Bank WDI `ST.INT.RCPT.CD` (1995–2019); KNBS Economic Survey 2026, Table 6.16 (BoP travel receipts) and Table 6.19 (exchange rates), 2021–2025 |
| `visitors_by_purpose.csv` | KNBS Economic Survey 2026, Table 12.2 |
| `monthly_arrivals.csv` | KNBS Economic Survey 2026, Table 12.1 (2023–2025); KNBS Leading Economic Indicators March 2026, Table 18 (Jan–Mar 2026) |

Data downloaded/extracted: 17 November 2026. 2025 and 2026 figures are provisional.

## Limitations
- World Bank has no Kenya data after 2019, so the long series is stitched from different sources and definitions.
- World Bank and KNBS arrivals differ for 2015–2019 (e.g. 1.18 m vs 1.46 m in 2015), so they are shown separately, not combined.
- Earnings for 2021–2025 are balance-of-payments *travel receipts* converted to US$ by me. They are not the same measure as the World Bank series, and 2020 is missing.
- Arrivals count international visitors and exclude Kenyans.
