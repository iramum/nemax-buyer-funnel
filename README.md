# NEMAX: воронка покупателя — Dubai Yield Map, реклама, письма, контент

Обновлено **16.11.2026: страницы в лайве.** Зеркало брокерской воронки ([nemax-broker-ads](https://github.com/iramum/nemax-broker-ads)),
но для конечного покупателя: человека, который покупает квартиру в Дубае как вложение.
Любой файл скачивается так: открыть его → кнопка **Download raw file** (стрелка вниз справа сверху).
Скачать всё разом: зелёная кнопка **Code** → **Download ZIP**.

**Живые страницы:** [nemax-finance.com/yield-map](https://nemax-finance.com/yield-map) → после формы
[/thank-you/yield-map](https://nemax-finance.com/thank-you/yield-map) (карта + Purchase Check + Apply на портал).

## 🔎 Маше на звонок 16.11

1. **Карта, финал** — [PDF для покупателя (стоит на сайте)](map/NEMAX-Dubai-Yield-Map.pdf) и [для брокеров](map/NEMAX-Dubai-Yield-Map-for-brokers.pdf), по 12 страниц.
   Текст, как он стоит в вёрстке: [покупатель](map/YIELD_MAP_BUYER_TEXT_from_Figma_2026-11-16.md), [брокер](map/YIELD_MAP_BROKER_TEXT_from_Figma_2026-11-16.md).
2. **Обложки** — [карта](map/covers/yield-map-cover-C2-2026-11-16.jpg), [брокерская](map/covers/yield-map-cover-broker-2026-11-16.png), [Purchase Check](map/covers/purchase-check-cover-2026-11-16.png).
3. **Purchase Check** — [PDF, 2 страницы](purchase-check/NEMAX-2-Minute-Purchase-Check.pdf): обложка + 8 вопросов, кнопка «Apply now →» на портал.
4. **Реклама, новый набор** — ниже и [ads/ADS_KIT_BUYER.md](ads/ADS_KIT_BUYER.md) §0.
5. **Решить Маше:** в абзацах о NEMAX на стр. 02 и 12 стоит «We» (4 раза), стоп-стандарт его запрещает. Замены готовы: «NEMAX co‑finances…», «NEMAX provides…».

## Что изменилось 16.11

- **Страницы опубликованы** и проверены по живому коду: форма ведёт на страницу выдачи, оба PDF открываются, Apply ведёт на портал Макса с меткой источника.
- **Новый хук первого экрана:** «7.1% in the listing. 6.3% in the registered data.» + подписи, чья цифра, + «Which number do you plan on?». «12 pages» убрано отовсюду.
- **Новая обложка** с двумя крупными цифрами; такая же для брокерской редакции; своя обложка у Purchase Check (8 / 2).
- **Цифры перепроверены 16.11:** новых выпусков нет ([research/yield-map-refresh-2026-11-16.md](research/yield-map-refresh-2026-11-16.md)).
- **Гейты по тексту из Figma:** B2 SHIP, anti-AI 0, стоп-слова чисто. Во всём тексте карты и в Purchase Check короткие слова не висят в конце строки.
- **Apply с UTM везде:** первый экран, страница выдачи, обе PDF, в конце каждого письма ([emails/EMAILS_BUYER.md](emails/EMAILS_BUYER.md)).
- **Почты сотрудников со страниц убраны.**

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
Каждый кадр в трёх форматах: `4x5` лента, `1x1` квадрат, `9x16` сторис.

**Набор v2, 16.11 — основной** ([ads/creatives/0_v2_2026-11-16](ads/creatives/0_v2_2026-11-16)), в стиле обложки:

| `Y1_two_numbers` ⛔ только Facebook | `Y2_aed_gap` | `Y3_fourteen_three` | `Y4_purchase_check` |
|---|---|---|---|
| ![Y1](ads/creatives/0_v2_2026-11-16/NEMAX_ad_Y1_two_numbers_FB_ONLY_4x5.png) | ![Y2](ads/creatives/0_v2_2026-11-16/NEMAX_ad_Y2_aed_gap_4x5.png) | ![Y3](ads/creatives/0_v2_2026-11-16/NEMAX_ad_Y3_fourteen_three_4x5.png) | ![Y4](ads/creatives/0_v2_2026-11-16/NEMAX_ad_Y4_purchase_check_4x5.png) |

Y1 несёт проценты, поэтому идёт только в ленту Facebook (в Instagram процентов не ставим). Y2–Y4 без процентов, на все плейсменты.
Стартовая пара: Y2 + Y3, Y1 отдельно в Facebook, Y4 со второй недели.

**Прежний набор (14.10–12.11), стартовая пара** ([ads/creatives/1_start](ads/creatives/1_start)):

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

## Что ещё не сделано (16.11)

- кампания Meta в кабинете, конверсия `Yield map lead` в пикселе, страны для нерезидентов;
- письма: Brevo пока не пускает ключ (ограничение по IP), автоматизаций на бесплатном тарифе нет; списки под карту и «Apply for Capital» — после доступа;
- брокерская редакция карты: рассылка брокерам из Brevo;
- вход на /yield-map с главной и из статей про доходность;
- 🔴 ноябрьский Property Monitor выше листингов во всех районах — ждёт проверки;
- можно ли «ипотека банка + капитал NEMAX на взнос» — вопрос Максу, до ответа этот ход нигде не предлагается.
