# NEMAX: воронка покупателя — Dubai Yield Map, реклама, письма, контент

Обновлено 12.11.2026. Зеркало брокерской воронки ([nemax-broker-ads](https://github.com/iramum/nemax-broker-ads)),
но для конечного покупателя: человека, который покупает квартиру в Дубае как вложение.
Любой файл скачивается так: открыть его → кнопка **Download raw file** (стрелка вниз справа сверху).
Скачать всё разом: зелёная кнопка **Code** → **Download ZIP**.

## 🔎 Маше на проверку

1. **Текст карты в Word** — [для покупателя](map/NEMAX-Dubai-Yield-Map-v3-BUYER-for-review-2026-11-12.docx) и [для брокера](map/NEMAX-Dubai-Yield-Map-v3-BROKER-for-review-2026-11-12.docx).
   Жёлтым — цифры и даты для сверки. Зелёным — абзацы из плейбука «7 Reasons» дословно. Красным — вопросы до выпуска.
2. **Как сверстано** — [PDF для покупателя](map/NEMAX-Dubai-Yield-Map-v3-BUYER-DRAFT-2026-11-12.pdf) и [для брокера](map/NEMAX-Dubai-Yield-Map-v3-BROKER-DRAFT-2026-11-12.pdf), по 12 страниц.
3. **По каким правилам написан текст** — [STYLE_MASHA.md](STYLE_MASHA.md): разбор языка плейбука «7 Reasons» и что из него взято.
4. **Откуда вопросы на стр. 11** — [research/REDDIT_QUESTIONS.md](research/REDDIT_QUESTIONS.md).

## Что изменилось 12.11

- **Цифры на ноябрь 2026** ([research/yield-map-refresh-2026-11-12.md](research/yield-map-refresh-2026-11-12.md)):
  Listings = Bayut Q3 2026 (сентябрь), Registered = Property Monitor ноябрь 2026 (страница Engel & Völkers от 12.11),
  DLD data = июньский датасет. Колонка «E&V Aug» снята: в таблице три источника, а не четыре.
  ⚠️ Ноябрьский Property Monitor выше листингов во всех районах, раньше было наоборот. Выгрузку стоит перепроверить.
- Новые примеры: причина 01 = Jumeirah Village Circle 7.10% / 6.3% (сентябрь), причина 02 = Downtown Dubai 5.10% / 7.43%,
  причина 06 = смешанный Q3 и 136,100 домов в 2027 (пресса).
- Текст приведён к правилам ноября: объект держит ADGM SPV, NEMAX co-finances **вместо** банка и не доплачивает
  к ипотеке (взнос по ипотеке только из своих средств), объект с golden visa в SPV не ставится,
  дисклеймер «NEMAX structures asset-backed co-financing secured by real estate and does not operate as a retail bank» на стр. 12.
- Те же правки в письмах (2, 3, 4, 6), Purchase Check, рекламе (B02 = AED 12,000, B03 = «3 sources», B05 = новая таблица) и блоках сайта.
- Страницы `/yield-map` и `/thank-you/yield-map` собраны в Webflow черновиками, не опубликованы.
- Instagram: новая сетка 8 постов с 19.11 (ЧТ + СБ) или с 30.11 (ПН + СР).
- B2: покупатель SHIP (6), брокер 8, из них 4 балла дают оглавление и строка источников. Anti-AI: 0 в обеих.

## Что изменилось 15.10

- Добавлена стр. 11 **«What buyers ask»**: шесть вопросов, которые покупатели задавали на Reddit в августе–октябре 2026, и короткие ответы. Ещё два вопроса вплетены в причины 01 и 03.
- Язык проверен по стандарту B2 проекта (средняя фраза ≤ 16 слов, ни одной длиннее 30, grade ≤ 9):

  | Редакция | Средняя фраза | Фраз длиннее 25 слов | Grade | Итог |
  |---|---|---|---|---|
  | Покупатель | 12,1 слова | 1% | 6,3 | SHIP |
  | Брокер | 12,2 слова | 2% | 6,3 | SHIP |

  Проверка на шаблонные обороты (anti-AI): 0 в обеих.
- Ответ 4 на стр. 11 и причина 04 проверены по Указу Дубая № 43 от 2013 года (ст. 1 и 3), источник стоит в подвале стр. 07.
- Цифры перепроверены 15.10: с 13.10 новых выпусков нет ни у одного источника ([research/yield-map-refresh-2026-10-15.md](research/yield-map-refresh-2026-10-15.md)).

## 🧭 Воронка

**[FUNNEL_BUYER.md](FUNNEL_BUYER.md)**: кого привлекаем, зачем скачивать карту, что человек делает дальше,
когда звонить, что уже готово и чего нет.

![Воронка покупателя](funnel/NEMAX-buyer-funnel-2026-10-13.png)

## 🗺 Лид-магнит: The Dubai Yield Map

Две редакции на одних и тех же страницах: для покупателя («you») и для брокера («your buyer»).

| Файл | Что это |
|---|---|
| [YIELD_MAP_v3_BUYER_TEXT.md](map/YIELD_MAP_v3_BUYER_TEXT.md) / [BROKER](map/YIELD_MAP_v3_BROKER_TEXT.md) | Текст по страницам |
| [research/yield-map-refresh-2026-11-12.md](research/yield-map-refresh-2026-11-12.md) | **Актуально, 12.11:** откуда каждая цифра таблицы, источник, дата, уровень |
| [research/yield-map-refresh-2026-10-13.md](research/yield-map-refresh-2026-10-13.md) | Октябрь: старое → новое |
| [research/yield-map-refresh-2026-10-15.md](research/yield-map-refresh-2026-10-15.md) | Перепроверка 15.10 |

## ✅ Ступень 2: Purchase Check

[NEMAX-2-Minute-Purchase-Check-v1-DRAFT.pdf](purchase-check/NEMAX-2-Minute-Purchase-Check-v1-DRAFT.pdf):
одна страница, восемь вопросов «да / нет», по форме брокерского Deal Check. Кнопка ведёт на портал заявок.

## ✉️ Письма прогрева

[emails/EMAILS_BUYER.md](emails/EMAILS_BUYER.md): email д0 → WhatsApp д2 → email д3, д7, д14 → звонок д21 →
email д30, д45 → раз в квартал. Для тех, кто ответил «Just researching» или молчит.

## 📣 Реклама Meta

[ads/ADS_KIT_BUYER.md](ads/ADS_KIT_BUYER.md): тексты объявлений, лид-форма дословно, аудитории, сборка кампании.
Каждый кадр в трёх форматах: `4x5` лента, `1x1` квадрат, `9x16` сторис. На кадрах нет процентов.

**Стартовая пара** ([ads/creatives/1_start](ads/creatives/1_start)):

| `B01_seven` | `B05_map_table` |
|---|---|
| ![B01](ads/creatives/1_start/NEMAX_ad_B01_seven_4x5.png) | ![B05](ads/creatives/1_start/NEMAX_ad_B05_map_table_4x5.png) |

**Для теста** ([ads/creatives/2_test](ads/creatives/2_test)):

| `B02_listing_contract` | `B03_three_sources` | `B04_transfer_day` | `B06_three_questions` |
|---|---|---|---|
| ![B02](ads/creatives/2_test/NEMAX_ad_B02_listing_contract_4x5.png) | ![B03](ads/creatives/2_test/NEMAX_ad_B03_three_sources_4x5.png) | ![B04](ads/creatives/2_test/NEMAX_ad_B04_transfer_day_4x5.png) | ![B06](ads/creatives/2_test/NEMAX_ad_B06_three_questions_4x5.png) |

## 📱 Контент для Instagram

[instagram/IG_CONTENT_BASE_BUYER.md](instagram/IG_CONTENT_BASE_BUYER.md): опоры, банк тем, план на первые четыре недели, идеи рилсов.

## 🌐 Страницы сайта

[site/](site/): блоки для `/yield-map` и `/thank-you/yield-map` (Webflow Embed). Форма на странице
нативная, её поля расписаны в комментарии блока `22c`. 12.11 обе страницы собраны в Webflow черновиками, не опубликованы.

## Что ещё не сделано

- обложка карты: картинку ставит Ирина;
- публикация `/yield-map` и `/thank-you/yield-map` (canonical, адрес уведомлений формы, обложка, два PDF в Webflow Assets);
- кампания Meta в кабинете, конверсия `Yield map lead` в пикселе;
- отправка писем: Brevo на бесплатном тарифе не даёт автоматизаций;
- вычитка Маши;
- можно ли «ипотека банка + капитал NEMAX на взнос» — вопрос Максу, до ответа этот ход нигде не предлагается.
