# SEO-бриф: Insight «Dubai rental yield 2026» (статья из карты доходности)

Собрано 18.11.2026 по формату брифа Insight #1 (Notion, «SEO Engine & Insight Blog»).
Сам скилл `nemax-insight` лежит на локальном диске (`02_WEBSITE`), в облачной сессии его не было.
Шаги повторены вручную: ключ из Keyword Map → выдача конкурентов → бриф → статья.
Механические гейты (`antiai_gate.py`, `plain_gate.py`) запустить здесь нельзя, текст написан под их правила, прогнать на диске перед `/nemax-publish`.

## Мета

- **Кластер:** Dubai market / analytics · **ICP:** покупатель квартиры как вложения (borrower:individual) · **Воронка:** TOFU → MOFU · **Рубрика:** Market/Analytics (четверговый хаб)
- **Роль:** вход из поиска. Не реклама и не лид-магнит. Внутри две ссылки: бесплатная карта (`/yield-map`) и заявка на портале.
- **Мост к продукту:** седьмая причина карты, «деньги не готовы к дате платежа» (transfer day). NEMAX co-finances вместо банка, от AED 1 млн.
- **Slug:** `/article/dubai-rental-yield-2026`

## Целевые ключи (Keyword Map, все Status = New)

- **Основной:** `dubai rental yield`
- **Вторичные:** `dubai rental yield by area` · `dubai rental yield map` · `dubai rental yield average` · `dubai rental yield percentage` · `dubai rental returns` · `dubai rental yield calculator` · `dubai rental yield reddit` · `dubai rental yield 2025` (год в заголовке 2026, 2025 ловим упоминанием)
- После публикации: эти 9 ключей → Status = Used.

## Интент и читатель

Человек выбирает квартиру в Дубае под сдачу и ищет «какой район даёт больше». Видит в объявлении одну цифру, в отчёте другую.
Ему нужно: таблица по районам, почему цифры расходятся, как посчитать свою (net), что проверить до покупки.
Часть таких читателей уже покупает. У них вторая проблема: деньги на день сделки (transfer day).

## Выдача конкурентов (поиск 18.11.2026, «Dubai rental yield 2026 by area»)

| Кто | Что даёт |
|---|---|
| famproperties.com (брокер) | «best rental yield areas 2026», рейтинг районов |
| engelvoelkers.com (E&V) | «Highest ROI», цифры Property Monitor, средняя 6.5–6.7% |
| realestateclubdubai.com, aigentsrealty.com, dubaiinvest.com.au | «ranked by area», вилки 8–11% без источника |
| joinoliva.com | «Underwrite before you commit», Ejari / DLD |

**Все закрывают:** рейтинг районов, одна цифра на район, gross. Часть даёт вилки без даты и источника.
**Гэп → угол NEMAX:** никто не ставит рядом цифру объявления и цифру зарегистрированных сделок за **один и тот же месяц** и не объясняет, на какую планировать.
Никто не доводит читателя до денег на день сделки. Это и есть наш угол: «The yield in the listing and the yield in fact».

## Title / Meta / H1

- **Title tag (≤ 60):** Dubai Rental Yield 2026: Listing vs Fact, by Area
- **H1:** Dubai rental yield in 2026: the number in the listing and the number in fact
- **Meta (≤ 155):** Dubai rental yields by area for 2026, from listings and from registered deals. Why they differ, how to work out a net yield, and what to check before you buy.
- **OG:** обложка C3 (`map/covers/yield-map-cover-C3-2026-11-16.jpg`) или картинка из набора к статье.

## Аутлайн (≈ 1 700 слов)

1. Лид: 7.1% в объявлении, 6.3% по зарегистрированным сделкам, один район, один месяц.
2. H2 Dubai rental yield by area in 2026 (таблица: 6 районов, обе цифры за сентябрь 2026 + средние)
3. H2 Why the listing yield is usually higher
4. H2 Gross yield vs net yield: the costs the headline leaves out (+ мини-расчёт)
5. H2 Renewals, small samples and dated figures (причины 04–06 сжато)
6. H2 How to check a yield before you commit (чек-лист)
7. H2 The question after the yield: is your money ready on transfer day? (мост, причина 07)
8. H2 Get the full Dubai Yield Map (CTA 1, `/yield-map`)
9. H2 FAQ (5 вопросов, FAQPage JSON-LD)
10. Дисклеймер + источники с датами

## Внутренние ссылки

- `/yield-map` (основной CTA, без UTM: внутренние UTM ломают сессии в GA)
- `apply.nemax-finance.com/?src=insight-yield-map&utm_source=web&utm_medium=insight&utm_campaign=yield-map-buyer-q4&utm_content=cta-apply-article`
- `/article/dubai-cash-vs-bank-finance` (cash vs bank)
- `/article/raising-capital-against-dubai-property` (капитал под свой объект)

## Чек комплаенса и голоса

- «NEMAX», не «we». Продукт: co-finances / asset-backed / secured by the property. Без loan, credit, lender, fast, best, guarantee.
- NEMAX не доплачивает к ипотеке (взнос по ипотеке только из своих средств). Объект с golden visa не ставится.
- Ни одна доходность не подана как доходность NEMAX. Рамка «past results, not a promise».
- Каждая цифра с источником и датой. Цифры только из `research/yield-map-refresh-2026-11-12.md` и `-11-16.md` (проверены).
- 🔴 Ноябрьские цифры Property Monitor (через E&V 12.11) **не берём**: они под вопросом (рост до 1.4 п.п. за 2 месяца при падающей аренде, ответа E&V нет). В статье только сентябрь 2026, обе колонки за один месяц.
- Стиль Маши / B2: фраза 10–16 слов, may / could, без тире, без многоточий, без middot.
- Reddit: только как «вопросы покупателей», без цифр из тредов, без ников.
