# Agent says… Data says…: Property Hauz, Microburbs Hackathon 2026

**Task:** A social post on any finding. `demo.mp4` is the finished 35-second vertical post (1080×1920).

**Finding:** Across inner Sydney, a median unit costs between about 6.5 and 10 years of a typical local household's gross income, depending on the suburb. A higher price doesn't come with lower modelled crime or faster past growth. So check the numbers before you talk to an agent.

**Area:** City of Sydney council area only. That's the hackathon key's coverage, so the post says "inner Sydney".

## Every figure in the video and where it comes from

All data comes from the Microburbs Hackathon API (`https://api-ht.microburbs.com.au`), pulled on Saturday 7 November 2026 with team key `team-46`.

| Figure on screen | Value | Calculation | Endpoint(s) |
|---|---|---|---|
| Glebe: 10 years for a unit | 10.2 years | $930,000 median unit ÷ $1,760/wk median household income ÷ 52 | `/v1/suburbs/Glebe (NSW)/market/all` (median_sale_price.unit); `/v1/suburbs/Glebe (NSW)/demographics/income-map` (median_weekly_income) |
| Start at 22, done at 32 | 22 + 10.2 | Starting age 22 is an assumption | as above |
| 37,200 smashed avos | $930,000 ÷ $25 | $25 per serve is an assumption, shown on screen | as above |
| Alexandria: 6.5 years | 6.5 years | $901,000 ÷ $2,650/wk ÷ 52 | `/v1/suburbs/Alexandria/market/all`; `/v1/suburbs/Alexandria/demographics/income-map` |
| "Almost 4 years less" | 3.6 years | 10.2 − 6.5 | derived |
| "Same-ish price" | $930k vs $901k | Glebe vs Alexandria median unit | `market/all` |
| Surry Hills: 4.4× national crime | +336% | 1 + 336/100 | `/v1/suburbs/Surry Hills/crime/summary` (vs_national_pct) |
| Glebe units +37% in 10 years | +37% | Median unit price, first month on or after Aug 2011 → Aug 2021 | `/v1/suburbs/Glebe (NSW)/market/median-sale-price-series` |
| Surry Hills units +83% | +83% | same window | `/v1/suburbs/Surry Hills/market/median-sale-price-series` |
| "Slowest of these five" | Glebe +37% vs Alexandria +76%, Surry Hills +83%, Erskineville +66%, Darlinghurst +62% | same window | `market/median-sale-price-series` |
| Erskineville and Surry Hills: same 7.1 years | 7.07 and 7.08 years | Erskineville $1,110,000 ÷ $3,020/wk ÷ 52; Surry Hills $850,000 ÷ $2,310/wk ÷ 52 | `market/all`; `demographics/income-map` |
| Erskineville 1.5× crime | +52% | 1 + 52/100 | `/v1/suburbs/Erskineville/crime/summary` |
| "About a third of the crime" | 0.35 | 1.52 ÷ 4.36 | derived |

## Assumptions and caveats (also shown on screen)

- "Years of work" uses **gross** median weekly **household** income and assumes every dollar is saved: no tax, spending or interest. It's a comparison tool, not a savings plan.
- Prices are Microburbs modelled medians (`market/all`, as of 25 Oct 2026).
- Crime is a **modelled** rate (model trained on Queensland police mesh-block incidents, 2020–2022), compared with the national median. It isn't a count of NSW police records.
- Past price growth isn't a forecast. Not financial advice.
- The real-estate agent is a generic cartoon and doesn't depict any real person or agency.

## Supporting files

- `script_v6_agent_says_data_says.xlsx`: the shot-by-shot script, the data points with live formulas, and accuracy checks.
- `hours_to_buy_with_crime.csv`: all 29 suburbs, with houses, units, hours, years and crime, plus data-quality notes.
- `suburb_summary.csv`, `pop_vs_price_2011_2021.csv`: wider analysis tables.

Data: Microburbs (microburbs.com.au).
