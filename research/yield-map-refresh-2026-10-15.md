# Dubai Yield Map: перепроверка выпусков на 15.10.2026

> Продолжение `04_RESEARCH:/market_reports/yield-map-refresh-2026-10-13.md`. Весь ресёч заново не делался. Задача одна: вышло ли у какого-то источника что-то новое между 13.10 и 15.10.2026.
> Проверено **15.10.2026**: curl с браузерным UA, где нужно, WebFetch и WebSearch. Копии лежат в `04_RESEARCH:/market_reports/yield-map-refresh-2026-10-15-sources/`. Для сверки «было/стало» брала файлы 13.10 из `yield-map-refresh-2026-10-13-sources/downloads/`.
> Уровни: **PRIMARY** = открыт сам документ или страница издателя. **PUBLISHER RELEASE** = пресс-релиз компании. **PRESS** = пересказ в СМИ. **NOT FOUND** = искала, не нашла, проверить.
> Текст карты сверяла по `05_OPERATIONS:/sales/buyer-funnel/YIELD_MAP_v3_buyer_2026-10-13.md`, прочитан целиком.

---

## Итог

**С 13.10 ни у одного источника, на котором стоят цифры карты, нового выпуска нет. Менять в тексте карты ничего не нужно.** Обе страницы E&V, Bayut H1 2026 и датасет Mendeley v1 совпадают с 13.10 до цифры, а у Mendeley совпадает и хэш файла. Сентябрьского Property Monitor не нашла ни у E&V, ни у самого PM. Полного отчёта CM за Q3, Savills WCPRI H2, Knight Frank Q3 и Bayut Q3/9M тоже нет.

Сдвинулся только живой CSV dataHabibi: он пересобирается каждый день. В карту он не входит, там вариант A с июньским Mendeley. Ещё нашлись три мелочи для справки, тексту карты они не мешают: §3.

---

## 1. Источник / 13.10 / 15.10 / изменилось ли

| Источник | Состояние на 13.10 | Состояние на 15.10 (чем проверено) | Изменилось? | Уровень |
|---|---|---|---|---|
| **E&V «Dubai Rental Yield in 2026»** (Property Monitor) `engelvoelkers.com/ae/en/resources/rental-yield-dubai` | «Updated: 9 Sept 2026», «As of August…», 15 районов, средняя 6.34% | Шапка та же: «Updated: 9 Sept 2026», JSON-LD `dateModified 2026-09-09`, в sitemap E&V `lastmod 2026-09-09`. Текст «As of August 2026, the average rental yield… was 6.34%». Все 15 районов и средние совпали (§2.1) | **Нет** | PRIMARY |
| **E&V «Highest ROI properties in Dubai 2026»** | «Published: 27 Aug 2026» | Та же шапка, `dateModified 2026-08-27`, sitemap `lastmod 2026-08-27`. 9.61 / 8.89 / 8.18 / 7.89 / 7.83, средние 6.5 / 6.8 / 5.1 / 4.5 на месте | **Нет** | PRIMARY |
| E&V, отчёты в разделе `/ae/en/research/` | — | По sitemap E&V (`/ae/sitemap.xml`) последний жилой отчёт `residential-market-report-h1-2026` (lastmod 05.08.2026). Q3 2026 нет. С 13.10 в sitemap обновлены только `the-yards-plaza-by-beyond`, `company/awards` (14.10) и `sustainable-workspaces` (13.10), к доходности они отношения не имеют | Нет | PRIMARY (sitemap) |
| **Bayut Dubai Sales Market Report H1 2026** | H1 2026, «Updated: 13 Oct, 2026», 13 цифр совпали | Шапка теперь **«Updated: 15 Oct, 2026»** (`dateModified 2026-10-15T08:17:49`), но title тот же: «…Sales Market Report H1 2026», `datePublished 2026-07-09`. Все 13 цифр те же (8.79 / 8.12 / 7.24 / 9.06 / 8.23 / 7.15 / 7.10 / 7.69 / 6.29 / 5.88 / 5.46 / 6.30 / 4.48) | **Нет** (сменилась только дата в шапке) | PRIMARY |
| Bayut, есть ли Q3/9M 2026 | В sitemap нет | Прошла все 5 файлов `post-sitemap1…5.xml` (4 981 URL). Отчётов Dubai за 2026: только `dubai-sales-market-report-h1-2026` и `dubai-rental-market-report-h1-2026`. Q3/9M 2026 нет. 14.10 Bayut массово переотметил сотни старых постов (вплоть до отчёта H1 2021 и «Bayut Premier Cup 2018»), так что «Updated» на страницах Bayut о свежести данных ничего не говорит | Нет | PRIMARY (sitemap) |
| **Mendeley, dataHabibi, DOI 10.17632/rwnn99mdz5** | v1 от 03.07.2026, единственная | API `/versions` → `[{"version":1,"publish_date":"2026-07-03","available":true}]`. `/versions/2` → 404 «Cannot GET». `/datasets/rwnn99mdz5` → version 1. Файл `dubai-community-yields-2026-06.csv` скачан заново, **sha256 `a81917dd…7aebe` совпадает с файлом 13.10** | **Нет** | PRIMARY |
| DataCite, новые DOI того же датасета | 6 DOI (Mendeley ×2, IEEE 30.09, B2SHARE ×2 03.10, ScienceDB 08.10) | Запрос `datahabibi`: те же 6, ничего после 08.10. Запрос `"rental yields" AND Dubai`: 11 записей, новых после 08.10 нет | Нет | PRIMARY (API) |
| **dataHabibi, живая страница** `datahabibi.ae/dubai/intelligence/price-index` | «built 13 October 2026», 6.4%, «data through 11 October 2026» | HTML страницы **побайтно совпадает** с копией 13.10 (`cmp`): тот же «built 13 October 2026», 6.4% и кредит «data through 11 October 2026» | Нет | PRIMARY |
| **dataHabibi, живой CSV** `api/data/price-index.csv?series=communities` | `generated_at 2026-10-13T06:11:34Z` | `generated_at 2026-10-14T22:00:52Z`, 96 районов, состав тот же. Цифры по 16 районам сдвинулись на 0–0.66 п.п. (§2.2) | **Да, но это ежедневная пересборка**, а не выпуск. В карту не входит | PRIMARY |
| dataHabibi, описание метода | «Сам dataHabibi метод не объясняет» | Отдельной страницы метода нет: `/methodology`, `/about/methodology`, `/dubai/methodology`, `/dubai/intelligence/methodology` отдают 404, в sitemap такого URL нет. `/about` про доходность ничего не пишет. Описание метода нашлось в блоге `datahabibi.ae/blog/dubai-rental-yields`, но статья старая, **от 11.07.2026**, а не новая (§3.1) | Новой заметки нет | PRIMARY |
| **Property Monitor напрямую** | архив до Dec 2025 | Лента `…/category/monthly-market-report/feed`: последний выпуск «Monthly Market Report December 2025», 16.01.2026. `insights-sitemap.xml`: последний lastmod 19.01.2026. URL `…/monthly-market-report/monthly-market-report-<месяц>-2026` за январь…сентябрь все 404 (13.10 проверялся другой шаблон URL, сегодня проверила оба) | **Нет** | PRIMARY |
| **Property Monitor / E&V, September 2026** | ожидался «около середины октября» | На E&V нет (см. выше). Поиск сентябрьского выпуска не нашёл, в выдаче только E&V от 09.09 и вторичные сайты | **NOT FOUND**, проверить | — |
| **Cavendish Maxwell Q3 2026, полный отчёт** | только продажи, PRESS (The National 07.10) | Сайт CM по-прежнему за AWS WAF (HTTP 202, `x-amzn-waf-action: challenge`), WebFetch 403. Угаданный URL `…/dubai-residential-market-performance-q3-2026` тоже 202. В Wayback (CDX с 09.2026) есть только страница H1 2026 (06.10.2026). Gulf Business «…Dhs72.6bn… in Q3» отдаёт 403 и curl, и WebFetch. Поиск находит только те же продажи Q3: AED 72.6bn, ~34 000 сделок, 9M AED 292bn / 112 580. Цен, аренды и сдачи за Q3 от CM нет | **Нет** | NOT FOUND (полный отчёт) / PRESS (продажи, как 13.10) |
| **Savills, Dubai residential** | Q3 2026, релиз 12.10 | На `savills.ae/insight-and-opinion/savills-news.aspx` последний жилой Dubai по-прежнему Q2 (393062). Новый релиз Savills на Zawya **14.10.2026**: «Dubai and Abu Dhabi rank among the world's top 10 hubs for next-generation wealth». Цен, аренды, доходности и прогноза там нет (§3.2) | **Нового по рынку нет** | PUBLISHER RELEASE |
| **Savills WCPRI** | H1 2026 от 19.08, следующий около 02.2027 | Нового выпуска не нашла. Отчёт 14.10 «Spotlight on Wealth Trends» к прайм-индексу не относится | Нет | NOT FOUND (H2) |
| **Knight Frank, Dubai Residential Market Review** | «последний в newsroom Q4 2025» | Страница отчёта `knightfrank.ae/research/reports/dubai-residential-market-review-2365`: последний выпуск **Q1 2026, 12 May 2026**. Список «All Editions» за 2026: Q1 2026. Q2 и Q3 2026 нет. Поправка к 13.10: Q1 2026 существует, но вышел в мае, после 13.10 ничего нового | **Нет** | PRIMARY |
| **Правило 01.02.2025** (банки не включают transfer fee и agency fee) | отмены не нашла | Два поиска (новые правила ЦБ на октябрь 2026; «banks allowed again… reversal») находят только январскую статью 2025 года и её повторы. Источники 2026 года по-прежнему пишут, что эти расходы платят сверху. Отмены или пересмотра не нашла. Сайт CBUAE сам не открывала, по канону публичного циркуляра нет | **Нет** | PRESS |
| ValuStrat VPI | September 2026 (07.10) | **Сегодня не перепроверяла**: в задании этого пункта нет, а октябрьский VPI по циклу выходит в начале ноября | — | — |

---

## 2. Цифры: старое → новое

### 2.1. Цифры, на которых стоит карта, не изменились

| Колонка карты (вариант A, §3.1 файла 13.10) | 13.10 | 15.10 |
|---|---|---|
| Listings, Bayut H1 2026 | 13 значений | **все 13 те же** |
| Registered, Property Monitor Aug 2026 через E&V | 14 значений + средние 6.34 / 6.66 / 5.06 / 4.45 | **все те же**: Business Bay 5.92, Downtown 5.10, Dubai Creek Harbour 5.12, Dubai Marina 5.51, JBR 5.19, JLT 6.58, JVC 6.36, Dubai Hills 5.82, Palm 4.58, Dubai South 7.21, Sports City 7.76, International City 8.93, Al Furjan 7.08, Arjan 6.95, DSO 6.69. Discovery Gardens по-прежнему нет |
| Aug read, E&V 27.08 | 8 значений + средние | **все те же** |
| DLD-derived + n, Mendeley June 2026 | 14 значений + n | **файл побайтно тот же** (sha256) |
| Фон: CM H1, Savills Q3 (12.10), WCPRI H1 | см. 13.10 §2.7–2.8 | новых цифр нет |

**Каких предложений в YIELD_MAP_v3_buyer коснулось: ни одного.** Проверила все, где стоят цифры: стр. 02 (8.2% / 6.7%), 04/01 (8.23% / 6.69%), 05/02 (JVC 6.36% / 8.86%, AED 37,500), 09/06 (−2.5% / −2.5% / −4.8% / −1.7%, 162,500, Savills −10%), 10/07 (правило 01.02.2025), дисклеймер («published between July and October 2026»). Все опираются на источники без изменений.

### 2.2. Живой dataHabibi CSV: 13.10 → 15.10 (в карту не входит)

Справочно, на случай если выберут вариант B. Вывод тот же, что 13.10: это живая метрика, она двигается каждый день, поэтому если брать её в печатный PDF, нужна точная дата среза.

| Район | gross 13.10 (gen 13.10 06:11Z) | gross 15.10 (gen 14.10 22:00Z) | Δ п.п. | transactions_12m 13.10 → 15.10 |
|---|---|---|---|---|
| International City | 7.16 | 7.14 | −0.02 | 3 359 → 3 381 |
| Dubai Sports City | 5.62 | 5.62 | 0 | 3 023 → 3 020 |
| Dubai South | 7.46 | 7.46 | 0 | 13 186 → 13 180 |
| Discovery Gardens | 6.99 | 7.00 | +0.01 | 1 197 → 1 189 |
| Dubai Silicon Oasis | 5.89 | 5.89 | 0 | 2 065 → 2 046 |
| Jumeirah Village Circle | 6.69 | 6.71 | +0.02 | 11 633 → 11 605 |
| Arjan | 7.01 | 7.02 | +0.01 | 3 745 → 3 750 |
| Al Furjan | 6.32 | **6.10** | −0.22 | 2 269 → 2 359 |
| Jumeirah Lakes Towers | 6.13 | **5.47** | **−0.66** | 1 321 → 1 624 |
| Business Bay | 4.70 | 4.73 | +0.03 | 6 526 → 6 421 |
| Dubai Marina | 4.89 | 5.00 | +0.11 | 2 298 → 2 278 |
| Downtown Dubai | 4.67 | 4.55 | −0.12 | 2 671 → 2 728 |
| Dubai Hills Estate | 5.44 | 5.41 | −0.03 | 2 814 → 2 798 |
| Palm Jumeirah | 3.56 | 3.56 | 0 | 1 250 → 1 247 |
| Dubai Investments Park | 4.89 | 5.00 | +0.11 | 2 127 → 2 048 |
| Dubai Production City | 4.84 | 4.82 | −0.02 | 3 196 → 3 173 |

⚠️ У JLT за полтора дня «сделок за 12 месяцев» стало на 303 больше (+23%), а доходность упала на 0.66 п.п. Так ведёт себя пересчёт или перевыгрузка, а не рынок. Ещё одно подтверждение, что для печатной карты колонка ненадёжна. Столбец `net_yield_pct` в CSV был и 13.10: заголовок в копии того дня тот же. Файл 13.10 его просто не упомянул.

---

## 3. Что нашлось попутно (тексту карты не мешает)

### 3.1. dataHabibi: как считается живая доходность (статья от 11.07.2026, не новая)

`datahabibi.ae/blog/dubai-rental-yields`, JSON-LD `datePublished/dateModified 2026-07-11`. Уровень **PRIMARY**. Дословно:
- «…registered rental contracts and median sold prices over the last 12 months, dataHabibi's analysis of Dubai Land Department records puts indicative gross yield anywhere from the high 4% range to just above 7%…»
- «…calculated using sale prices that include off-plan transactions alongside ready resales.»
- «Every yield figure in this article comes from residential apartment rent contracts and sale transactions.»

Это частично отвечает на вопрос 1 из §5 файла 13.10 (почему живые цифры на 2–4 п.п. ниже июньского датасета). Живая метрика делит медианную аренду по контрактам на медианную цену сделки за 12 месяцев, **и в цену входят off-plan**. Off-plan дороже готового жилья, поэтому доходность получается ниже. Метод июньского датасета на Mendeley построен по зданиям (n buildings), это другая конструкция. 🔴 **Что разница объясняется именно off-plan в цене, это мой вывод. Сам dataHabibi так разницу не объясняет.** Вопрос про листинги Bayut в расчёте этим текстом не закрыт: в статье сказано «rent contracts», а манифест `bayut_rentals.csv` в коде страницы остаётся необъяснённым.

### 3.2. Savills, 14.10.2026: Next Generation Wealth Hubs Index

Zawya, `…/dubai-and-abu-dhabi-rank-among-the-worlds-top-10-hubs-for-next-generation-wealth-new-savills-analysis-1650791`, `datePublished 2026-10-14`. Уровень **PUBLISHER RELEASE**. Дубай и Абу-Даби в глобальном top 10 индекса. Цифр по ценам, аренде и доходности нет. Для карты не нужен.

### 3.3. Asking rents Q3 2026, Property Finder (через прессу, 13.10.2026)

В §5 п. 7 файла 13.10 говорилось: Arabian Business «Dubai asking rents fall up to 22%…» отдаёт 403, провайдер данных не назван. Сегодня Arabian Business по-прежнему 403 (curl и WebFetch). Пересказ нашёлся в The Week от **13.10.2026**: `theweek.in/news/middle-east/2026/10/13/rents-plunge-in-dubai-…`, открыт через WebFetch. Уровень **PRESS** (пересказ пересказа). Провайдер: **Property Finder**. Сравнение: медиана **запрашиваемой** аренды, Q3 2025 против Q3 2026. Квартиры: Downtown −22%, Dubai Marina −16.13%, Meydan −13.33%, Business Bay −12.5%, JVC −10%, Dubai Hills без изменений. Виллы: Arabian Ranches 3 −18.92%, MBR City −15%, Dubai South −12.45%, Palm −10.55%, Al Furjan +15%. WebSearch добавляет, что медиана запрашиваемой аренды квартир выросла с AED 100,000 в августе до AED 105,000 в сентябре. Это есть только в сниппете поиска, **сама статья не открыта**.

Это год к году и по **листингам**, а не квартал к кварталу и не сделки. В абзац 09/06 («In the second quarter… rents also fell by 2.5%…») это не ложится, поэтому менять его не предлагаю. Если захотите упомянуть, то только после того, как откроется оригинал Arabian Business или релиз Property Finder.

### 3.4. Knight Frank: поправка к §1 файла 13.10

13.10 было записано «последний Dubai residential review в newsroom — Q4 2025». На странице отчёта есть **Q1 2026 от 12.05.2026**. Это не новый выпуск после 13.10, а неточность прошлой проверки. Q2 и Q3 2026 у Knight Frank нет.

### 3.5. E&V: третья страница с другими «августовскими» средними (не новая)

`engelvoelkers.com/ae/en/resources/dubai-housing-market`, «Updated: 9 Sep 2026». В тексте: «As of August 2026… 6.3%. Apartments averaged 6.7%…», а в FAQ на той же странице: «As of July 2026, average residential rental yields remain attractive at 6.58%, including approximately 6.9% for apartments, 5.1% for townhouses and 4.5% for villas». Гипотезу 13.10 (статья 27.08 построена на более раннем срезе) это не подтверждает и не опровергает: июль 6.58 / 6.9 не совпадает с 6.5 / 6.8 из «Highest ROI». В карту не идёт.

---

## 4. Что ждать и когда проверять снова

- **Property Monitor / E&V за September 2026**: не вышел. Прошлый выпуск (August) E&V опубликовал 09.09. Проверить ещё раз около 20–25.10: `rental-yield-dubai` (шапка «Updated») и `lastmod` этого URL в `engelvoelkers.com/ae/sitemap.xml`.
- **CM Q3 2026 полным отчётом**: сайт за WAF. Открыть руками в обычном браузере: `cavendishmaxwell.com/insights/category/market-reports/residential`.
- **Knight Frank**: Q2 2026 не вышел вовсе. Q3 по прошлогоднему циклу около ноября.
- **Bayut**: Q3/9M Bayut с 2024 не выпускает, ждать годовой 2026 в январе 2027. Дата «Updated» на Bayut ориентиром не служит (§1).
- **Savills WCPRI H2 2026**: около февраля 2027.
- **Mendeley v2**: не вышел. Проверять тем же API `/versions`.

---

## 5. Источники (копии в `yield-map-refresh-2026-10-15-sources/`)

| Файл | URL | Дата скачивания |
|---|---|---|
| `ev-rental-yield.html` | https://www.engelvoelkers.com/ae/en/resources/rental-yield-dubai | 15.10.2026 |
| `ev-highest-roi.html` | https://www.engelvoelkers.com/ae/en/resources/highest-roi-in-dubai-real-estate | 15.10.2026 |
| `ev-dubai-housing-market.html` | https://www.engelvoelkers.com/ae/en/resources/dubai-housing-market | 15.10.2026 |
| `ev-ae-sitemap.xml`, `ev-resources.html` | https://www.engelvoelkers.com/ae/sitemap.xml , …/ae/en/resources | 15.10.2026 |
| `bayut-h1.html`, `bayut-sitemap_index.xml`, `bayut-post-sitemap1…5.xml` | https://www.bayut.com/mybayut/dubai-sales-market-report-h1-2026/ , …/mybayut/post-sitemapN.xml | 15.10.2026 |
| `mendeley-versions.json`, `mendeley-v2.json`, `mendeley-dataset.json`, `mendeley-dubai-community-yields-2026-06.csv` | https://data.mendeley.com/public-api/datasets/rwnn99mdz5/versions (и /versions/2, /datasets/rwnn99mdz5, файл CSV) | 15.10.2026 |
| `datacite-datahabibi.json`, `datacite-rental-yields.json` | https://api.datacite.org/dois?query=… | 15.10.2026 |
| `datahabibi-price-index.html`, `datahabibi-communities.csv` | https://datahabibi.ae/dubai/intelligence/price-index , https://datahabibi.ae/api/data/price-index.csv?series=communities | 15.10.2026 |
| `dh-blog-dubai-rental-yields.html`, `dh-about.html`, `dh-sitemap.xml`, `dh-sm-*.xml`, `dh-robots.txt` | https://datahabibi.ae/blog/dubai-rental-yields , /about , sitemaps | 15.10.2026 |
| `pm-archive.html`, `pm-feed.xml`, `pm-sitemap.xml`, `pm-insights-sitemap.xml` | https://www.propertymonitor.com/insights/category/monthly-market-report (+ /feed, sitemaps) | 15.10.2026 |
| `cm-home.html` (0 байт) + `cm-home.headers`, `cm-residential.html` (0 байт) | https://cavendishmaxwell.com/ (WAF 202) | 15.10.2026 |
| `gulfbusiness-cm-q3.html` (403) | https://gulfbusiness.com/en/2026/real-estate/dubai-residential-sales-values-top-dhs72-6bn-across-34000-transactions-in-q3-26/ | 15.10.2026 |
| `zawya-research.html`, `zawya-real-estate.html`, `zawya-search-*.html`, `zawya-savills-nextgen-wealth.html` | https://www.zawya.com/en/press-release/research-and-studies и др. | 15.10.2026 |
| `savills-news*.html` | https://www.savills.ae/insight-and-opinion/savills-news.aspx , savills.com | 15.10.2026 |
| `kf-newsroom.html`, `kf-research.html`, `kf-dubai-resi-review.html`, `kf-press.html` | https://www.knightfrank.ae/research/reports/dubai-residential-market-review-2365 и др. | 15.10.2026 |
| `theweek-rents-1310.html` (403 для curl; текст получен WebFetch), `arabianbusiness-rents-q3.html` (403) | см. §3.3 | 15.10.2026 |
| `txt/` | текстовые выжимки из HTML (скрипт `scripts/totext.py`) | 15.10.2026 |
