# Реклама Meta на покупателей — кит для сборки

Собрано 14.10.2026 по образцу брокерского `05_OPERATIONS:/sales/ads_creatives/ADS_KIT.md`.
Лид-магнит — The Dubai Yield Map, редакция для покупателя. Креативы отрендерены,
тексты и лид-форма написаны. Кампания в кабинете не собрана.

---

## 0. Креативы v3, 16.11.2026 вечер: ОСНОВНОЙ НАБОР

Переделано по её разбору v2: реклама должна быть понятна человеку, который видит её впервые.
- **Никаких названий компаний** (Bayut, Property Monitor) ни на кадрах, ни в текстах. Источники живут сноской внутри карты.
- **«Listing и fact»** вместо «registered data» и «3 sources». Вместо «3 sources» простое «14 Dubai communities».
- **Ни одного процента:** та же пара JVC показана арендой в дирхамах на квартире за AED 1,5 млн
  (7.10% → AED 106,500 в год, 6.3% → AED 94,500; разница AED 12,000 = стр. 04 карты и письмо 2). Поэтому все кадры идут на все плейсменты, включая Instagram.
- **Дубай с первого взгляда:** фото Dubai Marina из брендбука (`01_BRAND:/stock_media/photos/dubai_cityscape/`), без Бурдж-Халифы (правило «ни паруса, ни шпиля»).
- **Purchase Check назван день:** transfer day, и почему: сборы платятся наличными в этот день (с февраля 2025).
- **Без местоимений** (you / your / we): её слово 16.11.

Генератор `05_OPERATIONS:/sales/ads_creatives/build_ads_buyer_v3.py`, кадры `ads_creatives/png_buyer_v3/` (4 × 4x5 / 1x1 / 9x16).
Проверено 16.11: видимого процента 0, названий компаний 0, местоимений 0, стоп-слова 0, anti-AI 0 (SHIP); висячие хвосты склеены и проверены глазами во всех 12 кадрах.

| Кадр | Что на нём |
|---|---|
| `Z1_listing_vs_fact` | DUBAI YIELD MAP. **AED 106,500** «rent a year, as the listing says» / **AED 94,500** коралловая «rent a year, in fact: signed contracts». «The same AED 1.5M apartment in Jumeirah Village Circle, Dubai.» Жирно «Which number to plan on?» |
| `Z2_aed_gap` | BUYING IN DUBAI. **AED 35,000** «a year between the listing and the fact, for one AED 1.5M apartment in Downtown Dubai.» Жирно «Which one is in the offer?» (5.10% / 7.43% × 1,5 млн = 34,950) |
| `Z3_fourteen_communities` | DUBAI YIELD MAP. **14** «Dubai communities. Listing and fact, side by side.» Жирно «Check the area before buying.» |
| `Z4_transfer_day_check` | BUYING IN DUBAI. Крупно «Cash ready on transfer day?» «Since February 2025 the transfer fee and the agent fee are paid in cash on the day, on top of the buyer's own share.» **8** questions, yes or no / **2** minutes to check a purchase. Кнопка «Get the free check» |

**Тексты объявлений (лимиты 125 / 40 / 30, проверено счётчиком):**

| Кадры | Primary text | Headline | Description |
|---|---|---|---|
| Z1, Z2, Z3 | Same Dubai apartment, two rent figures: the listing and the signed contracts. A free map shows both for 14 Dubai communities. (125) | The Dubai Yield Map (19) | Free: 14 Dubai communities (26) |
| Z4 | Buying in Dubai? Transfer and agent fees are paid in cash on transfer day. A 2-minute check: will the money be ready? (117) | The 2-Minute Purchase Check (27) | Free for Dubai buyers (21) |

CTA кнопка Meta: **Download** (лид-форма) или **Learn more** (трафик на сайт).

**Ссылки (если кампания на трафик), `utm_content` = кадр:** `https://nemax-finance.com/yield-map?utm_source=facebook&utm_medium=paid&utm_campaign=yield-map-buyer-q4&utm_content=z1-listing-vs-fact`
(далее `z2-aed-gap`, `z3-fourteen`, `z4-transfer-day`). Строки в `03_INSTAGRAM:/UTM_REGISTRY.md`.

**Стартовая пара:** Z1 + Z3 на все плейсменты, Z2 и Z4 со второй недели (меняем одну переменную за раз).
Набор v2 (Y1–Y4) ниже не ставить: там названия компаний и проценты.

---

## 0a. Креативы v2, 16.11.2026 днём (ЗАМЕНЁН набором v3, не ставить)

В стиле утверждённой обложки (Figma 2421:359): фото башни на весь кадр, синий градиент, две крупные цифры, подпись
«чья это цифра», жирный вопрос, белая кнопка. Генератор `05_OPERATIONS:/sales/ads_creatives/build_ads_buyer_v2.py`,
кадры `ads_creatives/png_buyer_v2/` (4 концепции × 4x5 / 1x1 / 9x16). Висячих слов нет (склейка при рендере),
стоп-слова и anti-AI проверены, 0.

| Кадр | Что на нём | Куда ставить |
|---|---|---|
| `Y1_two_numbers_FB_ONLY` | **7.1%** белая / **6.3%** коралловая: «In the listing / Bayut / September 2026» и «In the registered data / Property Monitor / September 2026», «Same area: Jumeirah Village Circle», жирно «Which number do you plan on?» | ⛔ **Только лента Facebook.** Плейсменты вручную, Instagram снять: правило «никаких процентов в IG». 🔴 Её решение, ставить ли вообще |
| `Y2_aed_gap` | **AED 35,000** «a year. The gap between two published figures for the same AED 1.5 million apartment in Downtown Dubai.» Жирно «Which one were you shown?» | везде, процентов нет. Цифра = стр. 05 карты (5.10% / 7.43% × AED 1,5 млн = 34,950) |
| `Y3_fourteen_three` | **14** Dubai communities / **3** published sources, side by side. «One free table. Every figure with its source and date.» Жирно «See where the numbers do not match.» | везде |
| `Y4_purchase_check` | **8** questions, yes or no / **2** minutes before the payment date. Жирно «Is your money ready on the day?» Фото — башня с обложки Purchase Check | везде. Отдельной страницы у Purchase Check нет: ведёт на ту же /yield-map, оба файла выдаются вместе |

**Тексты объявлений (≤125 / 40 / 30 знаков):**

| Кадры | Primary text | Headline | Description |
|---|---|---|---|
| Y1, Y2, Y3 | Same Dubai area, same month. The listing shows one figure, registered data another. A free map compares 14 areas. | The Dubai Yield Map | Free: 14 areas, 3 sources |
| Y4 | Eight yes-or-no questions before your payment date. Is your money ready for a Dubai purchase? Free, with the Dubai Yield Map. | The 2-Minute Purchase Check | Free for Dubai buyers |

CTA кнопка Meta: **Download** (лид-форма) или **Learn more** (трафик на сайт).

**Ссылка на сайт (если кампания на трафик, а не лид-форма), `utm_content` = кадр:**
`https://nemax-finance.com/yield-map?utm_source=facebook&utm_medium=paid&utm_campaign=yield-map-buyer-q4&utm_content=y1-two-numbers`
(далее `y2-aed-gap`, `y3-fourteen-three`, `y4-purchase-check`). Строки в `03_INSTAGRAM:/UTM_REGISTRY.md`.

**Стартовая пара:** Y2 + Y3 на все плейсменты (оба без процентов), Y1 отдельным объявлением только в ленту Facebook,
Y4 — второй неделей. Старый набор B01–B06 ниже остаётся для сравнения; у B01 подпись — старый хук, его не ставить.

---

## 1. Креативы (набор 14.10–12.11)

Генератор `05_OPERATIONS:/sales/ads_creatives/build_ads_buyer.py`. Вёрстку, цвета, шрифты и склейку
висячих слов он берёт из брокерского `build_ads.py`, поэтому две кампании не разъедутся.
Кадры лежат в `png_buyer/`: шесть концепций, у каждой три формата (4:5 лента, 1:1, 9:16 сторис).

| Файл | Что на нём | Роль |
|---|---|---|
| `B01_seven` | «7» во весь кадр на синем, «reasons the yield you see is not the yield you get», фото-полоса | основной, повторяет форму брокерского победителя `01_seven`. 🔴 16.11: подпись — старый хук, который она забраковала («сломаешь язык»). Перерендер по её выбору подписи, кадр не переделан |
| `B02_listing_contract` | «The number in the listing is not the number in the contract», фото справа | тест против B01: тот же оффер, другая форма |
| `B03_three_sources` | «3» во весь кадр: три источника, три разные доходности (12.11: было «4», колонка E&V снята) | второй кандидат в форме победителя |
| `B04_transfer_day` | «Transfer day is set. Your money is still in another sale.» | ближе к деньгам: причина 07, где у NEMAX есть ход |
| `B05_map_table` | страница 03 карты (таблица) уходит за нижний край | прямой оффер: человек видит, что получит |
| `B06_three_questions` | три вопроса из чек-листа, серый, без фото | тихий кадр для теста |

⛔ **На кадрах нет ни одного процента.** Правило ленты: никаких % и ставок в Instagram, а Meta
показывает эти кадры в Instagram. Разницу в доходности показываем в дирхамах: AED 12,000 в год
на квартире за AED 1,5 млн. Это Jumeirah Village Circle: Bayut Q3 2026 (7.10) против Property Monitor
за сентябрь 2026 (6.3), 0,8 п.п. × 1,5 млн, тот же пример, что на стр. 04 карты. Расчёт наш, иллюстративный.
(До 12.11 было AED 23,100 по Dubai Silicon Oasis за август: снято вместе с августовскими цифрами.)

⛔ **Урок брокерской кампании перенесён:** с 18.09 по 20.09 кадр-документ `05_playbook` дал ноль кликов,
а «7 во весь кадр» дал все заявки. Поэтому основной кадр здесь в той же форме (B01), а кадр с
документом (B05) идёт только тестом.

## 2. Тексты объявлений

Лимиты Meta: основной текст обрезается примерно на 125 знаках, заголовок до 40, описание до 30.

### A. Карта (к B01, B03, B05)

**Primary text**
> Portals, market reports and Land Department data give three different yields for the same
> Dubai community. The map puts them in one table and explains why.

**Headline:** `The Dubai Yield Map`
**Description:** `Free map for Dubai buyers`
(16.11: было `Free, 12 pages` — её слово «зачем столько страниц», число страниц из всех текстов убрано.)
**CTA:** Download

### B. Цифра в объявлении (к B02, B06)

**Primary text**
> The yield in a listing is calculated from asking prices. The yield in registered data is
> calculated from what was signed. Before you buy, check which one you were given.

**Headline:** `Listing yield vs real yield`
**Description:** `Free map for Dubai buyers`
**CTA:** Download

### C. День сделки (к B04)

**Primary text**
> Since February 2025 the transfer fee and the agency fee are paid in cash on the day.
> If your money is still in another sale or abroad, read reason 07 before you sign.

**Headline:** `When your money arrives late`
**Description:** `Free map for Dubai buyers`
**CTA:** Download

⛔ Проверено по стоп-словам: нет `loan`, `lending`, `credit`, `mortgage` о продукте, `financing`
в одиночку, `fast`, `guaranteed`, `passive income`, процентов, ставок. Нет em-dash и эмодзи.

## 3. Лид-форма, дословно

**Тип:** Higher intent.

**Экран 1**
> **The Dubai Yield Map**
> Same Dubai area, same month. The listing shows one yield, the registered data shows another.
> Which one will you plan on? 14 communities, 3 sources, one free table.

(16.11: новый хук, как на первом экране /yield-map, но без процентов: форма открывается в Instagram.
Было «And seven reasons the yield you see may not be the yield you get» — её слово «сломаешь язык».)

**Экран 2**

| Поле | Тип | Зачем |
|---|---|---|
| Full name | из профиля | |
| Email | из профиля | |
| Phone number | из профиля | для звонка, если покупает сейчас |
| `Are you buying a property in Dubai now?` | выбор: `Yes, this month` / `Yes, within 3 months` / `Just researching` | делит на звонок и письма |
| `Do you live in the UAE?` | выбор: `Yes` / `No` | нерезиденту банки обычно дают меньше, это меняет разговор |

**Privacy policy URL:** `https://nemax-finance.com/terms` (отдельного `/privacy` на сайте нет, проверено 07.09).

**Экран 3**
> **Your map is ready.**
> If you are buying this month or within three months, a NEMAX manager comes back within 48 hours.
>
> Кнопка: `Download the map`
> Ссылка: `https://nemax-finance.com/thank-you/yield-map?utm_source=facebook&utm_medium=paid&utm_campaign=yield-map-buyer-q4`

🔴 **Страница `/thank-you/yield-map` собрана 12.11 черновиком в Webflow, не опубликована** (на живом сайте 404).
Пока её нет, форму не запускать. Кит страницы: артефакт claude.ai/artifact/2vckR6eHvGgeSH8hgD6A1H.

## 4. Как собрать кампанию

1. **Событие в пикселе.** Пиксель `681363008312802` → пользовательская конверсия `LEAD`
   `Yield map lead`, правило: URL содержит `/thank-you/yield-map`. Не заведена.
2. **Кампания:** цель Leads → Instant forms.
3. **Группы объявлений** (базы покупателей, как у брокеров, у нас нет, поэтому две широкие):
   - `buyers-uae` — гео UAE, интересы Real estate investing / Property / Dubai, English;
   - `buyers-abroad` — нерезиденты: 🔴 **страны выбрать** (UK, Индия, Германия и т.д. — твоё решение).
4. **Бюджет:** как у брокеров, 25–30 AED в день на группу. Тест: 12–15 лидов, около 14 дней.
5. **Объявления:** по два кадра на группу, один текст на пару (как у брокеров: меняем одну переменную).
   Стартовая пара: B01 + B05 с текстом A.

## 5. Что проверить до первого дня

- [ ] `/yield-map` и `/thank-you/yield-map` опубликованы, PDF карты в Webflow Assets
- [ ] Тестовая заявка видна в Lead Center и уходит уведомлением
- [ ] Конверсия `Yield map lead` создана
- [ ] Ответ «Yes, this month / within 3 months» попадает в выгрузку (у брокеров его не было в CSV Центра лидов)
- [ ] Кто звонит в 48 часов — назначено

## 6. Открытые вопросы по кадрам

1. 🔴 **Слово «yield» на кадрах.** Скилл `/nemax-content` §5a держит `yields` в списке NEVER для ленты, а стоп-слова
   разрешают чужую доходность с источником. Кадры B01–B05 и название карты его используют. Если слово нельзя,
   кадры переписываются генератором за один прогон.
2. 🔴 **Разница доходности в дирхамах** (B02: AED 12,000 в год): по сути это процент, переведённый в деньги.
   Разрешаешь на кадре или оставляем только механизм.
