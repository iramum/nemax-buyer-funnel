# DLD Service Charge Index — JVC, 2026, Residential

Собрано 19.11.2026 руками из живого индекса DLD (Chrome):
https://dubailand.gov.ae/en/eservices/service-charge-index-overview/service-charge-index#/
вкладка «Service Charge Index», Usage = Residential, Year = 2026 (бюджет 1/1/2026–31/12/2026).

«Total» = General Fund + Reserved Fund, AED за кв. фут в год. Парковка и прочие
Additional Charges в Total не входят.

| Башня (как в DLD) | Управляющая компания | General Fund | Reserved Fund | **Total, AED/sq ft** |
|---|---|---|---|---|
| Belgravia | Deyaar Community Management | 13.57 | 1.41 | **14.98** |
| Bloom Towers | Kingfield OA Management | 13.11 | 2.03 | **15.14** |
| Bloom Heights | Kingfield OA Management | 13.18 | 2.04 | **15.22** |
| Binghatti Gate | Kaizen OA Management | 15.55 | 0.52 | **16.07** |
| Dana Tower | Bunat Al Mustaqbal OA | 16.50 | 1.08 | **17.58** |
| Binghatti Gems | Better Communities OA Management | 17.65 | 0.25 | **17.90** |
| Eaton Place | Deyaar Community Management | 17.18 | 0.75 | **17.93** |
| Binghatti Luna | Stealth OA Management | 17.44 | 1.21 | **18.65** |
| Belgravia Square | Al Rustumani OA Management | 19.84 | 0.55 | **20.39** |
| Cappadocia | Saga International OA Management | 17.25 | 3.17 | **20.42** |

**Медиана (10 башен): 17.74 AED/sq ft** (среднее 17.58 и 17.90).
Среднее: 17.43. Разброс: 14.98–20.42.

Пример: квартира 750 sq ft × 17.74 ≈ AED 13 300 в год.

## Оговорки
- Diamond Views 2: ставки 2026 в индексе нет — не включена.
- Cappadocia в DLD заведена дважды («Jumeirah Village» и «Jumeirah Village Circle»), цифры одинаковые.
- Dana Tower: сверху Additional Charge «Unit A/C» 2.96 AED/sq ft — в Total не входит.
- Парковка (Bloom Towers 423.58, Bloom Heights 472.18, Belgravia 1 260.28, Binghatti Gate 572.00, Eaton Place 1 462.25) — ставка в AED за место, не за фут.
- Арреары («Service charge does not include arrears») в ставку не входят.

## Типичная квартира JVC (DLD Open Data, готовые Flat, янв–окт 2026, сделка = TRANSACTION_NUMBER)
Выгрузка 12.11.2026 (`Nemax/04_RESEARCH:/market_reports/dubai-cash-vs-mortgage-2026-11-12-sources/g1_2026-*.json`), 3 432 сделки.

| Тип | Сделок | Медиана площади, sq ft (IQR) | Медиана цены, AED | AED/sq ft |
|---|---|---|---|---|
| Studio | 875 | 432 (404–488) | 600 000 | 1 393 |
| 1 B/R | 1 966 | 812 (740–908) | 975 000 | 1 240 |
| 2 B/R | 511 | 1 276 (1 156–1 494) | 1 500 000 | 1 165 |

Пример в статье (19.11): 1BR 812 sq ft, AED 975 000; аренда 6,3% = 61 425; SC 812 × 17,74 = 14 405; пустой месяц 5 119; остаток 41 901 → нетто ≈ 4,3%.
