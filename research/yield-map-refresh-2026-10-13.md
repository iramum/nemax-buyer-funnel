# Dubai Yield Map: обновление цифр на 13.10.2026

> Пересверка всех цифр `05_OPERATIONS:/sales/YIELD_MAP_v3_broker-plain_2026-10-13.md` (и таблиц PAGE 05/06 из `ROI_MAP_v2.md`) против ресёча `roi-map-dubai-2026-09-04.md`.
> Дата проверки: **13.10.2026**. Всё открыто сегодня curl'ом (браузерный UA) или WebFetch; локальные копии лежат в scratchpad сессии `…/scratchpad/yield-refresh/downloads/` и `…/txt/` (🔴 **scratchpad временный: если нужен архив источников, как у `mortgage-timeline-2026-09-30-sources/`, его надо перенести отдельно, я этого не делала, по заданию трогать можно было только этот файл**).
> Ярлыки уровня: **PRIMARY** = открыт сам документ/датасет/страница издателя, цифра стоит там дословно. **PUBLISHER RELEASE** = пресс-релиз самой компании (на Zawya), сам отчёт не открыт. **PRESS** = СМИ пересказывают первоисточник. **NOT FOUND** = искала, не нашла, проверить.

---

## 1. Сводка: у каких источников вышли новые выпуски

| Источник | Что было в ресёче 04.09 | Что есть на 13.10.2026 | Новый выпуск? |
|---|---|---|---|
| **Bayut Dubai Sales Market Report** | H1 2026 | H1 2026, та же страница. Шапка «Updated: 13 Oct, 2026», но **все 13 цифр по нашим районам совпали** с 04.09. В sitemap MyBayut нет ни одного Q3/9M-отчёта за 2024–2026: Bayut с 2024 выпускает только H1 и годовой | **Нет.** Следующий ожидаемый: годовой 2026, по прошлому циклу (годовой 2025 вышел 22.01.2026) это январь 2027 |
| **Property Monitor** (через Engel & Völkers) | April 2026 (E&V `rental-yield-dubai`) | Та же страница E&V **переписана: «Updated: 9 Sept 2026», «As of August 2026… Source: Property Monitor»**. Новые средние и новый список из 15 районов. Апрельской таблицы и сплита new lets / renewals на странице больше нет | **Да: August 2026, опубликовано 09.09.2026** |
| Property Monitor напрямую | архив до Dec 2025 | Архив `propertymonitor.com/insights/category/monthly-market-report` по-прежнему заканчивается December 2025; URL `monthly-market-report-<месяц>-2026` за январь…сентябрь 2026 все 404 | Нет публичного |
| **Engel & Völkers, «Highest ROI»** | August 2026 | Та же статья, «Published: 27 Aug 2026», цифры те же | **Нет** |
| **dataHabibi на Mendeley** (DOI 10.17632/rwnn99mdz5.1) | June 2026, v1 | API Mendeley: версия одна (`[{"version":1,"publish_date":"2026-07-03"}]`), v2 → «Dataset Not Found». CSV скачан заново, все 22 строки совпали. Три других DOI в DataCite (ScienceDB 08.10, B2SHARE 03.10, IEEE 30.09) — перепубликации того же **June 2026** снапшота | **Нет** |
| dataHabibi, живая страница | не использовалась | `datahabibi.ae/dubai/intelligence/price-index`, «built 13 October 2026», данные до 11.10.2026, CSV по 96 районам. **Метод и масштаб другие** (см. §2.3), цифры ниже на 1–4 п.п. | Это **не** новый выпуск датасета, а другой продукт того же автора |
| **Cavendish Maxwell** | H1 2026 (релиз на Zawya) | Q3 2026 вышел, но я нашла **только продажи**, и только в прессе (The National 07.10.2026). Сайт CM закрыт AWS WAF (HTTP 202, `x-amzn-waf-action: challenge`), Gulf Business 403. Цен, аренды, сдачи за Q3 не нашла | **Частично**, PRESS |
| **Savills, Dubai Residential Market in Minutes** | Q2 2026 не использовался | **Q3 2026: пресс-релиз Savills, Zawya, 12.10.2026.** Цены Q3, аренда, предложение | **Да**, PUBLISHER RELEASE |
| **Savills World Cities Prime Residential Index** | H1 2026 | H1 2026 от **19.08.2026** — по-прежнему последний. Более свежая статья в той же ленте 01.10.2026 — про благосостояние (Great Wealth Transfer), не прайм-индекс | **Нет** |
| **ValuStrat VPI** | не использовался | **September 2026, опубликовано 07.10.2026** (сам PDF только по e-mail, открыто описание на странице издателя) | Да, PUBLISHER PAGE |
| Knight Frank / Betterhomes / CBRE / Property Finder | — | Knight Frank: последний Dubai residential review в newsroom — Q4 2025. Betterhomes: в списке market reports последний Q1 2026 (поиск называет Q2 2026). Q3 2026 ни у кого не нашла | NOT FOUND, проверить ближе к ноябрю |

**Главное, что меняется в документе:**
1. Колонка «Contracts» (Property Monitor) переезжает с April на **August 2026**. Почти все районы просели на 0,3–0,9 п.п. **Discovery Gardens и Dubai Investments Park в августовском списке Property Monitor нет.** Значит, наш ключевой пример «9.06% в листингах против 7.41% в контрактах» больше не опирается на живую страницу.
2. Сплит **new lets 6.98% / renewals 6.40%** больше нигде не опубликован. Свежего сплита я не нашла.
3. Средняя по Дубаю от Property Monitor: **6.68% → 6.34%**, квартиры **7.15% → 6.66%**.
4. dataHabibi на живом сайте теперь даёт **6.4%** по городу вместо **8.16%**, а по районам на 2–4 п.п. ниже июньского датасета. Это противоречие внутри одного источника. Июньский датасет на Mendeley не изменился и остаётся единственной версией с n зданий.
5. Фон рынка: у Savills за **Q3 2026** квартиры **−4.8% к Q2** (для одних и тех же объектов −1.7%). Процента по аренде за Q3 нет ни у кого из найденных.

---

## 2. Каждая цифра: старое → новое

### 2.1. Таблица районов, колонка Bayut (listings, H1 2026)

Источник: Bayut, «Bayut's Dubai Sales Market Report for H1 2026», https://www.bayut.com/mybayut/dubai-sales-market-report-h1-2026/ , `datePublished 2026-07-09`, шапка «Updated: 13 Oct, 2026». Уровень: **PRIMARY** (страница открыта 13.10, цифры в сегментных таблицах).

| Район | 04.09 | 13.10 | Где на странице |
|---|---|---|---|
| International City | 8.79% | **8.79%**, без изменений | только в тексте блока «Highest ROIs»: «followed closely by International City at 8.79%» (своей строки в таблице нет) |
| Dubai Sports City | 8.12% | **8.12%**, без изменений | Affordable apartments |
| Dubai South | 7.24% | **7.24%**, без изменений | Affordable apartments |
| Discovery Gardens | 9.06% | **9.06%**, без изменений | Highest rental yields for apartments |
| Dubai Silicon Oasis | 8.23% | **8.23%**, без изменений | Affordable apartments |
| Jumeirah Village Circle | 7.15% | **7.15%**, без изменений | Mid-tier apartments |
| Arjan | 7.10% | **7.10%**, без изменений | Mid-tier apartments |
| Al Furjan | 7.69% | **7.69%**, без изменений | Highest rental yields (mid-tier) |
| Jumeirah Lakes Towers | — | **—** (Bayut не публикует) | — |
| Business Bay | 6.29% | **6.29%**, без изменений | Mid-tier apartments |
| Dubai Marina | 5.88% | **5.88%**, без изменений | Luxury apartments |
| Downtown Dubai | 5.46% | **5.46%**, без изменений | Luxury apartments |
| Dubai Hills Estate | 6.30% | **6.30%**, без изменений | Luxury apartments |
| Palm Jumeirah | 4.48% | **4.48%**, без изменений | Ultra-luxury apartments |

Методическая оговорка на странице прежняя, теперь с уточнением: «based on property prices advertised by real estate agencies… reflect advertised listing prices only and are not representative of actual real estate transaction prices… Reported price metrics are calculated using a trimmed mean methodology».

⚠️ Расхождения внутри отчёта Bayut никуда не делись: Al Barari apartments 6.49% / 6.48%, DAMAC Hills 2 villas 6.03% / 5.97%, и новое, которого не было в ресёче: Dubai Hills Estate villas 4.30% в таблице и 4.31% в тексте. На нашу таблицу квартир это не влияет.

### 2.2. Колонка Property Monitor (contracts): April 2026 → August 2026

Источник: Engel & Völkers, «Dubai Rental Yield in 2026: Where to Invest for High Returns», Francis Gomez, «Updated: 9 Sept 2026», https://www.engelvoelkers.com/ae/en/resources/rental-yield-dubai . Дословно: «As of August, some of the most popular apartment communities with investors offered average rental yields of: … Source: Property Monitor». Уровень: **PRIMARY для публикации E&V**, Property Monitor через E&V (как и в апреле: у PM нет публичного архива 2026).

| Район | April 2026 (04.09) | **August 2026 (13.10)** | Δ |
|---|---|---|---|
| International City | — | **8.93%** | новое значение |
| Dubai Sports City | 8.23% | **7.76%** | −0.47 |
| Dubai South | — | **7.21%** | новое значение |
| Discovery Gardens | 7.41% | **— (нет в августовском списке)** | значение пропало |
| Dubai Silicon Oasis | 7.62% | **6.69%** | −0.93 |
| Jumeirah Village Circle | 7.43% | **6.36%** | −1.07 |
| Arjan | — | **6.95%** | новое значение |
| Al Furjan | — | **7.08%** | новое значение |
| Jumeirah Lakes Towers | 7.17% | **6.58%** | −0.59 |
| Business Bay | 6.77% | **5.92%** | −0.85 |
| Dubai Marina | 6.18% | **5.51%** | −0.67 |
| Downtown Dubai | 5.73% | **5.10%** | −0.63 |
| Dubai Hills Estate | 6.35% | **5.82%** | −0.53 |
| Palm Jumeirah | — | **4.58%** | новое значение |
| Dubai Investments Park (вне таблицы) | 8.53% | **— (нет в списке)** | значение пропало |

Ещё в августовском списке есть Dubai Creek Harbour 5.12% и JBR 5.19%, их в нашей таблице нет.

⚠️ **Методика.** В августовской версии страницы больше нет слов про registered contracts и сплита new / renewals. Подпись прежняя: «Source: Property Monitor». Называть колонку «registered contracts» можно только по методике самого Property Monitor (DLD + Ejari), а на этой странице август так не описан. 🔴 **Предлагаю подпись колонки «Property Monitor, registered data, August 2026», без слова contracts. Решение за тобой.**

### 2.3. Колонка dataHabibi (DLD-derived) и n

**Mendeley, июньский датасет: без изменений.** API `data.mendeley.com/public-api/datasets/rwnn99mdz5/versions` → `[{"version":1,"publish_date":"2026-07-03","available":true}]`. Файл `dubai-community-yields-2026-06.csv` скачан 13.10 и сверен построчно: **все 14 значений и все n те же.** Уровень: **PRIMARY** (датасет скачан и прочитан).

| Район | Yield, June 2026 | n (buildings with yield data) |
|---|---|---|
| International City | 9.98% | 220 |
| Dubai Sports City | 9.54% | 54 |
| Dubai South | 9.35% | 85 |
| Discovery Gardens | 9.04% | 88 |
| Dubai Silicon Oasis | 9.04% | 67 |
| Jumeirah Village Circle | 8.86% | 213 |
| Arjan | 8.66% | 70 |
| Al Furjan | 8.07% | 51 |
| Jumeirah Lakes Towers | 7.87% | 39 |
| Business Bay | 7.75% | 115 |
| Dubai Marina | 7.71% | 106 |
| Downtown Dubai | 7.43% | 116 |
| Dubai Hills Estate | 6.99% | 36 |
| Palm Jumeirah | 5.66% | 87 |

**Живая страница dataHabibi: противоречит июньскому датасету.** https://datahabibi.ae/dubai/intelligence/price-index , «Gross rental yield 6.4%. Weighted mean of published community gross yields, built 13 October 2026», кредит «data through 11 October 2026». CSV `https://datahabibi.ae/api/data/price-index.csv?series=communities` (96 районов, `generated_at 2026-10-13T06:11:34Z`). Уровень: **PRIMARY** (страница и CSV издателя), но это **другая метрика**:
- в CSV нет n зданий, вместо него `transactions_12m` (сделки за 12 мес.);
- в CSV нет разбивки по типу жилья (у Al Barari 8.32%, значит, в выборку входят и виллы);
- в CSV есть явные выбросы: Dubai Internet City 26.06%, Emirates Golf Club 17.05%, Falcon City 14.94%;
- в коде страницы есть манифест выгрузки `bayut_rentals.csv` / `bayut-listings` (118 589 строк на 13.10). **Входят ли листинги Bayut в расчёт доходности, страница не говорит.** Если входят, то колонка перестаёт быть «чистой DLD».
- На той же странице другая оценка: «rent runs near AED 78 per square foot a year against a sale price near AED 1,666, and the ratio between them is the gross yield, about 4.7% before service charges».

| Район | Mendeley June 2026 | **Живой dataHabibi 13.10.2026** | Δ | transactions_12m |
|---|---|---|---|---|
| International City | 9.98% | 7.16% | −2.82 | 3 359 |
| Dubai Sports City | 9.54% | 5.62% | −3.92 | 3 023 |
| Dubai South | 9.35% | 7.46% | −1.89 | 13 186 |
| Discovery Gardens | 9.04% | 6.99% | −2.05 | 1 197 |
| Dubai Silicon Oasis | 9.04% | 5.89% | −3.15 | 2 065 |
| Jumeirah Village Circle | 8.86% | 6.69% | −2.17 | 11 633 |
| Arjan | 8.66% | 7.01% | −1.65 | 3 745 |
| Al Furjan | 8.07% | 6.32% | −1.75 | 2 269 |
| Jumeirah Lakes Towers | 7.87% | 6.13% | −1.74 | 1 321 |
| Business Bay | 7.75% | 4.70% | −3.05 | 6 526 |
| Dubai Marina | 7.71% | 4.89% | −2.82 | 2 298 |
| Downtown Dubai | 7.43% | 4.67% | −2.76 | 2 671 |
| Dubai Hills Estate | 6.99% | 5.44% | −1.55 | 2 814 |
| Palm Jumeirah | 5.66% | 3.56% | −2.10 | 1 250 |
| Dubai Investments Park | — | 4.89% | — | 2 127 |
| Dubai Production City | — | 4.84% | — | 3 196 |

Падение на 2–4 п.п. за три месяца рыночным движением не объясняется: CM дал −2.5% по аренде за квартал. Скорее всего, изменился метод (взвешивание, состав выборки, тип жилья). Сам dataHabibi метод не объясняет. 🔴 **Это главное решение по документу, см. §5, вопрос 1.**

### 2.4. Колонка Engel & Völkers «August read»

Источник: Engel & Völkers, «Highest ROI properties in Dubai 2026», Usman Adrees, «Published: 27 Aug 2026», https://www.engelvoelkers.com/ae/en/resources/highest-roi-in-dubai-real-estate . Уровень: **PRIMARY**. Новой версии нет, цифры те же. Источник данных в статье не назван.

| Район | 04.09 | 13.10 |
|---|---|---|
| International City | 8.89% | 8.89%, без изменений |
| Dubai Sports City | 7.89% | 7.89%, без изменений |
| Discovery Gardens | 7.83% | 7.83%, без изменений |
| Dubai Marina | 5.64% | 5.64%, без изменений |
| Downtown Dubai | 5.21% | 5.21%, без изменений |
| Palm Jumeirah | 4.66% | 4.66%, без изменений |
| Dubai Investments Park | 9.61% | 9.61%, без изменений |
| Dubai Production City | 8.18% | 8.18%, без изменений |
| Средние: all / apartments / TH / villas | ~6.5% / 6.8% / 5.1% / 4.5% | без изменений |

⚠️ **Противоречие внутри E&V.** Обе статьи пишут «as of August 2026», а цифры разные:

| | «Highest ROI», 27.08 | «Rental Yield», 09.09, Source: Property Monitor |
|---|---|---|
| All residential | ~6.5% | 6.34% |
| Apartments | 6.8% | 6.66% |
| Townhouses | 5.1% | 5.06% |
| Villas | 4.5% | 4.45% |
| International City | 8.89% | 8.93% |
| Dubai Sports City | 7.89% | 7.76% |
| Dubai Marina | 5.64% | 5.51% |
| Downtown Dubai | 5.21% | 5.10% |
| Palm Jumeirah | 4.66% | 4.58% |

Похоже, что статья от 27.08 построена на более раннем срезе (вероятно, июльском) Property Monitor, а подписана августом. Это **моё предположение, проверить нечем.** Получается, что две колонки таблицы, «Contracts» и «Aug read», скорее всего, один и тот же источник в двух соседних месяцах. 🔴 **См. §5, вопрос 2.**

### 2.5. Средние по Дубаю

| Цифра в v2/v3 | Было | Стало | Источник / дата / URL | Уровень |
|---|---|---|---|---|
| Dubai average, Property Monitor | 6.68% (April 2026) | **6.34% (August 2026)** | E&V «Rental Yield», upd. 09.09.2026, `…/resources/rental-yield-dubai` | PRIMARY (E&V), PM через E&V |
| Apartments, Property Monitor | 7.15% | **6.66%** | то же | то же |
| Villas, Property Monitor | 4.98% (villas/TH) | **Villas 4.45%, Townhouses 5.06%** | то же | то же |
| Dubai average, DLD-derived | 8.16% (June 2026) | **8.16% без изменений** (Mendeley v1) / **6.4%** на живом сайте 13.10.2026 | Mendeley DOI 10.17632/rwnn99mdz5.1 / datahabibi.ae price-index | PRIMARY оба, **противоречат** |
| New lets | 6.98% (April 2026) | **не обновлено**: в августовской версии E&V сплита нет, другого публичного источника не нашла | — | NOT FOUND (свежего) |
| Renewals | 6.40% (April 2026) | **не обновлено**, то же | — | NOT FOUND (свежего) |
| Cavendish Maxwell apartments / villas | «nearly 7%» / «5%» (H1 2026) | **без изменений**: в найденной Q3-прессе доходностей нет | Zawya, CM release H1 2026 | PUBLISHER RELEASE |

⚠️ Апрельские 6.68 / 7.15 / 4.98 / 6.98 / 6.40 теперь **не видны ни на одной живой странице**: E&V переписал страницу на август, Wayback её не сохранил (CDX пустой). Подтверждение остаётся только в нашем ресёче от 04.09. Если цифры остаются в документе, ссылка на источник ведёт на страницу, где их уже нет.

### 2.6. DIP и Dubai Production City

| Цифра | Было | Стало | Примечание |
|---|---|---|---|
| Dubai Investments Park 9.61% (E&V Aug) | 9.61% | **9.61%**, без изменений (E&V 27.08) | Ещё два значения: **CM H1 2026: 9.7%** («Dubai Investments Park saw the highest yields at 9.7%», Zawya, PUBLISHER RELEASE) и **живой dataHabibi: 4.89%**. В Property Monitor August DIP нет (в апреле был 8.53%) |
| Dubai Production City 8.18% (E&V Aug) | 8.18% | **8.18%**, без изменений | Живой dataHabibi: **4.84%**. В Property Monitor August нет |

Разброс по DIP теперь 4.89–9.7%, почти пять пунктов. Фраза v3 «appear only in the August figures» верна, если оставить июньский датасет. Если перейти на живой dataHabibi, она станет неверной.

### 2.7. Фон рынка: Cavendish Maxwell H1 2026 и что вышло за Q3

**CM H1 2026: перепроверено, всё на месте.** Релиз CM на Zawya, https://www.zawya.com/en/press-release/research-studies/dubai-adds-24800-new-residential-units-in-h1-2026-as-market-shifts-from-launch-led-to-delivery-driven-says-cavendish-maxwell-414719 . Уровень: **PUBLISHER RELEASE** (сам PDF CM не открыт: сайт за WAF).

| Цифра | H1 2026 (подтверждено 13.10) | Свежее за Q3 2026 | Источник Q3 / дата | Уровень Q3 |
|---|---|---|---|---|
| Prices q/q | −2.6% (Q2 vs Q1; в шапке «around 2.5%»), +1.9% y/y, AED 1,639 psf в июне | **CM: не нашла.** **Savills Q3: apartments AED 1,817 psf, −4.8% QoQ (like-for-like −1.7%); villas/TH AED 1,523 psf, −3.3% QoQ (like-for-like flat).** **ValuStrat Sept 2026: VPI 218.6, −0.1% m/m, −4.5% y/y; villas −3.4% y/y; apartments −6.4% y/y** | Savills, релиз на Zawya 12.10.2026 / ValuStrat, страница продукта, опубл. 07.10.2026 | PUBLISHER RELEASE / PUBLISHER PAGE |
| Rents q/q | −2.5% (Q2 vs Q1), +7.8% y/y | **Процента за Q3 не нашла ни у кого.** Savills Q3: «Rental rates across selected communities showed early signs of stabilisation»; 181,900 rental transactions (+16% QoQ), new leases 44% (36% в Q2) | Savills, 12.10.2026 | PUBLISHER RELEASE |
| Homes delivered | 24,800 в H1 | **Q3 не нашла.** ⚠️ Savills Q2 (21.07.2026): **27,300 сдано за один Q2**, то есть больше, чем CM насчитал за всё полугодие | savills.com news 393062 | PRIMARY (страница Savills) |
| H2 2026 scheduled / expected | 47,000 / 14,000–23,500 | без изменений | CM H1 | PUBLISHER RELEASE |
| Pipeline 2027 / 2028 | 162,500 / 128,200 | без изменений у CM. Savills Q3: «more than 525,000 units currently scheduled for delivery between 2027 and 2030» | Savills 12.10.2026 | PUBLISHER RELEASE |
| New launches | 28,000 units / 124 launches (H1) | Savills Q3: «around 5,000» за Q3, около 50,000 за 9M 2026 (−64% y/y) | Savills 12.10.2026 | PUBLISHER RELEASE |
| Sales transactions | 79,300 в H1, −14% y/y | **CM Q3: ~34,000, −38% y/y; 9M: 112,580, −23%.** Savills Q3: ~34,500, −4% QoQ, −38% YoY | The National 07.10.2026 (CM) / Savills 12.10 | PRESS / PUBLISHER RELEASE |
| Sales value | AED 221.4bn (off-plan ~166, ready 55.5) | **CM Q3: AED 72.6bn, −47% y/y; 9M: AED 292bn, −27%.** Savills Q3: AED 70.8bn, −14% QoQ; ready AED 25.1bn (Q2: 21.3) | то же | PRESS / PUBLISHER RELEASE |
| Off-plan share | ~75% сделок | CM Q3: 65% стоимости, 72% сделок | The National 07.10.2026 | PRESS |
| Off-plan / ready y/y | −9% / −26% | CM Q3: не нашла | — | NOT FOUND |
| Mortgage transactions | 22,500, +7.2% y/y | CM Q3: не нашла | — | NOT FOUND |

**The National, 07.10.2026** (https://www.thenationalnews.com/business/property/2026/10/07/dubai-home-sale-transactions-fall-in-third-quarter-due-to-regional-uncertainty/), дословно: «Dubai recorded home sales worth a total of Dh72.6 billion ($19.7 billion) in the three months to the end of September, down 47 per cent… The number of transactions dropped 38 per cent to 34,000». Там же S&P Global Ratings, со ссылкой на «industry reports»: «prices declined by 5 per cent to 15 per cent between the end of 2025 and September 2026». Это PRESS, отчёт S&P не открыт.

⚠️ Ловушка: в выдаче по «Cavendish Maxwell Q3» Khaleej Times показывает статью «Off-plan sales dominate… in Q3 amid record transaction volumes». Она от **14.11.2025 и про Q3 2025**. Для 2026 её не брать.

⚠️ **Противоречия, которые нельзя сглаживать:**
- Аренда за Q2: **CM −2.5% q/q**, а **Savills −8–10%** («rental rates across major residential communities fell by an average of 8–10%», Savills, 21.07.2026). Разные выборки: у CM весь рынок, у Savills «major residential communities».
- Сдача за Q2: у Savills 27,300 за квартал, у CM 24,800 за полугодие.
- Запуски за Q2: в релизе Savills Q3 «approximately 36,400 in the previous quarter», а в пересказе их Q2-отчёта в Khaleej Times 5,335 (PRESS, сам Q2-отчёт не открыт).

### 2.8. Savills World Cities Prime Residential Index

| Цифра | Было | Стало | Источник | Уровень |
|---|---|---|---|---|
| Index-wide capital values H1 2026 | +0.6% | **+0.6%, без изменений** | https://www.savills.com/research_articles/255800/393831-0 , «Spotlight: World Cities Prime Residential Index – H1 2026», **19 August 2026** | PRIMARY |
| Index-wide rents H1 2026 | +1.1% | **+1.1%, без изменений** | то же | PRIMARY |
| Dubai declines in values and rents | «Dubai, Berlin and Bangkok recorded declines in both» | **без изменений** | то же | PRIMARY |
| Dubai H2 2026 forecast | «values forecast to fall by around −10%» | **без изменений**, дословно: «Dubai remains the clear outlier, with values forecast to fall by around -10% as oversupply and geopolitical uncertainty continue to weigh on the market.» | то же | PRIMARY |
| Более новый прогноз Savills по прайму Дубая | — | **Не нашла.** Следующий WCPRI (H2 2026) по циклу выходит около февраля 2027 | — | NOT FOUND |

⚠️ Свежие цифры Savills по прайму **не прогноз, но смотрят в другую сторону.** Q3 2026, 12.10: «prime apartment prices remained 4.0% higher YoY at AED 5,237 per sq ft, while prime villa and townhouse prices increased 3.6% YoY to AED 2,791 per sq ft». Прайм к прошлому году ещё в плюсе, хотя прогноз на H2 −10%. Одно другому не противоречит: H1 2026 уже был минусовым, а годовое сравнение включает рост второй половины 2025. Но брокер, который читал релиз 12.10, может это заметить.

⚠️ Старая ловушка на месте: страница Savills «Rents and Yields» (`savills.us/research_articles/256536/331038-0`) показывает данные за шесть месяцев до июня **2022**. Не цитировать.

### 2.9. Правило «банки не финансируют transfer fee и agency fee с 01.02.2025»

| | Результат |
|---|---|
| Статус на 13.10.2026 | **Отмены или пересмотра не нашла.** Поиск по 2026 году находит только повторы правила |
| Источник | The National, 25.01.2025, https://www.thenationalnews.com/business/property/2025/01/25/uae-property-mortgages-fees/ , открыт: «The Central Bank of the UAE's recent instruction for banks to stop financing the Dubai Land Department registration fees and real estate broker fees from February 1…» и «the Central Bank has told banks to stick to the original LTV of 80 per cent of the collateral». Уровень: **PRESS** |
| Первоисточник CBUAE | По канону проекта (`individual-dubai-2026-06-28.md`, строка 38): публичного циркуляра нет, это непубличное указание. Цитировать The National, номер циркуляра не придумывать. **Сегодня заново не проверяла** |
| ⚠️ Противоречие | Bayut «Home Loans in Dubai» (шапка «Updated: 13 Oct, 2026», https://www.bayut.com/mybayut/home-loans-dubai/) до сих пор пишет: «Some banks in Dubai allow mortgage takers to add three-quarters of the total purchase fee to their home loan.» Это старый текст до 2025 года под свежей датой. Брокер может на него наткнуться |
| Формулировка v3 | «UAE banks no longer finance the transfer fee and the agency fee» держится, но это пересказ указания ЦБ через прессу, а не цитата регуляции. Вариант точнее: «Since 1 February 2025, UAE banks have been told not to include…». Оставляю на твоё решение |

### 2.10. Dubai REST: service charge по проекту

| | Результат |
|---|---|
| Страница DLD | https://dubailand.gov.ae/en/eservices/service-charge-index-overview/ , «Site was last updated on 07 October 2026». Дословно: «This service allows the customer to inquire about the approved service fees for Joint ownership properties from the Real Estate Regulatory Agency (RERA in Dubai Emirate.» Шаги: «A customer selects the name of the project from the menu, the uses, and the year». Service time: «Immediate». Channels: «1) Land Department website (Mollak system) 2) The Land Department website 3) Dubai REST App». Residency status: «All». Уровень: **PRIMARY** |
| Листовка | https://dubailand.gov.ae/media/vkcojy4z/service_charge_index_en.pdf отдаётся, 4 страницы, создана 05.07.2022, текст тот же: Dubai REST → Services → Service Charge Index → Project / usage / year |
| Вывод | **Механика прежняя:** ставка по проекту, утверждена RERA, смотреть в Dubai REST или на сайте DLD (Mollak). Каналов теперь три, не только приложение |
| ⚠️ «It is free.» (v3, стр. 06) | **Не подтверждено.** На странице услуги раздела про плату нет, слова «free» тоже. В ресёче 04.09 это тоже не проверялось. Либо убрать, либо проверить в приложении |

---

## 3. Новая таблица на 14 районов (для вставки) и разброс

### 3.1. Вариант A (рекомендую): то же, что в v2/v3, но Property Monitor на August 2026

Колонки: **Listings** = Bayut Dubai Sales Market Report H1 2026 / **Registered** = Property Monitor, August 2026, as published by Engel & Völkers (upd. 9 Sep 2026) / **Aug read** = Engel & Völkers, 27 Aug 2026 / **DLD-derived** = dataHabibi, June 2026, Mendeley Data, CC BY 4.0 / **n** = buildings behind the DLD figure.

| Community | Listings | Registered | Aug read | DLD-derived | n |
|---|---|---|---|---|---|
| International City | 8.79% | 8.93% | 8.89% | 9.98% | 220 |
| Dubai Sports City | 8.12% | 7.76% | 7.89% | 9.54% | 54 |
| Dubai South | 7.24% | 7.21% | | 9.35% | 85 |
| Discovery Gardens | 9.06% | | 7.83% | 9.04% | 88 |
| Dubai Silicon Oasis | 8.23% | 6.69% | | 9.04% | 67 |
| Jumeirah Village Circle | 7.15% | 6.36% | | 8.86% | 213 |
| Arjan | 7.10% | 6.95% | | 8.66% | 70 |
| Al Furjan | 7.69% | 7.08% | | 8.07% | 51 |
| Jumeirah Lakes Towers | | 6.58% | | 7.87% | 39 |
| Business Bay | 6.29% | 5.92% | | 7.75% | 115 |
| Dubai Marina | 5.88% | 5.51% | 5.64% | 7.71% | 106 |
| Downtown Dubai | 5.46% | 5.10% | 5.21% | 7.43% | 116 |
| Dubai Hills Estate | 6.30% | 5.82% | | 6.99% | 36 |
| Palm Jumeirah | 4.48% | 4.58% | 4.66% | 5.66% | 87 |

Заполненных ячеек теперь 46 (было 42): у Property Monitor появились International City, Dubai South, Arjan, Al Furjan и Palm Jumeirah, пропал Discovery Gardens.

**Разброс по району** (минимум и максимум среди опубликованных; было = таблица v2 со старой колонкой April):

| Community | Lowest | Highest | Spread | Было (v2) |
|---|---|---|---|---|
| Jumeirah Village Circle | 6.36% | 8.86% | **2.50 pp** | 7.15–8.86, 1.71 |
| Dubai Silicon Oasis | 6.69% | 9.04% | **2.35 pp** | 7.62–9.04, 1.42 |
| Downtown Dubai | 5.10% | 7.43% | **2.33 pp** | 5.21–7.43, 2.22 |
| Dubai Marina | 5.51% | 7.71% | **2.20 pp** | 5.64–7.71, 2.07 |
| Dubai South | 7.21% | 9.35% | **2.14 pp** | 7.24–9.35, 2.11 |
| Business Bay | 5.92% | 7.75% | **1.83 pp** | 6.29–7.75, 1.46 |
| Dubai Sports City | 7.76% | 9.54% | **1.78 pp** | 7.89–9.54, 1.65 |
| Arjan | 6.95% | 8.66% | **1.71 pp** | 7.10–8.66, 1.56 |
| Jumeirah Lakes Towers | 6.58% | 7.87% | **1.29 pp** | 7.17–7.87, 0.70 |
| Discovery Gardens | 7.83% | 9.06% | **1.23 pp** | 7.41–9.06, 1.65 |
| International City | 8.79% | 9.98% | **1.19 pp** | 8.79–9.98, 1.19 |
| Palm Jumeirah | 4.48% | 5.66% | **1.18 pp** | 4.48–5.66, 1.18 |
| Dubai Hills Estate | 5.82% | 6.99% | **1.17 pp** | 6.30–6.99, 0.69 |
| Al Furjan | 7.08% | 8.07% | **0.99 pp** | 7.69–8.07, 0.38 |

Что это значит для текста: самый широкий разрыв теперь **JVC, 2.50 п.п.** (раньше Downtown, 2.22). Тезис v2 «affordable disagree by around a point and a half, prime by more than two» больше не держится: у JVC и DSO разрыв больше, чем у Downtown. В v3 этой страницы нет, но если её вернут, текст надо переписать. Для 12 районов из 14 самая низкая цифра теперь августовская Property Monitor, самая высокая почти всегда июньская DLD-derived. Часть разрыва может быть временем (июнь против августа), а не методом. Это стоит сказать в тексте.

### 3.2. Вариант B (если берём живой dataHabibi вместо июньского)

Колонку n убрать: живой CSV даёт сделки, а не здания. Дата: «dataHabibi analysis of DLD records, data through 11 October 2026».

| Community | Listings | Registered | Aug read | dataHabibi live | Lowest | Highest | Spread |
|---|---|---|---|---|---|---|---|
| International City | 8.79% | 8.93% | 8.89% | 7.16% | 7.16% | 8.93% | 1.77 pp |
| Dubai Sports City | 8.12% | 7.76% | 7.89% | 5.62% | 5.62% | 8.12% | 2.50 pp |
| Dubai South | 7.24% | 7.21% | | 7.46% | 7.21% | 7.46% | 0.25 pp |
| Discovery Gardens | 9.06% | | 7.83% | 6.99% | 6.99% | 9.06% | 2.07 pp |
| Dubai Silicon Oasis | 8.23% | 6.69% | | 5.89% | 5.89% | 8.23% | 2.34 pp |
| Jumeirah Village Circle | 7.15% | 6.36% | | 6.69% | 6.36% | 7.15% | 0.79 pp |
| Arjan | 7.10% | 6.95% | | 7.01% | 6.95% | 7.10% | 0.15 pp |
| Al Furjan | 7.69% | 7.08% | | 6.32% | 6.32% | 7.69% | 1.37 pp |
| Jumeirah Lakes Towers | | 6.58% | | 6.13% | 6.13% | 6.58% | 0.45 pp |
| Business Bay | 6.29% | 5.92% | | 4.70% | 4.70% | 6.29% | 1.59 pp |
| Dubai Marina | 5.88% | 5.51% | 5.64% | 4.89% | 4.89% | 5.88% | 0.99 pp |
| Downtown Dubai | 5.46% | 5.10% | 5.21% | 4.67% | 4.67% | 5.46% | 0.79 pp |
| Dubai Hills Estate | 6.30% | 5.82% | | 5.44% | 5.44% | 6.30% | 0.86 pp |
| Palm Jumeirah | 4.48% | 4.58% | 4.66% | 3.56% | 3.56% | 4.66% | 1.10 pp |

В этом варианте DLD-колонка из самой высокой становится самой низкой, и меняется весь рассказ (стр. 05/08 v3: «200 buildings… fewer than 40» держится только на июньском n). Поэтому рекомендую A, а живой dataHabibi упомянуть в сноске как отдельный, более свежий расчёт с другим методом.

---

## 4. Предложения в YIELD_MAP_v3, которые надо поменять

Формулировки на английском в стиле плейбука: короткие фразы, may/could, без длинных тире и middot. 🔴 **Всё ниже собрано под вариант A.**

**1. Стр. 02 INTRO, абзац 2.** Сейчас: «You check a property portal and find a yield of 9%. A market report shows 7.4% for the same area.»
7.4% (Discovery Gardens, Property Monitor April) больше не опубликован. Предлагаю перейти на Dubai Silicon Oasis, где обе цифры свежие:
> You check a property portal and find a yield of 8.2%. A market report shows 6.7% for the same area. A third source gives a different number again.

Запасной вариант, если важно оставить «9%»: Discovery Gardens 9.06% (Bayut) против 7.83% (E&V Aug):
> You check a property portal and find a yield of 9%. Another market source shows 7.8% for the same area.

**2. Стр. 03 THE MAP.** Таблицу заменить на §3.1. Подпись второй колонки: «Registered, Aug 2026» вместо «Contracts, Apr 2026». Note:
> Note: n is the number of buildings behind the DLD figure. Where n is small, the average can move easily. Dubai Investments Park (9.61%) and Dubai Production City (8.18%) appear in only one August source, so they are not included.

Строку «Таблица — без изменений из v2» в v3 тоже надо поправить, это служебная пометка.

**3. Стр. 04 / 01, абзац 2.** Сейчас: «In Discovery Gardens, listings showed 9.06% in the first half of 2026. Registered contracts for the same community showed 7.41%.»
> Registered data often shows a lower number. In Dubai Silicon Oasis, listings showed 8.23% in the first half of 2026. Registered data for August 2026 showed 6.69% for the same community.

Sources:
> Sources: Bayut Dubai Sales Market Report H1 2026 (advertised listings) / Property Monitor, August 2026, as published by Engel & Völkers (registered data).

**4. Стр. 05 / 02, абзац 2.** Сейчас: «In Downtown Dubai, one source published 5.21% and another 7.43% for the same year. On an AED 1.5 million apartment, a gap of 2 points is AED 30,000 of rent a year.»
Вариант с самым широким разрывом:
> In Jumeirah Village Circle, one source published 6.36% and another 8.86% in 2026. On an AED 1.5 million apartment, a gap of 2.5 points is AED 37,500 of rent a year.

> Sources: Property Monitor, August 2026, as published by Engel & Völkers / dataHabibi, derived from DLD records, June 2026, CC BY 4.0. The AED example is illustrative.

Если оставить Downtown:
> In Downtown Dubai, one source published 5.10% and another 7.43% in 2026. On an AED 1.5 million apartment, a gap of more than 2 points is about AED 35,000 of rent a year.

(2.33 × 15,000 = AED 34,950.) Слова «for the same year» заменила на «in 2026»: источники июньский и августовский.

**5. Стр. 06 / 03, WHAT TO CHECK.** «It is free.» не подтверждено (§2.10). Предлагаю:
> Look up the service charge for the specific building in the Dubai REST app or on the Dubai Land Department website. It shows the rate approved by RERA, the Dubai property regulator, for each project.

Если в приложении окажется, что услуга бесплатна, «It is free.» можно вернуть.

**6. Стр. 07 / 04, абзац 2.** «In April 2026, registered new contracts showed an average yield of 6.98%. Renewals showed 6.40%.» Свежего сплита нет, а апрельская страница уже переписана. Два варианта.
Оставить с датой (цифры остаются апрельскими, источник больше не виден онлайн):
> In April 2026, registered new contracts showed an average yield of 6.98%. Renewals showed 6.40%. A unit with a sitting tenant and an empty unit can give different results.

Или без цифр:
> Yields based on renewals are often lower than yields based on new tenancies. A unit with a sitting tenant and an empty unit can give different results.

🔴 **Выбор за тобой.** Если цифры остаются, source: «Property Monitor, April 2026, as published by Engel & Völkers (no longer online)», или без пометки в скобках, по решению.

**7. Стр. 09 / 06, абзац 1.** CM за Q2 остаётся последней цифрой по аренде. Добавляю Savills Q3:
> Yield is rent divided by price. In the second quarter of 2026, Dubai prices fell by 2.5% and rents also fell by 2.5%, compared with the first quarter. In the third quarter, average apartment prices fell by a further 4.8%. For the same homes, the fall was 1.7%.

Абзац 2 («About 162,500 new homes… Savills also expects… around 10%…») остаётся как есть, обе цифры актуальны. По желанию можно добавить:
> More than 525,000 homes are scheduled for completion between 2027 and 2030.

Sources:
> Sources: Cavendish Maxwell, Dubai residential market H1 2026 / Savills, Dubai Residential Market in Minutes Q3 2026 / Savills World Cities Prime Residential Index H1 2026.

**8. Стр. 10 / 07.** Правило 01.02.2025 оставить. По желанию сформулировать точнее:
> Since 1 February 2025, UAE banks have been told not to include the transfer fee and the agency fee in the mortgage. These costs must be paid on the day of transfer.

**9. Стр. 11, финальный дисклеймер.** «Yields in this guide are third-party market figures published between April and August 2026» верно для варианта A с апрельским сплитом. Если сплит убрать, самая ранняя дата станет «published between July and September 2026» (Bayut 09.07, dataHabibi 03.07, E&V 27.08 и 09.09). Сноска к кнопке без изменений.

**10. Шапка v3 (служебная).** «🔴 13.10 заново не перепроверялись» после правок заменить ссылкой на этот файл.

---

## 5. Открытые вопросы

1. 🔴 **Колонка DLD-derived: июньский Mendeley или живой dataHabibi?** Mendeley v1 по-прежнему единственная версия: с n, лицензией CC BY 4.0, датой. На живом сайте того же автора на 13.10 цифры на 2–4 п.п. ниже, n нет, метод не описан, и есть признаки, что в расчёте участвуют листинги Bayut. Рекомендую A: июнь в таблице, живую цифру 6.4% в сноске как противоречие. Можно написать автору датасета и спросить, что поменялось в методе. Я не писала.
2. 🔴 **Две «августовские» колонки E&V, скорее всего, один источник.** Статья 27.08 без указания источника и страница 09.09 с подписью «Property Monitor» расходятся на 0.04–0.16 п.п. по одним и тем же районам. Варианты: оставить обе с честными датами публикации (27 Aug / 9 Sep), убрать колонку «Aug read» (тогда у Discovery Gardens остаётся только Bayut и DLD) или переименовать её в «Engel & Völkers, published 27 Aug 2026».
3. 🔴 **Discovery Gardens выпал из Property Monitor.** Главный пример ресёча 04.09 («9.06% vs 7.41%, the number in the listing is not the number in the contract») больше не подкреплён живым источником. Я предложила DSO (8.23% vs 6.69%), разрыв там 1.54 п.п.
4. **Подпись «contracts».** Августовская страница E&V не пишет, что данные по зарегистрированным контрактам. Предлагаю «registered data».
5. **«Apartment yields» в DLD-колонке.** README Mendeley называет датасет «Residential Community Yields», без деления на квартиры и виллы. Подпись страницы 03 «Apartment yields by community» для этой колонки строго не подтверждена. Так было уже в v2, просто раньше это не отмечали.
6. **Cavendish Maxwell Q3 2026.** Сайт CM за WAF, полный отчёт не открыт. Q3-цифры CM взяты из The National (PRESS). Цен, аренды и сдачи за Q3 от CM не нашла. Возможно, они в PDF. Можно открыть cavendishmaxwell.com в обычном браузере и скачать отчёт руками.
7. **Аренда за Q3 2026 в процентах** не найдена ни у одного источника (CM, Savills, ValuStrat, Knight Frank, Betterhomes, Property Finder). Отдельно: Arabian Business «Dubai asking rents fall up to 22%…» (`arabianbusiness.com/real-estate/dubai-rents-q3-2026`) отдаёт 403, провайдер данных в выдаче не назван. Не использовать, пока не откроется.
8. **ValuStrat September 2026**: цифры с описания на странице издателя, сам PDF только по e-mail. Если ValuStrat пойдёт в текст, PDF надо скачать.
9. **Правило 01.02.2025**: отмены не нашла, но и в первоисточнике CBUAE сегодня заново не проверяла (по канону публичного циркуляра нет). Страница Bayut от 13.10.2026 противоречит правилу (старый текст).
10. **«It is free»** про Dubai REST не подтверждено ничем.
11. **Архив источников.** Апрельская страница E&V уже исчезла. Чтобы с августовской не случилось того же, стоит сохранить копии в `04_RESEARCH:/market_reports/` рядом с этим файлом. Сырые HTML/CSV сейчас лежат только в scratchpad этой сессии. Я их не переносила.
12. **Следующие выпуски, которых ждать:** Property Monitor / E&V за September (по прошлому циклу около середины октября); CM Q3 полным отчётом; Bayut 2026 annual (январь 2027); Savills WCPRI H2 2026 (около февраля 2027); Knight Frank Q3 2026 (по прошлому году около ноября).
