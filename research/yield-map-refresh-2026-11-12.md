# Dubai Yield Map: перепроверка выпусков на 12.11.2026

> Продолжает `yield-map-refresh-2026-10-13.md` (метод, вариант A) и `yield-map-refresh-2026-10-15.md` (состояние на 15.10). Вопрос этого файла: какие источники выпустили новое между 15.10 и 12.11.2026 и что из-за этого меняется в карте.
> Проверено **12.11.2026**. Инструменты: curl с браузерным UA, PyMuPDF для PDF (страница 10 отчёта E&V отрендерена в картинку и прочитана глазами), WebSearch только чтобы найти URL. Сниппеты поиска как источник не использованы. Сверка «было/стало» шла по копиям 15.10 из `yield-map-refresh-2026-10-15-sources/`.
> Копии сегодняшних загрузок: `04_RESEARCH:/market_reports/yield-map-refresh-2026-11-12-sources/` (HTML, PDF, `txt/` с текстовыми выжимками, `img/ev-q3-p10.png`).
> Текст карты сверяла по `05_OPERATIONS:/sales/buyer-funnel/YIELD_MAP_v3_buyer_2026-10-13.md`, прочитан целиком.
> Уровни: **PRIMARY** = открыт сам документ или страница издателя. **PUBLISHER RELEASE / PAGE** = пресс-релиз или страница продукта издателя, сам отчёт не открыт. **PRESS** = пересказ в СМИ. **NOT FOUND** = искала, не нашла, проверить.

---

## Итог

**Меняется почти всё, на чём стоит таблица.** С 15.10 вышли три новых выпуска:

1. **E&V / Property Monitor**, страница `rental-yield-dubai` переписана **сегодня, 12.11.2026**: «As of November 2026». Доходности по всем 15 районам выросли, у DSO на 1.42 п.п., у JVC на 1.17 п.п. 🔴 **Скачок подозрительный** (§2.2).
2. **E&V, Residential Market Report Q3 2026** (PDF, создан 27.10.2026): Property Monitor **на сентябрь 2026**, по 7 нашим районам. Сентябрьские цифры почти совпадают с августовскими, а ноябрьские от того же E&V через два месяца выше на 0.1–1.2 п.п.
3. **Bayut, Dubai Sales Market Report Q3 2026** (опубликован 30.10.2026). Листинговые доходности по всем нашим районам упали на 0.05–0.56 п.п.

Главное последствие: **в свежих данных листинги Bayut ниже, чем Property Monitor, во всех 11 районах, где есть обе цифры.** Тезис причины 01 («листинг даёт самую высокую цифру, registered ниже») на ноябрьской странице E&V больше не держится. На сентябрьской паре (обе «as of September») он держится для JVC: 7.10% против 6.3%. Предлагаю перестроить причину 01 на эту пару (§4).

Ещё изменилось: CM за Q3 дал цены +0.3% к Q2, аренду обратно на уровне марта, план сдачи на 2027 год 136,100 вместо 162,500 (PRESS, §2.5). ValuStrat October: VPI +0.1% м/м. Mendeley, Savills WCPRI, правило 01.02.2025 и Decree 43/2013 без изменений.

---

## 1. Источник / 15.10 / 12.11 / изменилось ли

| Источник | Состояние на 15.10 | Состояние на 12.11 (чем проверено) | Изменилось? | Уровень |
|---|---|---|---|---|
| **E&V «Dubai Rental Yield in 2026»** (Property Monitor) https://www.engelvoelkers.com/ae/en/resources/rental-yield-dubai | «Updated: 9 Sept 2026», «As of August», средняя 6.34% | Шапка **«Updated: 12 Nov 2026»**, JSON-LD `dateModified 2026-11-12`, sitemap `lastmod 2026-11-12`. «As of November 2026, the average rental yield… was 6.66%». 15 районов, все цифры новые. Блок вилл/таунхаусов разделён на две отдельные таблицы. Полный дифф с копией 15.10 сделан (§2.2) | **Да** | PRIMARY (E&V), Property Monitor через E&V |
| E&V, немецкая версия `/ae/de/ressourcen/mietrendite-dubai` | — | «Aktualisiert: 12 Nov 2026», районы те же, что в EN. ⚠️ В тексте осталось «Stand November 2026 … 6,34 %», а в Key Takeaways 6,66 %: правили наспех | Да | PRIMARY |
| **E&V «Highest ROI properties in Dubai 2026»** https://www.engelvoelkers.com/ae/en/resources/highest-roi-in-dubai-real-estate | «Published: 27 Aug 2026» | **«Updated: 12 Nov 2026»**, `dateModified 2026-11-12`. «As of November 2026»: средние 6.7 / 7.0 / 5.2 / 4.7, IC 8.94, DIP 8.69, DPC 7.99, DSC 8.04, Discovery Gardens 8.58, Palm 4.97, Downtown 5.32, Marina 5.92. Источник по-прежнему не назван. ⚠️ В FAQ осталось «As of August 2026… Dubai Investments Park … approximately 8.7%», в разделе про типы жилья «averaging 4.5% compared with 6.8%» (старые цифры) | **Да** | PRIMARY |
| **E&V Residential Market Report Q3 2026** https://www.engelvoelkers.com/ae/en/research/residential-market-report-q3-2026 , PDF https://a.storyblok.com/f/209096/x/4632cd29cb/engel-voelkers-residential-market-report-q3-2026.pdf | не было (последний H1 2026) | **Новый.** PDF 20 стр., метаданные `creationDate 2026-10-27`. Стр. 9: средние Q3 6.3% / apts 6.6% / TH 5.1% / villas 4.4%. Стр. 10: «Community rental yields, Average gross yield as of September 2026», Source: Property Monitor. Методология: «Property Monitor Intelligence Platform, which contains detailed DLD transaction information» | **Да, новый** | PRIMARY |
| **Bayut Dubai Sales Market Report H1 2026** | «Updated: 15 Oct», 13 цифр | «Updated: 12 Nov, 2026». Переписаны формулировки (ROI → gross rental yield), **все 13 цифр по нашим районам те же** | Нет (по цифрам) | PRIMARY |
| **Bayut Dubai Sales Market Report Q3 2026** https://www.bayut.com/mybayut/dubai-sales-market-report-q3-2026/ | не было | **Новый.** `datePublished 2026-10-30`, `dateModified 2026-11-11`. «gross rental yields, are based on average listing prices and rents in Dubai on Bayut.com… Q3 2026 vs Q2 2026, as of September 2026». Цифры с одним знаком после запятой (7.10%, 6.00%) | **Да, новый** | PRIMARY |
| **Mendeley dataHabibi** DOI 10.17632/rwnn99mdz5 | v1, 03.07.2026 | API `/versions` → `[{"version":1,"publish_date":"2026-07-03","available":true}]`, `/versions/2` → 404 «Cannot GET». CSV скачан, **sha256 `a81917dd…7aebe` тот же**. DataCite `query=datahabibi`: те же 6 DOI, последний от 08.10 | **Нет** | PRIMARY |
| **Property Monitor напрямую** | архив до Dec 2025 | Лента `…/monthly-market-report/feed`: последний выпуск по-прежнему «Monthly Market Report December 2025» | Нет | PRIMARY |
| **Cavendish Maxwell Q3 2026, полный отчёт** | только продажи (релиз 06.10) | Сайт CM за AWS WAF (HTTP 202, `x-amzn-waf-action: challenge`), PDF по шаблону URL прошлого года тоже 202. Полный отчёт пересказан в **Khaleej Times 02.11.2026**: цены, аренда, доходности, сдача, pipeline (§2.5). Релиз CM на Zawya за Q3 только один, от 06.10 (продажи) | **Да**, но только в прессе | PRESS (полный отчёт) / PUBLISHER RELEASE (продажи) |
| **Savills Dubai residential** | Q3 2026, релиз 12.10 | Страница отчёта Savills «Dubai Residential Market Report – Q3 2026», 12.10.2026 (savills.com/research_articles/255800/395342-0), новее не нашла. Цифры аренды Q3 по районам есть только в Khaleej Times 13.10 (§2.5) | **Нет** нового выпуска | PRIMARY (страница) / PRESS (детали) |
| **Savills WCPRI** | H1 2026 от 19.08 | Новее H1 2026 не нашла. H2 2026 по циклу около февраля 2027 | Нет | NOT FOUND (H2) |
| **Knight Frank, Dubai Residential Market Review** | последний Q1 2026 (12.05) | Страница отчёта: последний по-прежнему Q1 2026. В newsroom новое только «412 US$10 million+ homes sell in Dubai… Q1-Q3 2026» (прайм, пересказ в KT 21.10: цены в 10 прайм-районах −5% Q3 к Q2). Обзора рынка Q3 2026 нет | **Нет** обзора | PRIMARY (newsroom) / NOT FOUND (Q3 review) |
| **ValuStrat VPI** | September 2026 (07.10) | **October 2026, страница продукта `published_at 2026-11-10`**: VPI 218.9, +0.1% м/м, villas −4.8% г/г, apartments −7.2% г/г. PDF только по e-mail | **Да** | PUBLISHER PAGE |
| **Правило 01.02.2025** (банки не включают transfer fee и agency fee) | отмены нет | Отмены или пересмотра не нашла. Bayut «New UAE Central Bank Financing Rules for Upfront Property Costs», «Updated: 23 Oct, 2026», по-прежнему: «Effective February 1… banks will no longer include the Dubai Land Department (DLD) registration fees and real estate agent commission fees in mortgage financing». The National 25.01.2025 на месте | **Нет** | PRESS |
| **Decree No. 43 of 2013** (потолок роста аренды) | — | Замены не нашла. Bayut «Understanding Rent Increase Rules in Dubai», «Updated: 16 Oct, 2026»: «Under Decree No. (43) of 2013, legal rent hikes are determined by how much your current rent sits below this hyper-local benchmark», шкала 0 / 5 / 10 / 15 / 20% та же. Smart Rental Index (с 2025) даёт бенчмарк, декрет не отменяет. Текст самого декрета на dlp.dubai.gov.ae по угаданному URL 404, **первоисточник сегодня не открыт** | **Нет** | PRESS / NOT FOUND (первоисточник) |
| dataHabibi, живая страница и CSV | ежедневная пересборка | **Сегодня не проверяла**: в задании нет, в карту (вариант A) не входит | — | — |

---

## 2. Каждая изменившаяся цифра: старое → новое

### 2.1. Listings: Bayut H1 2026 → Bayut Q3 2026

Источник: Bayut, «Bayut's Q3 2026 Report: Dubai Property Sales Trends and Market Performance», https://www.bayut.com/mybayut/dubai-sales-market-report-q3-2026/ , опубл. 30.10.2026, upd. 11.11.2026. **PRIMARY.** Метод тот же, что в H1: листинговые цены и листинговая аренда на Bayut.com, «as of September 2026». Disclaimer: «Figures represent advertised prices only and do not reflect actual transaction prices unless stated».

| Район | H1 2026 | **Q3 2026** | Δ п.п. | Где на странице Q3 |
|---|---|---|---|---|
| International City | 8.79% | **— (апартаменты не опубликованы)** | пропало | «International City and Rukan at 6.30% each» это **виллы**, в квартиры не брать |
| Dubai Sports City | 8.12% | **7.90%** | −0.22 | Affordable apartments |
| Dubai South | 7.24% | **6.90%** | −0.34 | Affordable apartments |
| Discovery Gardens | 9.06% | **8.50%** | −0.56 | Highest rental yields, affordable apts: «followed by Discovery Gardens at 8.50%» |
| Dubai Silicon Oasis | 8.23% | **7.90%** | −0.33 | Affordable apartments |
| Jumeirah Village Circle | 7.15% | **7.10%** | −0.05 | Mid-tier apartments |
| Arjan | 7.10% | **6.90%** | −0.20 | Mid-tier apartments |
| Al Furjan | 7.69% | **— (апартаменты не опубликованы)** | пропало | «Al Furjan 4.50%» это **виллы** |
| Jumeirah Lakes Towers | — | — | — | — |
| Business Bay | 6.29% | **6.00%** | −0.29 | Mid-tier apartments |
| Dubai Marina | 5.88% | **5.60%** | −0.28 | Luxury apartments |
| Downtown Dubai | 5.46% | **5.10%** | −0.36 | Luxury apartments |
| Dubai Hills Estate | 6.30% | **6.00%** | −0.30 | Luxury apartments |
| Palm Jumeirah | 4.48% | **4.40%** | −0.08 | Ultra-luxury apartments |
| Dubai Investments Park (вне таблицы) | — | 9.50% | — | Highest rental yields, affordable |

⚠️ В Q3 Bayut даёт доходность с одним знаком (все значения кончаются на 0). Сравнение с двухзначными цифрами других источников точно до ±0.05.

### 2.2. Registered: Property Monitor August 2026 → **November 2026** (страница E&V) и **September 2026** (отчёт E&V Q3)

**(a) Страница E&V, «Updated: 12 Nov 2026», «As of November»**, https://www.engelvoelkers.com/ae/en/resources/rental-yield-dubai . **PRIMARY для публикации E&V**, Property Monitor через E&V.
**(b) E&V Residential Market Report Q3 2026, стр. 10, «Average gross yield as of September 2026», Source: Property Monitor** (картинка `img/ev-q3-p10.png`). **PRIMARY.** Один знак после запятой, только 10 районов, из наших 7.

| Район | August (09.09) | **September (PDF, 27.10)** | **November (страница, 12.11)** | Δ Aug→Nov | Δ Sep→Nov |
|---|---|---|---|---|---|
| International City | 8.93% | — | **8.94%** | +0.01 | — |
| Dubai Sports City | 7.76% | — | **8.04%** | +0.28 | — |
| Dubai South | 7.21% | 7.2% | **7.28%** | +0.07 | +0.08 |
| Discovery Gardens | — | — | **—** (на этой странице нет; есть на «Highest ROI», §2.3) | — | — |
| Dubai Silicon Oasis | 6.69% | — | **8.11%** | **+1.42** | — |
| Jumeirah Village Circle | 6.36% | 6.3% | **7.53%** | **+1.17** | **+1.23** |
| Arjan | 6.95% | 6.9% | **7.48%** | +0.53 | +0.58 |
| Al Furjan | 7.08% | — | **7.38%** | +0.30 | — |
| Jumeirah Lakes Towers | 6.58% | 6.5% | **6.93%** | +0.35 | +0.43 |
| Business Bay | 5.92% | 5.9% | **6.33%** | +0.41 | +0.43 |
| Dubai Marina | 5.51% | — | **5.92%** | +0.41 | — |
| Downtown Dubai | 5.10% | — | **5.32%** | +0.22 | — |
| Dubai Hills Estate | 5.82% | 5.8% | **6.12%** | +0.30 | +0.32 |
| Palm Jumeirah | 4.58% | 4.6% | **4.97%** | +0.39 | +0.37 |
| Dubai Creek Harbour (вне таблицы) | 5.12% | — | 5.37% | +0.25 | — |
| JBR (вне таблицы) | 5.19% | — | 5.74% | +0.55 | — |
| JGE / JVT / DAMAC Hills, apts (вне таблицы) | — | 6.4% / 6.7% / 7.2% | — | — | — |

Средние по Дубаю (Property Monitor):

| | August (стр. 09.09) | September / Q3 (PDF) | **November (стр. 12.11)** |
|---|---|---|---|
| All residential | 6.34% | 6.3% | **6.66%** |
| Apartments | 6.66% | 6.6% | **6.96%** |
| Townhouses | 5.06% | 5.1% | **5.20%** |
| Villas | 4.45% | 4.4% | **4.67%** |

🔴 **Почему ноябрьским цифрам я не доверяю без вопросов:**
- Сентябрь (отчёт E&V от 27.10) почти равен августу. Ноябрь от того же E&V через 6 недель выше на 0.1–1.2 п.п. По JVC +1.23 п.п. за два месяца. Чтобы так вырасти при неизменной цене, аренда должна подняться почти на 20%. Рынок показывает обратное: Savills Q3 аренда квартир в JVC −10.4% г/г, цены квартир −4.8% к Q2; CM аренда за Q3 вернулась к уровню марта.
- «As of November» опубликовано 12 ноября: полного ноябрьского месяца ещё нет.
- Новая общая средняя 6.66% в точности равна старой средней по квартирам (6.66%). Может быть совпадение, может быть ошибка при правке.
- Страницы правили наспех: на немецкой версии под «Stand November 2026» стоит старая 6,34%, на «Highest ROI» в FAQ осталось «As of August 2026… 8.7%».
- Возможна смена метода (например, только новые договоры). Страница метод не описывает.
Это **мои выводы**, проверить их нечем, кроме вопроса к E&V (Francis Gomez, автор страницы).

### 2.3. Колонка «Aug read» (E&V «Highest ROI»): August → November

Источник: E&V «Highest ROI properties in Dubai 2026», Usman Adrees, «Updated: 12 Nov 2026». **PRIMARY.** Источник данных в статье по-прежнему не назван.

| Район | 27.08 («August») | **12.11 («November»)** | Δ |
|---|---|---|---|
| International City | 8.89% | **8.94%** | +0.05 |
| Dubai Sports City | 7.89% | **8.04%** | +0.15 |
| Discovery Gardens | 7.83% | **8.58%** | +0.75 |
| Dubai Marina | 5.64% | **5.92%** | +0.28 |
| Downtown Dubai | 5.21% | **5.32%** | +0.11 |
| Palm Jumeirah | 4.66% | **4.97%** | +0.31 |
| Dubai Investments Park | 9.61% | **8.69%** | −0.92 |
| Dubai Production City | 8.18% | **7.99%** | −0.19 |
| Средние all / apts / TH / villas | 6.5 / 6.8 / 5.1 / 4.5 | **6.7 / 7.0 / 5.2 / 4.7** | — |

**Закрывает вопрос 2 из §5 файла 13.10.** Теперь все пять общих районов на «Highest ROI» совпадают с ноябрьской страницей Property Monitor до сотой (8.94 / 8.04 / 5.92 / 5.32 / 4.97), а средние 6.7 / 7.0 / 5.2 / 4.7 это округлённые 6.66 / 6.96 / 5.20 / 4.67. Значит, это один источник (Property Monitor). Кроме того, в разделе «Rental Yield vs Capital Appreciation» той же статьи старые 7.83% (Discovery Gardens) и 8.18% (DPC) теперь подписаны **«In H1 2026»**. То есть «августовская» колонка на самом деле была H1 2026.
Вывод для таблицы: третья колонка дублирует вторую. Новое в ней только **Discovery Gardens 8.58%**.

### 2.4. DLD-derived (Mendeley, June 2026) и n

**Без изменений.** Версия 1, файл побайтно тот же (sha256 совпал). Все 14 значений и n как в §2.3 файла 13.10.

### 2.5. Фон рынка (страница 09/06 карты)

| Цифра | Было в карте / на 15.10 | Новое | Источник, дата, URL | Уровень |
|---|---|---|---|---|
| Цены, Q3 к Q2 | CM: нет. Savills: квартиры −4.8% QoQ (like-for-like −1.7%) | **CM: сентябрь AED 1,644 psf, −2.2% г/г («first annual decline since the post-pandemic recovery began»), +0.3% к Q2.** Savills без изменений | Khaleej Times, «Dubai rents: 1 in 5 tenants now pays less…», 02.11.2026, https://www.khaleejtimes.com/business/dubai-rents-1-in-5-tenants-now-pays-less-than-before-as-rentals-ease-on-new-supply | PRESS (пересказ отчёта CM) |
| Аренда, Q3 | процента нет | **CM: AED 77.3 psf в сентябре, +5.5% г/г; «Rates dipped in the second quarter before recovering in the third to return to their March 2026 level».** 21.4% договоров Q3 со снижением аренды (Q1: 4.8%). **Savills: аренда квартир г/г Marina −12.8%, Business Bay −12.2%, JVC −10.4%, Al Furjan −7.5%, Discovery Gardens −4.3%, International City Ph. 2–3 −0.4%** | KT 02.11.2026 (CM) / KT 13.10.2026, https://www.khaleejtimes.com/business/rents-in-dubai-fall-over-12-dubai-marina-business-bay-and-jvc-lead (Savills) | PRESS |
| Доходности CM | H1: «nearly 7%» apts / «5%» villas | **Q3: apartments 6.6%, villas and townhouses 4.9%. DIP 10%, International City 9%, DPC 8%** | KT 02.11.2026 | PRESS |
| Сдано | CM: 24,800 в H1 | **CM: ~38,000 за январь–сентябрь (+41.4% г/г)**; разница даёт ~13,200 за Q3, это мой расчёт. Savills: 26,500 в H1 | KT 02.11 / KT 13.10 | PRESS |
| План на остаток 2026 | CM H1: 47,000 по графику, 14,000–23,500 ожидается в H2 | **CM: 24,400 по графику на остаток 2026, ожидается 7,300–12,200** | KT 02.11.2026 | PRESS |
| **Pipeline 2027 / 2028** | **162,500 / 128,200** (CM H1) — стоит в карте | **CM: 136,100 / 155,700 (вместе 291,800)** | KT 02.11.2026 | PRESS |
| Продажи Q3 | CM: AED 72.6bn, ~34,000 | без изменений; KT 02.11 уточняет 33,900, −13.2% / −2% к Q2 | Zawya, релиз CM 06.10.2026 | PUBLISHER RELEASE |
| ValuStrat | Sept: VPI 218.6, −0.1% м/м, −4.5% г/г; villas −3.4%, apts −6.4% г/г | **Oct: VPI 218.9, +0.1% м/м («edging up for the first time since February»), villas −4.8% г/г, apartments −7.2% г/г** | https://valustrat.com/products/dubai-vpi-residential-values-october-2026 , `published_at 2026-11-10` | PUBLISHER PAGE |
| E&V Q3 (Property Monitor) | — | 33,969 продаж, AED 73.9bn; 173,076 договоров аренды (+23.5% к Q2), new contracts 45.3% (Q2 36.2%); средняя годовая аренда AED 90,200 | PDF E&V Q3, стр. 3, 15 | PRIMARY |
| Knight Frank, прайм | — | цены в 10 прайм-районах −5% Q3 к Q2, «the first decline since 2020» | KT 21.10.2026, https://www.khaleejtimes.com/business/dubais-10-million-plus-home-sales-reach-86-in-q3-2026 | PRESS |
| Savills WCPRI, прайм H2 2026 | «around −10%» | без изменений | savills.com 393831-0, 19.08.2026 | PRIMARY |

⚠️ Противоречия, которые нельзя сглаживать:
- Цены Q3 к Q2: **CM +0.3%**, **Savills −4.8%** (квартиры), ValuStrat в сентябре ещё −0.1% м/м.
- Аренда: **CM +5.5% г/г** по городу, **Savills −10…−13% г/г** по квартирам в Marina, Business Bay, JVC. Разные выборки.
- Аренда за Q3: CM 172,000+, E&V/PM 173,076, Savills 181,900.

---

## 3. Новая таблица на 14 районов (логика варианта A)

Колонки как в варианте A, каждая взята из **последнего** выпуска того же источника:
**Listings** = Bayut Dubai Sales Market Report Q3 2026 (as of September 2026, published 30 Oct 2026) / **Registered** = Property Monitor, as published by Engel & Völkers, «as of November 2026», updated 12 Nov 2026 / **E&V Highest ROI** = Engel & Völkers, updated 12 Nov 2026 / **DLD-derived** = dataHabibi, June 2026, Mendeley Data, CC BY 4.0 / **n** = buildings behind the DLD figure.

| Community | Listings | Registered | E&V Highest ROI | DLD-derived | n |
|---|---|---|---|---|---|
| International City | | 8.94% | 8.94% | 9.98% | 220 |
| Dubai Sports City | 7.90% | 8.04% | 8.04% | 9.54% | 54 |
| Dubai South | 6.90% | 7.28% | | 9.35% | 85 |
| Discovery Gardens | 8.50% | | 8.58% | 9.04% | 88 |
| Dubai Silicon Oasis | 7.90% | 8.11% | | 9.04% | 67 |
| Jumeirah Village Circle | 7.10% | 7.53% | | 8.86% | 213 |
| Arjan | 6.90% | 7.48% | | 8.66% | 70 |
| Al Furjan | | 7.38% | | 8.07% | 51 |
| Jumeirah Lakes Towers | | 6.93% | | 7.87% | 39 |
| Business Bay | 6.00% | 6.33% | | 7.75% | 115 |
| Dubai Marina | 5.60% | 5.92% | 5.92% | 7.71% | 106 |
| Downtown Dubai | 5.10% | 5.32% | 5.32% | 7.43% | 116 |
| Dubai Hills Estate | 6.00% | 6.12% | | 6.99% | 36 |
| Palm Jumeirah | 4.40% | 4.97% | 4.97% | 5.66% | 87 |

Заполнено 46 ячеек, как и было: у Bayut пропали International City и Al Furjan (апартаменты не опубликованы), всё остальное на месте.

🔴 **Предлагаю убрать колонку «E&V Highest ROI»** (§2.3: это тот же Property Monitor, пять из шести значений повторяют соседнюю колонку). Discovery Gardens 8.58% тогда перенести в колонку Registered со сноской «Engel & Völkers, Highest ROI page, 12 Nov 2026». Решение за тобой.

**Разброс по району** (минимум и максимум среди опубликованных; «было» = вариант A на 15.10):

| Community | Lowest | Highest | Spread | Было (15.10) |
|---|---|---|---|---|
| Dubai South | 6.90% | 9.35% | **2.45 pp** | 7.21–9.35, 2.14 |
| Downtown Dubai | 5.10% | 7.43% | **2.33 pp** | 5.10–7.43, 2.33 |
| Dubai Marina | 5.60% | 7.71% | **2.11 pp** | 5.51–7.71, 2.20 |
| Jumeirah Village Circle | 7.10% | 8.86% | **1.76 pp** | 6.36–8.86, 2.50 |
| Arjan | 6.90% | 8.66% | **1.76 pp** | 6.95–8.66, 1.71 |
| Business Bay | 6.00% | 7.75% | **1.75 pp** | 5.92–7.75, 1.83 |
| Dubai Sports City | 7.90% | 9.54% | **1.64 pp** | 7.76–9.54, 1.78 |
| Palm Jumeirah | 4.40% | 5.66% | **1.26 pp** | 4.48–5.66, 1.18 |
| Dubai Silicon Oasis | 7.90% | 9.04% | **1.14 pp** | 6.69–9.04, 2.35 |
| International City | 8.94% | 9.98% | **1.04 pp** | 8.79–9.98, 1.19 |
| Dubai Hills Estate | 6.00% | 6.99% | **0.99 pp** | 5.82–6.99, 1.17 |
| Jumeirah Lakes Towers | 6.93% | 7.87% | **0.94 pp** | 6.58–7.87, 1.29 |
| Al Furjan | 7.38% | 8.07% | **0.69 pp** | 7.08–8.07, 0.99 |
| Discovery Gardens | 8.50% | 9.04% | **0.54 pp** | 7.83–9.06, 1.23 |

Что это значит для текста:
- Самый широкий разрыв теперь **Dubai South, 2.45 п.п.** (было JVC, 2.50). JVC сжался до 1.76.
- **Листинги теперь самая низкая цифра** везде, где она есть: во всех 11 районах с цифрой Bayut минимум даёт Bayut Q3. Самая высокая по-прежнему июньская DLD-derived во всех 14.
- **Bayut ниже Property Monitor во всех 11 районах, где есть обе цифры** (с Discovery Gardens по «Highest ROI»). Это ломает тезис причины 01 «listing yield is the highest likely figure». Если взять сентябрь Property Monitor (тот же «as of September», что у Bayut Q3), картина смешанная: JVC 7.10 против 6.3 и DHE 6.00 против 5.8 (листинг выше), Arjan 6.90 против 6.9 (равно), Dubai South 6.90 против 7.2 и Palm 4.40 против 4.6 (листинг ниже).

---

## 4. Предложения в карте, которые надо поменять

Формулировки по-английски, короткие фразы, may/could, без длинных тире и middot. 🔴 **Собрано под таблицу §3 (ноябрь на странице E&V) и сентябрьскую пару для причины 01.** Если ноябрь отложим до ответа E&V, пункты 2 и 4 меняются (см. варианты ниже).

**1. Стр. 02 INTRO, абзац 2.** Сейчас: «A property portal shows a yield of 8.2%. A market report shows 6.7% for the same area. A third source gives a different number again.» (DSO: Bayut H1 и PM August, оба выпуска заменены.)
Предлагаю JVC, обе цифры «as of September 2026»:
> A property portal shows a yield of 7.1%. A market report shows 6.3% for the same area. A third source gives a different number again.

**2. Стр. 03 THE MAP.** Таблица → §3. Подписи колонок: «Listings, Q3 2026» / «Registered, Nov 2026» / (если оставляем) «E&V, Nov 2026» / «DLD-derived, Jun 2026» / «n». Note без изменений:
> Note: n is the number of buildings behind the DLD figure. Where n is small, the average can move easily.

Если ноябрьскую страницу не берём, Registered = сентябрь из отчёта E&V Q3, но это 7 районов из 14 с одним знаком. Тогда честнее оставить август с пометкой, что страница уже переписана. 🔴 **Решение за тобой.**

**3. Стр. 04 / 01, абзац 2.** Сейчас: «Registered data often shows a lower number. In Dubai Silicon Oasis, listings showed 8.23% in the first half of 2026. Registered data for August 2026 showed 6.69% for the same community.» Обе цифры из заменённых выпусков, а в новых DSO листинг (7.90%) **ниже** registered (8.11%).
> Registered data may show a different number. In Jumeirah Village Circle, listings showed a yield of 7.10% in September 2026. Registered data for the same month showed 6.3%.

> Sources: Bayut Dubai Sales Market Report Q3 2026 (advertised listings, as of September 2026) / Property Monitor, September 2026, in the Engel & Völkers Dubai Residential Market Report Q3 2026 (registered data).

WHAT TO DO, сейчас: «Treat the listing yield as the highest likely figure, not a plan. Find the registered figure for the same community and plan on the lower number.» Первую фразу свежие данные больше не подтверждают. Предлагаю:
> Do not use the listing yield as a plan. Find the registered figure for the same community and plan on the lower of the two.

**4. Стр. 05 / 02, абзац 2.** Сейчас: «In Jumeirah Village Circle, one source published 6.36% and another 8.86% in 2026. On an AED 1.5 million apartment, a gap of 2.5 points is AED 37,500 of rent a year.» 6.36% больше не опубликовано (август заменён), у JVC теперь 7.10–8.86.
Вариант с Downtown (цена AED 1.5 млн для Downtown реалистична, 1-bed у Bayut Q3 AED 2.29M):
> In Downtown Dubai, one source published 5.10% and another 7.43% in 2026. On an AED 1.5 million apartment, a gap of more than 2 points is about AED 35,000 of rent a year.

(2.33 × 15,000 = AED 34,950.)
> Sources: Bayut Dubai Sales Market Report Q3 2026 / dataHabibi, derived from DLD records, June 2026, CC BY 4.0. The AED example is illustrative.

Вариант с самым широким разрывом, Dubai South (6.90 / 9.35, 2.45 × 15,000 = AED 36,750). Но средняя сделка по квартирам в Dubai South у Bayut Q3 AED 995,025, так что пример с AED 1.5 млн там натянут. Рекомендую Downtown.

**5. Стр. 09 / 06, абзац 1.** Сейчас: «In the second quarter of 2026, Dubai prices fell by 2.5% and rents also fell by 2.5%, compared with the first quarter. In the third quarter, average apartment prices fell by a further 4.8%. For the same homes, the fall was 1.7%.» Цифра Savills (−4.8% / −1.7%) верна, но CM за Q3 даёт обратное. Предлагаю показать оба:
> Yield is rent divided by price. In the second quarter of 2026, Dubai prices and rents both fell by about 2.5%, compared with the first quarter. In the third quarter, the picture was mixed. One consultancy recorded a small rise in prices, and rents returned to their March level. Another recorded a 4.8% fall in average apartment prices.

**6. Стр. 09 / 06, абзац 2.** Сейчас: «About 162,500 new homes are expected to be completed in 2027.» У CM в Q3 (PRESS) теперь 136,100:
> About 136,100 new homes are scheduled for completion in 2027. More supply can hold rents down. Savills also expects prime property values in Dubai to fall by around 10% in the second half of 2026.

🔴 **136,100 взято из Khaleej Times 02.11 (PRESS), сам отчёт CM не открыт (WAF).** Если в печать нужен PRIMARY, отчёт надо скачать руками в браузере.
Sources страницы:
> Sources: Cavendish Maxwell, Dubai residential market H1 2026 and Q3 2026 / Savills, Dubai Residential Market Report Q3 2026 / Savills World Cities Prime Residential Index H1 2026.

**7. Стр. 10 / 07 и FAQ стр. 11** («Since 1 February 2025, UAE banks have been told not to include…»). **Без изменений**, отмены нет.

**8. Стр. 07 / 04** («In Dubai, the rental index limits how much the rent can rise when a tenant renews.»). **Без изменений**, Decree 43/2013 и шкала 0–20% в силе (по Bayut 16.10, PRESS).

**9. Стр. 12, финальный дисклеймер.** Сейчас: «Yields in this guide are third-party market figures published between July and October 2026». С Bayut Q3 (30.10), отчётом E&V Q3 (27.10) и страницами E&V (12.11):
> Yields in this guide are third-party market figures published between July and November 2026: past results, not a promise, and not a NEMAX return.

**10. Шапка файла карты (служебная).** «Цифры подставляются из `yield-map-refresh-2026-10-13.md`» → добавить ссылку на этот файл.

---

## 5. Открытые вопросы

1. 🔴 **Ноябрьская страница E&V: брать или нет.** Рост на 0.1–1.4 п.п. за 2–3 месяца при падающей аренде (Savills) не объясняется рынком, сентябрьский отчёт того же E&V показывает август-уровень, «As of November» вышло 12 ноября, на DE-странице и в FAQ «Highest ROI» остались старые цифры. Можно спросить E&V (Francis Gomez / Usman Adrees), что за срез «November» и не менялся ли метод. Я не писала.
2. 🔴 **Причина 01 и её WHAT TO DO.** На ноябрьских данных листинги ниже registered во всех 11 районах. Предложила сентябрьскую пару JVC (7.10 против 6.3) и нейтральное «plan on the lower of the two». Сам заголовок «The yield is based on asking prices, not real sales» остаётся верным: Bayut прямо пишет, что считает по объявлениям.
3. **Колонка «E&V Highest ROI».** Подтверждено, что это тот же Property Monitor. Убрать её и перенести Discovery Gardens 8.58% в Registered?
4. **Пустые ячейки Bayut.** В Q3 нет квартир International City и Al Furjan. Подставлять H1 (8.79 / 7.69) не стала: выпуски нельзя смешивать в одной колонке.
5. **CM Q3 полным отчётом не открыт.** 136,100 на 2027, доходности 6.6 / 4.9, цены +0.3% к Q2, аренда 77.3 psf известны только из Khaleej Times 02.11 (PRESS). Сайт CM за WAF. Скачать PDF руками: `cavendishmaxwell.com/insights/market-reports/residential`.
6. **ValuStrat October** только со страницы продукта (PUBLISHER PAGE). PDF по e-mail. В карту ValuStrat не входит.
7. **Decree 43/2013**: первоисточник (dlp.dubai.gov.ae) сегодня не открылся (угаданный URL 404). Опираюсь на Bayut 16.10.2026 (PRESS).
8. **Правило 01.02.2025**: отмены не нашла. Публичного циркуляра CBUAE по канону нет, сайт CBUAE сегодня не открывала.
9. **Mendeley v2** не вышел. Июньский DLD-derived остаётся единственной колонкой с n, но теперь он **на 5 месяцев старше** остальных колонок. Это само по себе может объяснять, почему он везде самый высокий.
10. **Dubai Investments Park** (вне таблицы): Bayut Q3 9.50%, CM Q3 10%, E&V Nov 8.69%. Разброс сузился до 1.3 п.п. (был 4.89–9.7).
11. **Следующие выпуски:** Property Monitor через E&V (страница обновляется нерегулярно: 09.09, затем 12.11); E&V Q4 report (по циклу Q3 конец января 2027); Bayut annual 2026 (январь 2027); Savills Dubai Q4 (около середины января 2027); WCPRI H2 2026 (около февраля 2027); Knight Frank обзор Q2/Q3 2026 так и не вышел; ValuStrat November (около 10.12).

---

## 6. Источники (копии в `yield-map-refresh-2026-11-12-sources/`)

| Файл | URL | Скачано |
|---|---|---|
| `ev-rental-yield.html` | https://www.engelvoelkers.com/ae/en/resources/rental-yield-dubai | 12.11.2026 |
| `ev-de-mietrendite.html` | https://www.engelvoelkers.com/ae/de/ressourcen/mietrendite-dubai | 12.11.2026 |
| `ev-highest-roi.html` | https://www.engelvoelkers.com/ae/en/resources/highest-roi-in-dubai-real-estate | 12.11.2026 |
| `ev-dubai-housing-market.html` | https://www.engelvoelkers.com/ae/en/resources/dubai-housing-market | 12.11.2026 |
| `ev-ae-sitemap.xml` | https://www.engelvoelkers.com/ae/sitemap.xml | 12.11.2026 |
| `ev-resi-q3-2026.html`, `ev-resi-q3-2026.pdf`, `img/ev-q3-p10.png` (+ p3, p9) | https://www.engelvoelkers.com/ae/en/research/residential-market-report-q3-2026 , https://a.storyblok.com/f/209096/x/4632cd29cb/engel-voelkers-residential-market-report-q3-2026.pdf | 12.11.2026 |
| `bayut-h1.html` | https://www.bayut.com/mybayut/dubai-sales-market-report-h1-2026/ | 12.11.2026 |
| `bayut-q3.html` | https://www.bayut.com/mybayut/dubai-sales-market-report-q3-2026/ | 12.11.2026 |
| `bayut-sitemap_index.xml`, `bayut-post-sitemap*.xml` | https://www.bayut.com/mybayut/sitemap_index.xml | 12.11.2026 |
| `bayut-upfront-costs.html` | https://www.bayut.com/mybayut/changes-upfront-property-costs-dubai/ | 12.11.2026 |
| `bayut-rent-increase.html` | https://www.bayut.com/mybayut/rent-increase-rules-dubai/ | 12.11.2026 |
| `mendeley-versions.json`, `mendeley-v2.json`, `mendeley-dataset.json`, `mendeley-dubai-community-yields-2026-06.csv` | https://data.mendeley.com/public-api/datasets/rwnn99mdz5/versions (и /versions/2, /datasets/…, файл) | 12.11.2026 |
| `datacite-datahabibi.json` | https://api.datacite.org/dois?query=datahabibi | 12.11.2026 |
| `pm-feed.xml` | https://www.propertymonitor.com/insights/category/monthly-market-report/feed | 12.11.2026 |
| `cm-home.html`, `cm-residential.html`, `cm-q3-2026-1*.pdf` (все 0 байт, WAF 202) | https://cavendishmaxwell.com/ … | 12.11.2026 |
| `zawya-cm-q3-sales.html` | https://www.zawya.com/en/press-release/research-studies/dubai-residential-sales-values-top-aed72.6-billion-in-q3-2026-cavendish-maxwell-1518343 | 12.11.2026 |
| `kt-cm-rents-1in5.html` | https://www.khaleejtimes.com/business/dubai-rents-1-in-5-tenants-now-pays-less-than-before-as-rentals-ease-on-new-supply (02.11.2026) | 12.11.2026 |
| `kt-savills-rents12.html` | https://www.khaleejtimes.com/business/rents-in-dubai-fall-over-12-dubai-marina-business-bay-and-jvc-lead (13.10.2026) | 12.11.2026 |
| `kt-kf-q3.html`, `kf-newsroom.html`, `kf-dubai-resi-review.html` | https://www.khaleejtimes.com/business/dubais-10-million-plus-home-sales-reach-86-in-q3-2026 , https://www.knightfrank.ae/newsroom , …/dubai-residential-market-review-2365 | 12.11.2026 |
| `valustrat-september-2026.html`, `valustrat-october-2026.html` | https://valustrat.com/products/dubai-vpi-residential-values-september-2026 , …-october-2026 | 12.11.2026 |
| `thenational-fees-2025.html` | https://www.thenationalnews.com/business/property/2025/01/25/uae-property-mortgages-fees/ | 12.11.2026 |
| `dld-rental-index.html` | https://dubailand.gov.ae/en/eservices/rental-index/rental-index/ | 12.11.2026 |
| `savills-news.html`, `zawya-research.html`, `zawya-search-cm.html` | https://www.savills.ae/insight-and-opinion/savills-news.aspx , zawya.com | 12.11.2026 |
| Savills Q3 2026 (не сохранён, прочитан через WebFetch) | https://www.savills.com/research_articles/255800/395342-0 | 12.11.2026 |
| `txt/` | текстовые выжимки всех HTML и PDF; `txt/*-1510.txt` — копии 15.10 для диффа | 12.11.2026 |
