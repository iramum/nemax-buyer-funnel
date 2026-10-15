# Реклама Meta на покупателей — кит для сборки

Собрано 14.10.2026 по образцу брокерского `05_OPERATIONS:/sales/ads_creatives/ADS_KIT.md`.
Лид-магнит — The Dubai Yield Map, редакция для покупателя. Креативы отрендерены,
тексты и лид-форма написаны. Кампания в кабинете не собрана.

---

## 1. Креативы

Генератор `05_OPERATIONS:/sales/ads_creatives/build_ads_buyer.py`. Вёрстку, цвета, шрифты и склейку
висячих слов он берёт из брокерского `build_ads.py`, поэтому две кампании не разъедутся.
Кадры лежат в `png_buyer/`: шесть концепций, у каждой три формата (4:5 лента, 1:1, 9:16 сторис).

| Файл | Что на нём | Роль |
|---|---|---|
| `B01_seven` | «7» во весь кадр на синем, «reasons the yield you see is not the yield you get», фото-полоса | основной, повторяет форму брокерского победителя `01_seven` |
| `B02_listing_contract` | «The number in the listing is not the number in the contract», фото справа | тест против B01: тот же оффер, другая форма |
| `B03_four_sources` | «4» во весь кадр: четыре источника, четыре разные доходности | второй кандидат в форме победителя |
| `B04_transfer_day` | «Transfer day is set. Your money is still in another sale.» | ближе к деньгам: причина 07, где у NEMAX есть ход |
| `B05_map_table` | страница 03 карты (таблица) уходит за нижний край | прямой оффер: человек видит, что получит |
| `B06_three_questions` | три вопроса из чек-листа, серый, без фото | тихий кадр для теста |

⛔ **На кадрах нет ни одного процента.** Правило ленты: никаких % и ставок в Instagram, а Meta
показывает эти кадры в Instagram. Разницу в доходности показываем в дирхамах: AED 23,100 в год
на квартире за AED 1,5 млн. Это Dubai Silicon Oasis: Bayut H1 2026 против Property Monitor
за август 2026, 1,54 п.п. × 1,5 млн. Расчёт наш, иллюстративный.

⛔ **Урок брокерской кампании перенесён:** с 18.09 по 20.09 кадр-документ `05_playbook` дал ноль кликов,
а «7 во весь кадр» дал все заявки. Поэтому основной кадр здесь в той же форме (B01), а кадр с
документом (B05) идёт только тестом.

## 2. Тексты объявлений

Лимиты Meta: основной текст обрезается примерно на 125 знаках, заголовок до 40, описание до 30.

### A. Карта (к B01, B03, B05)

**Primary text**
> Portals, market reports and Land Department data give four different yields for the same
> Dubai community. The map puts them in one table and explains why.

**Headline:** `The Dubai Yield Map`
**Description:** `Free, 11 pages`
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
> Fourteen Dubai communities, four published sources, one table. And seven reasons the yield
> you see may not be the yield you get.

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

🔴 **Страница `/thank-you/yield-map` на сайте сейчас 404** (проверено curl 13.10). Пока её нет, форму
не запускать. Кит страницы: `02_WEBSITE:/pages/yield-map-CANON/` блоки `*-v3.html`.

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
2. 🔴 **Разница доходности в дирхамах** (B02: AED 23,100 в год): по сути это процент, переведённый в деньги.
   Разрешаешь на кадре или оставляем только механизм.
