# Instagram: контент-база под воронку покупателя (Dubai Yield Map, buyer edition)

Собрано 14.10.2026. Это банк тем и план постов, а не готовые слайды. Слайды и капшены
пишет `/nemax-content` по одной теме за раз, рендерит `/nemax-visual`.

**Что прочитано целиком перед сборкой:** `FUNNEL_BUYER.md`, `YIELD_MAP_v3_buyer_2026-10-13.md`,
`04_RESEARCH:/market_reports/yield-map-refresh-2026-10-13.md`, `04_RESEARCH:/market_reports/individual-dubai-2026-06-28.md`,
`.claude/skills/nemax-content/SKILL.md`, `HOOK_LIBRARY.md`, `_FINAL_REPORT.md`, `ANTI_AI_FILTER.md`,
`WRITING_BENCHMARK.md`, `02_WEBSITE:/seo/ARTICLE_REGISTRY.md`, `03_INSTAGRAM:/OLD-INSTA-THEME-REGISTRY.md`,
память: `nemax-cta-ladder`, `nemax-ig-no-percent`, `nemax-brand-stopwords`, `nemax-ig-teardown-content-rules`,
`nemax-no-licence-never-imply`, `nemax-narrow-to-partner-programme`, `nemax-reach-collapse-not-timing`,
`nemax-week-rhythm-pillars`, `nemax-relative-date-on-slide-rots`, `nemax-case-illustrative-rule`,
`nemax-ig-three-entry-points`, `nemax-utm-in-captions`, плюс `nemax-mortgage-timeline-refuted`,
`nemax-caption-no-cost-paragraph`, `nemax-broker-campaign-audience-split`, `nemax-thursday-monday-spokes`,
`nemax-plain-english-b2-reader`, `nemax-week-0510-built`. Пройдены первые слайды всех 52 папок
`03_INSTAGRAM:/content/` (на перекрытие), `03_INSTAGRAM:/tools/comment_autoreply.json` (какие слова уже заняты).

**Проверено curl 14.10.2026** (`-A "Mozilla/5.0"`): все статьи, которые ниже стоят в паре, отдают **200**.
`/yield-map` и `/thank-you/yield-map` отдают **404**. `apply.nemax-finance.com` отдаёт **200**.
Статьи про аренду и доходность на сайте нет: `/article/rental-yield-dubai` и `/article/dubai-rental-yield` = 404,
в `ARTICLE_REGISTRY.md` такой темы нет, в восьми скачанных статьях слово «yield» не встречается ни разу.

---

## 0. Сначала конфликт, честно

**10.09.2026 ты сузила ленту до партнёрской программы:** ПН + СР, всё непартнёрское в архив
(`nemax-narrow-to-partner-programme`). Причина там же: охват упирается в аудиторию, а не в час.
В июне 7 постов дали 108 подписчикам суммарный охват 170, в августе 14 постов дали 159.
Каждый лишний пост ест охват соседнего (`nemax-reach-collapse-not-timing`).
`FUNNEL_BUYER.md` §7 это повторяет: «внимание покупателя на ступени 0 идёт из поиска и рекламы,
а не из ленты. Менять это или нет — отдельное решение».

Эта база написана под твою новую задачу (конечный покупатель). Как её вписать, решаешь ты.
Четыре варианта, без моей рекомендации как решения:

| Вариант | Что это | Что за | Что против |
|---|---|---|---|
| **A. Отдельный слот ЧТ + СБ** | партнёрка остаётся на ПН + СР, покупатель получает два своих дня | суббота по тирдауну лучший день (Sat 0.249% против Wed 0.158%); партнёрская очередь не трогается | 4 поста в неделю на 108 подписчиков: по данным 10.09 это режет охват каждого поста, а не добавляет людей |
| **B. Покупатель забирает один из ПН/СР** | одна партнёрская + одна покупательская в неделю | каданс остаётся 2 в неделю, как ты решила 10.09 | партнёрская очередь по памяти идёт до 26.10 (Teaser 7). 🔴 **Я не сверяла живой Notion**, задание запрещало его трогать |
| **C. Только реклама + сторис** | темы отсюда уходят в креативы Meta на покупателей (кодом, как `05_OPERATIONS:/sales/ads_creatives/`), в ленте ничего | ступень 0 по `FUNNEL_BUYER.md` и так живёт в рекламе; 88 лидов по ≈$28 пришли из лид-формы, не из ленты | реклама на покупателей не запущена: «аудитории нет, бюджет не решён» (`FUNNEL_BUYER.md` §7, п.9) |
| **D. Только рилсы** | раздел 5 ниже, 1 в неделю, лицо Макса | рилс > карусели (0.21% против 0.12%), лицо ≈ ×3 | рилс 09.09 дал охват 5, то есть в норме аккаунта; без лица выигрыша нет |

Под любой вариант ниже стоят даты для **A** и для **B**. Если выберешь C или D, темы те же, меняется только носитель.

---

## 1. Позиционирование

Покупатель здесь — человек, который берёт квартиру в Дубае как вложение и смотрит, что она будет приносить:
резидент или нерезидент, экспат, владелец бизнеса; для NEMAX интересен тот, у кого покупка от AED 1,43 млн
(минимум капитала NEMAX AED 1 млн = 70% от такой цены, `FUNNEL_BUYER.md`). Ему не нужна ещё одна
цифра доходности: у него их уже три, и они не совпадают. Лента в этой воронке делает одно:
**учит читать чужую цифру** (листинг против реестра, брутто против нетто, среднее по 213 зданиям против
среднего по 36, дата цифры) и **показывает момент, где план ломается деньгами**, а не арендой: день
трансфера, оценка банка, доля банка нерезиденту, финальный платёж на хендовере. Первое ведёт на карту
(ступень 1, когда `/yield-map` заработает), второе ведёт на живые статьи и Purchase Check (ступень 2).
NEMAX появляется только во втором блоке и только как co-financing, когда деньги покупателя не готовы к дате.
Доходностью NEMAX не торгует, своей доходности у NEMAX нет, и ни один процент в ленту не попадает.

**Ось аудитории по скиллу:** `borrower:individual`, хэштег на слайде 1 `#DubaiProperty`.
Сценарии NEMAX из §0.6: **Property Acquisition** и **Final Payment**.
⚠️ В §0 скилла «investors» вне ленты, но там это поставщики капитала (трек `invest.`), а не покупатель-инвестор.
🔴 **Подтверди, что покупатель квартиры «как вложения» = `borrower:individual`.**

### Как решён конфликт «карта про доходность / в IG нет процентов»

Правила, как они записаны в файлах (они главнее задания):

1. **Ставку NEMAX** в IG не пишем никогда (`nemax-ig-no-percent`).
2. **В капшене нет ни одного знака `%`.** Это механический гейт `post_lint.py` и тирдаун (0.133% с процентом против 0.178% без).
3. **На слайде** правило 21.09 разрешает LTV («≤ 70%»), но §5a скилла прямо запрещает `yields` и «any return-%».
   Чужая доходность района = return-%. Поэтому **в этой базе ноль процентов и на слайдах тоже**, кроме LTV ≤ 70% на BOFU-слайде.
4. Чем заменяем процент: **механизмом** («портал считает по ценам объявлений»), **счётом** (213 зданий против 36,
   14 районов, 4 источника, 162 500 домов), **датой** (H1 2026 против August 2026), **AED-суммой** (сборы
   AED 90 000 на квартире AED 1,5 млн) и формулой «the number in the listing is not the number in the contract».
5. **Темы, которые без процента не работают**, помечены ⛔ в банке тем и в разделе 6.

🔴 **Отдельно: само слово «yield».** §5a скилла держит `yields` в списке NEVER. `nemax-brand-stopwords` разрешает чужую
доходность с источником и рамкой «past results, not a promise». Название магнита — «The Dubai Yield Map».
В этой базе **хуки и заголовки слайдов написаны без слова «yield»**, а название карты стоит только в CTA и капшене
как имя собственное, после запуска `/yield-map`. Если запретишь и это, CTA меняется на «Comment MAP for the map of 14 communities».

---

## 2. Рубрики (пиллары) и ступени воронки

Ступени — из `FUNNEL_BUYER.md` §1: **0** внимание / **1** обмен (карта за почту) / **2** активация (Purchase Check).
Стадия ленты по скиллу §3.1: TOFU = 0, MOFU = 1–2, BOFU = 3 (заявка).

| # | Рубрика | Что делает | Ступень | Стадия | Чем закрывается | Страницы карты |
|---|---|---|---|---|---|---|
| **P1** | **Read the number** | Почему одна и та же цифра района у разных источников разная: листинги против реестра, четыре источника, среднее на малом числе зданий, дата цифры | 0 → 1 | TOFU | `Save this` сейчас; `Comment MAP` после запуска `/yield-map` | 03, 04, 05, 08, 09 |
| **P2** | **Gross is not net** | Что съедает аренду: service charge по зданию, пустые недели, комиссия за сдачу, продление вместо нового договора | 0 → 1 | TOFU | `Save this` сейчас; `Comment MAP` после запуска | 06, 07 |
| **P3** | **Cash on transfer day** | Где план покупки ломается деньгами: сборы в кэше с 01.02.2025, банк по меньшей цифре, доля банка нерезиденту, хендовер, деньги в другом объекте | 1 → 2 | MOFU | `Comment <слово>` → **живая** статья; `Comment CHECK` после запуска Purchase Check | 10, 11 |
| **P4** | **The market, dated** | Фон рынка с абсолютными датами: сколько домов сдадут, сколько договоров аренды, сколько продаж в Q3 2026 | 0 | TOFU | `Save this` или `Comment EXIT` (слово живое) | 09 |
| **P5** | **Where NEMAX fits** | Деньги покупателя не готовы к дате → co-financing от AED 1 млн | 2 → 3 | BOFU (мягкий) | `DM STRUCTURE` (портал живой) | 10, 11 |

Пропорция на 4 недели: P1 + P2 + P4 = 5 постов, P3 = 2, P5 = 1. Жёсткий аск один раз за 4 недели, два подряд никогда (§3.4 скилла).

---

## 3. Банк тем (21 идея)

**Как читать колонку CTA:** ✅ = слово можно ставить сейчас (материал живой, 200 на 14.10) /
⏳ = станет валидным только после запуска страницы / 🆕 = слова ещё нет в `comment_autoreply.json`,
его надо завести через `/nemax-utm` с `enabled:false` и включить по твоему ок.
Уже заведены и включены: `PLAYBOOK`, `RELEASE`, `EXIT`, `STRUCTURE`, `HANDOVER` (→ `handoverwave2025`), `QUESTIONS`, `BRIDGE`.
⚠️ У живых `EXIT` и `BRIDGE` в ссылке стоит `utm_campaign=partner-teasers`: клик покупателя ляжет в партнёрскую кампанию.
🔴 **Нужна отдельная запись под покупателя или терпим смешение — решение твоё.**

**Колонка «Источник»:** файл + уровень из него. IDV = `individual-dubai-2026-06-28.md` (вердикт PUBLISH-READY / REWORD / MUST-DROP),
REF = `yield-map-refresh-2026-10-13.md` (PRIMARY / PUBLISHER RELEASE / PRESS), MAP = `YIELD_MAP_v3_buyer_2026-10-13.md`.

**Колонка «Перекрытие»:** с чем пересекается из `03_INSTAGRAM:/content/` и старого реестра (T-номер).

### P1 — Read the number

| # | Стадия | Архетип | Hook (EN, без %) | 10 слайдов одной строкой | Источник каждого факта | CTA | Пара | Перекрытие |
|---|---|---|---|---|---|---|---|---|
| 1 | TOFU / ступень 0→1 | Myth vs Reality | **The number in the listing is not the number in the contract.** | обложка → портал считает по ценам объявлений → цитата Bayut о своём методе → реестр считает по сделкам → у одного района два числа → вторая цифра почти всегда ниже → откуда цифра у агента → три ответа: listings / registered data / DLD records → правило: планировать по меньшей → CTA | Метод Bayut дословно: «reflect advertised listing prices only and are not representative of actual real estate transaction prices» (REF §2.1, **PRIMARY**). «Вторая ниже» = по 12 районам из 14 минимум даёт Property Monitor August 2026 (REF §3.1, **PRIMARY для E&V**). Цифры на слайд не идут | `Save this` ✅ / после запуска `Comment MAP` ⏳🆕 | карта стр. 04 / статьи нет | T14 «6.5% vs 6.0% only one number is real» (старая, с процентами) — угол тот же, подача без цифр. В новой ленте нет |
| 2 | TOFU / 0→1 | Head-to-head comparison | **Four sources. One community. Four different answers.** | обложка → кто считает: объявления → кто считает: реестр → кто считает: август 2026 → кто считает: данные DLD → почему они не совпадают (разная точка сделки) → самый широкий разрыв: JVC → в деньгах: AED 37,500 a year on an AED 1.5m flat → план на диапазон, а не на число → CTA | 4 источника, 14 районов, 46 заполненных ячеек (REF §3.1, вариант A). JVC = самый широкий разрыв (REF §3.1). AED 37,500 = 2.5 п.п. × AED 1,5 млн, пример в самой карте (MAP стр. 05, «illustrative»). | `Save this` ✅ / `Comment MAP` ⏳🆕 | карта стр. 03, 05 | нет. 🔴 **AED 37,500 — это процент в дирхамах.** Слайд 8 ставим только с твоего разрешения, иначе слайд 8 = «The gap on one flat can be a month's rent or more» без суммы. 🔴 Зависит от выбора варианта A/B таблицы (REF §5 вопрос 1) |
| 3 | TOFU / 0→1 | Number deep-dive | **213 buildings behind one average. 36 behind another.** | обложка → что такое среднее по району → JVC: 213 зданий → Dubai Hills Estate: 36 → JLT: 39 → одна новая башня двигает малое среднее → среднее ничего не говорит о твоём здании → что смотреть вместо: недавние договоры в этом здании → где это видно (колонка n на карте) → CTA | n зданий: JVC 213, International City 220, Dubai Hills 36, JLT 39 (REF §2.3, Mendeley DOI 10.17632/rwnn99mdz5.1, **PRIMARY**, датасет June 2026, скачан и сверен 13.10) | `Save this` ✅ / `Comment MAP` ⏳🆕 | карта стр. 08 | нет. ⚠️ n есть только в июньском Mendeley; если выберешь вариант B таблицы (живой dataHabibi), тема умирает (REF §3.2) |
| 4 | TOFU / 0→1 | Trend / What changed | **Check the date before you check the number.** | обложка → у каждой цифры есть дата → одна и та же страница переписана 09.09.2026 → апрельских цифр больше нет онлайн → цены за Q2 2026 и Q3 2026 двигались (словами) → за Q3 2026 изменение аренды не опубликовал никто из найденных → цифра прошлого года не про сегодня → если планируешь продажу, смотри и прогноз цены → правило: спрашивай дату → CTA | Страница E&V `rental-yield-dubai` переписана, «Updated: 9 Sept 2026» (REF §2.2, §2.5, **PRIMARY**). Цены падали в Q2 и Q3 2026: CM H1 (REF §2.7, **PUBLISHER RELEASE**) и Savills Q3 12.10.2026 (**PUBLISHER RELEASE**) — **на слайд только словами, без величины**. Аренда Q3 в процентах не найдена (REF §5 п.7) | `Save this` ✅ / `Comment MAP` ⏳🆕 | карта стр. 09 | нет |
| 5 | TOFU / 0→1 | Save-worthy checklist (Mechanism walkthrough) | **Six questions to ask before you plan the rent.** | обложка → откуда цифра → сравни два источника → service charge этого здания → новый договор или продление → дата цифры → когда придут деньги, включая сборы → итог: шесть вопросов на одном слайде для скрина → CTA | Чек-лист «Before you commit» (MAP стр. 11) | `Save this` ✅ / `Comment MAP` ⏳🆕 (чек-лист = стр. 11 карты) | карта стр. 11 | T13 «5 Dubai investor traps», T9 «What no one prepares you for as a first-time investor» — старые, другие пункты |

### P2 — Gross is not net

| # | Стадия | Архетип | Hook (EN, без %) | 10 слайдов одной строкой | Источник | CTA | Пара | Перекрытие |
|---|---|---|---|---|---|---|---|---|
| 6 | TOFU / 0→1 | Mechanism walkthrough | **The rent is not what you keep.** | обложка → опубликованная цифра = год аренды, делённый на цену → в ней нет service charge → нет пустых недель → нет комиссии за сдачу → вычитаем по шагам → получаем цифру нетто → нетто считается по зданию, не по району → план покупки по нетто → CTA | «Published yields are gross… do not include service charges, empty weeks between tenants or letting fees» (MAP стр. 06). Механизм, внешних чисел нет | `Save this` ✅ / `Comment MAP` ⏳🆕 | карта стр. 06 | **закрывает пробел T18 «Аренда / нетто»** из старого реестра: в ленте этого не было никогда |
| 7 | TOFU / 0→1 | Definition / Primer | **Same community. Different service charge.** | обложка → service charge ставится по зданию → внутри одного района разница большая → кто утверждает: RERA, the Dubai property regulator → где смотреть: Dubai REST app → или сайт DLD (Mollak) → шаги: проект / назначение / год → результат сразу → что с ним делать: вычесть из аренды → CTA | Страница DLD «Service Charge Index», «last updated 07 October 2026»: три канала, шаги «project, uses, year», «Immediate», «Residency status: All» (REF §2.10, **PRIMARY**). ⛔ «It is free» не подтверждено | `Save this` ✅ / `Comment MAP` ⏳🆕 | карта стр. 06 | T10 «Service Charges Before Handover» — другое правило, не пересекается |
| 8 | TOFU / 0→1 | Number made tangible | **One empty month takes a twelfth of the year.** | обложка → 11 месяцев из 12 → в деньгах на примере → между жильцами бывает ремонт и показы → комиссия за новую сдачу → продление дешевле, но ниже → как считать: 11 месяцев, а не 12 → спроси агента, сколько квартира стояла пустой → нетто по зданию → CTA | Арифметика из MAP стр. 06 («let for 11 months out of 12»). 🔴 **Пример аренды AED 90 000 в год (AED 7 500 месяц) — моё допущение**, на слайде с пометкой «illustrative» | `Save this` ✅ / `Comment MAP` ⏳🆕 | карта стр. 06 | нет |
| 9 | TOFU / 0→1 | FAQ explainer | **A sitting tenant changes the maths.** | обложка → квартира с жильцом и пустая квартира → продление ограничено индексом аренды → новый договор по рынку → цифра района смешивает оба → что спросить: договор и дата окончания → если сдана: план по текущей аренде до конца договора → если пустая: недавние договоры в этом здании → вывод → CTA | Механизм из MAP стр. 07. 🔴 **Первоисточник индекса аренды (RERA rental index) в ресёче 13.10 не открыт** — открыть до поста. ⛔ Сплит new lets / renewals (6.98 / 6.40) не использовать: больше не опубликован (REF §2.5) | `Save this` ✅ / `Comment MAP` ⏳🆕 | карта стр. 07 | нет |

### P3 — Cash on transfer day

| # | Стадия | Архетип | Hook (EN, без %) | 10 слайдов одной строкой | Источник | CTA | Пара | Перекрытие |
|---|---|---|---|---|---|---|---|---|
| 10 | MOFU / 1→2 | Number deep-dive | **AED 1.5m flat. AED 90,000 due in cash on the day.** | обложка → план считали по аренде, а ломается в день трансфера → transfer fee DLD в деньгах → agency fee в деньгах → since 1 February 2025 banks have been told not to include them → плюс своя доля цены → деньги лежат в другом месте → что спросить у агента: полная сумма на день трансфера → когда придут твои деньги → CTA | Upfront costs ≈ 6–7%, The National 25.01.2025 (IDV, **PUBLISH-READY**). Правило 01.02.2025: The National, без номера циркуляра, формулировка «have been told» (IDV **REWORD**, REF §2.9). AED 60 000 + AED 30 000 = 4% и 2% от AED 1,5 млн, пример с пометкой «illustrative» | `Comment FEES` ✅🆕 → `/article/dld-fees-dubai` (200, в статье «1 February 2025» ×5) | карта стр. 10 / статья dld-fees-dubai | ⚠️ сильное: `you-asked-cash-to-buy` (CASH), `myths-financing-dubai`, `dld-six-lines` (брокер), `dubai-2026-3-shifts`. Новый угол только один: **план инвестора построен на аренде, а рушится в первый день кэшем**. Без этого угла не ставить |
| 11 | MOFU / 1→2 | Myth vs Reality | **The bank lends on the lower number.** | обложка → договорились о цене → банк оценил ниже → банк считает от меньшей из двух → пример в AED → разницу закрываешь сам, в кэше → и сборы сверху → когда это видно: до трансфера, если спросить → что спросить у банка до задатка → CTA | «LTV applied to the lower of price / valuation» (IDV, **PUBLISH-READY**, CBUAE через DLA Piper). Пример: цена AED 1,5 млн, оценка AED 1,4 млн, доля банка четыре пятых → своих денег AED 380 000 вместо AED 300 000 (+AED 80 000), «illustrative». ⛔ «~12% discount» — MUST-DROP | `Comment VALUE` ✅🆕 → `/article/how-long-mortgage-approval-dubai` (200; «lower of» ×4; орфан, 0 входящих — пост даст ей вход) | статья how-long-mortgage-approval-dubai | ⚠️ сильное: `teaser4-valuation-gap` (в лайве с 08.10), `you-asked-valuation-gap`, `myths-financing-dubai`. 🔴 **Ставить не раньше декабря или не ставить** |
| 12 | MOFU / 1→2 | Pain → bridge | **Living abroad, the bank often funds about half.** | обложка → нерезидент покупает квартиру под сдачу → банки обычно дают нерезиденту около половины → это политика банков, а не норма ЦБ → пример AED 2 млн: своя доля AED 800 000–1 000 000 → плюс сборы → деньги за границей и перевод занимает время → что проверить: дату перевода против даты платежа → куда идти, если деньги не успевают → CTA | «Banks typically lend 50–60% to non-residents», bank policy, NOT a CBUAE cap (IDV **REWORD**). На слайд словами («about half»), без процента. AED-пример «illustrative» | `Comment ABROAD` ✅🆕 → `/article/non-resident-mortgage-dubai` (200) | статья non-resident-mortgage-dubai | ⚠️ `you-asked-non-resident`, `teaser2-nonresident-wall` (брокер), `myths-financing-dubai`. Угол: **инвестор-нерезидент, деньги за границей** |
| 13 | MOFU / 1→2 | Pain → bridge | **Off-plan: at handover the bank funds at most half.** | обложка → купил off-plan под сдачу → хендовер назначен → банк на off-plan даёт не больше половины стоимости → остаток в деньгах → сроки сдвигаются → где взять финальный платёж → что проверить: дату и сумму финального платежа сейчас → вариант без продажи → CTA | Off-plan LTV capped 50%, CBUAE verbatim (IDV, **High**). ⛔ 69,6% off-plan сделок (Med, вторичный) не брать | `Comment FINAL` ✅🆕 → `/article/off-plan-final-payment-dubai` (200). Живое `HANDOVER` ведёт на другую статью (handoverwave2025) | статья off-plan-final-payment-dubai | ⚠️ сильное: `off-plan-handover`, `teaser1-handover-shortfall`, `you-asked-handover-slipped`, T5 (8 старых). 🔴 **Только если хочешь закрыть страницу 10 карты постом; иначе пропустить** |
| 14 | MOFU / 1→2 | Pain → bridge | **Your money is in another flat. The payment date is not.** | обложка → новая квартира выбрана → деньги в старой → продажа старой не успевает к дате → что будет, если не заплатить вовремя → продать дёшево — дорогой выход → поднять капитал под уже свою квартиру → что проверить → CTA | Механизм (MAP стр. 10). Без внешних чисел | `Comment BRIDGE` ✅ (живое, но UTM партнёрский) → `/article/bridge-financing-dubai` (200) или `Comment RELEASE` ✅ → `/article/equity-release-dubai` (200) | статья bridge-financing-dubai / equity-release-dubai | ⚠️ `reason2-sell-before-buy` (09.10, брокер, тоже BRIDGE), `unlock-without-selling`, `equity-release-ceiling` |
| 15 | MOFU / 1→2 | Pain → bridge | **Funds abroad. Transfer day in Dubai.** | обложка → деньги на счёте за границей → банк-отправитель и банк-получатель держат проверку → дата трансфера в Дубае не двигается → сборы в день трансфера → что спросить у агента → что проверить у своего банка → вариант, если не успевает → CTA | Механизм (MAP стр. 10, FUNNEL §2 таблица болей). Без внешних чисел. 🔴 Сроков международного перевода в ресёче нет, на слайд сроки не ставить | `Save this` ✅ (у темы нет своей статьи; `ABROAD` занят темой 12) | карта стр. 10 | ⚠️ `reason6-money-from-abroad` (брокер). Памятка 07.10: «статьи-пары нет» |
| 16 | MOFU / ступень 2 | FAQ explainer | **Eight questions. Two minutes. Is your money ready?** | обложка → 8 вопросов Purchase Check по одному на слайд (объект в ОАЭ и сумма, оценка, сборы, нерезидент, деньги в другом месте, хендовер, срок Form F, план выхода) → шкала 7–8 / 4–6 / 0–3 → CTA | Черновик вопросов (FUNNEL §5). Срок Form F: «can be forfeited», не «is forfeited» (IDV **REWORD**) | `Comment CHECK` ⏳🆕 — **только после запуска Purchase Check** (статус 🟡 черновик). До запуска тему не ставить | Purchase Check | `five-questions-before-you-sign` (брокер), `you-asked-form-f-clock` |

### P4 — The market, dated

| # | Стадия | Архетип | Hook (EN, без %) | 10 слайдов одной строкой | Источник | CTA | Пара | Перекрытие |
|---|---|---|---|---|---|---|---|---|
| 17 | TOFU / 0 | Market / Data report | **162,500 new homes are due in 2027.** | обложка → сколько домов ждут в 2027 → больше 525 000 в 2027–2030 → больше предложения = аренда под давлением → новые башни рядом с твоей → что это значит для продажи через несколько лет → что это значит для арендатора → что проверить: сколько сдаётся рядом → дата каждой цифры на слайде → CTA | 162 500 в 2027 / 128 200 в 2028: Cavendish Maxwell H1 2026 на Zawya (REF §2.7, **PUBLISHER RELEASE**). «More than 525,000 units… between 2027 and 2030»: Savills Q3 2026, Zawya 12.10.2026 (**PUBLISHER RELEASE**) | `Comment EXIT` ✅ (живое) → `/article/dubai-supply-vs-exit-2026` (200) | статья dubai-supply-vs-exit-2026 / карта стр. 09 | T8 «Delivery Risk = Capital Risk» (2025), `prices-and-depth-fell`. ⚠️ Память `nemax-supply-vs-exit-depth-claim`: 24 800 — другой счётчик, сдачу за полугодие не ставить (REF §2.7: Savills 27 300 за квартал против CM 24 800 за полугодие) |
| 18 | TOFU / 0 | Number deep-dive | **181,900 rent contracts in three months.** | обложка → Q3 2026: 181 900 договоров аренды → это больше, чем в Q2 → Savills: «early signs of stabilisation» → изменение аренды за Q3 2026 не опубликовал никто из найденных → значит средняя по городу молчит → смотри договоры в своём здании → где их видно → CTA | 181 900 rental transactions, «early signs of stabilisation»: Savills Q3 2026, 12.10.2026 (REF §2.7, **PUBLISHER RELEASE**). Рост к Q2 словами, без процента. Отсутствие Q3-процента у всех источников (REF §5 п.7) | `Save this` ✅ | карта стр. 09 | нет |
| 19 | TOFU / 0 | Market / Data report | **About 34,500 home sales in Q3 2026. Fewer than a year before.** | обложка → сколько продаж в Q3 2026 → сколько денег прошло → меньше, чем год назад → цена, которую ты платишь, это половина формулы → при меньшем числе покупателей торг возможен → цифра в объявлении — цена продавца → что проверить: зарегистрированные сделки в здании → CTA | ~34 500 сделок, AED 70,8 млрд: Savills Q3, 12.10.2026 (**PUBLISHER RELEASE**). CM: ~34 000, AED 72,6 млрд — The National 07.10.2026 (**PRESS**). Брать Savills, расхождение указать в `sources`. Падение год к году — словами | `Comment EXIT` ✅ → `/article/dubai-supply-vs-exit-2026` | статья dubai-supply-vs-exit-2026 | `prices-and-depth-fell` (H1 2026) — это продолжение на Q3 |

### P5 — Where NEMAX fits

| # | Стадия | Архетип | Hook (EN, без %) | 10 слайдов одной строкой | Источник | CTA | Пара | Перекрытие |
|---|---|---|---|---|---|---|---|---|
| 20 | BOFU (мягкий) / 2→3 | The Reframe | **The flat works on paper. The cash is not ready on the day.** | обложка → аренда посчитана, квартира выбрана → деньги в другом объекте или за границей → сборы в день трансфера → THE REFRAME: «This is not a rent problem. It is a date problem.» → co-financing: ты вносишь свои, NEMAX добавляет капитал → обеспечение → LTV ≤ 70% (только на слайде, не в капшене) → от AED 1 млн → что сказать: объект, что мешает, дата платежа → CTA | Абзац «When to contact NEMAX Finance» (MAP стр. 11). AED 1 млн минимум (FUNNEL §1). LTV ≤ 70% (скилл §0). 🔴 **Обеспечение — см. вопрос 5 в разделе 6**: «the property you are buying» (карта v3, плейбук v4) против «there has to be a UAE property to work from» (плейбук v2). До ответа Макса слайд 7 не пишется | `DM STRUCTURE` ✅ (портал 200) | apply.nemax-finance.com | `six-situations-nemax`, `unlock-without-selling`, T7 |
| 21 | BOFU (мягкий) / 2→3 | FAQ explainer (You asked) | 🔴 **Нужен настоящий вопрос**, например из Reddit или директа: «I found the flat, but my money is still in my old one. Can I buy first?» | обложка-вопрос → почему банк не помогает → что можно → что спросить → CTA | 🔴 Reddit — только «ситуация», не статистика (IDV **MUST-DROP** для чисел); вопрос открыть целиком (`reddit_threads.py`) | `DM STRUCTURE` ✅ | apply.nemax-finance.com | ⚠️ рубрика YOU ASKED (суббота) архивирована 10.09 |

---

## 4. План на первые 4 недели (8 постов)

Под оба варианта. **Вариант A:** ЧТ + СБ, сторис на следующий день.
**Вариант B:** ПН + СР, сторис на следующий день. ⚠️ По памяти ПН/СР до 26.10 заняты партнёрской очередью (26.10 = Teaser 7),
🔴 **не сверено с живым Notion**.

UTM для всех стикеров ниже: `utm_source=instagram&utm_medium=stories&utm_campaign=` 🔴 **`ig-buyer-q4`** (моё предложение,
в реестре такой кампании нет) `&utm_content=<слаг>`. Все слаги с префиксом `buyer-` проверены в `03_INSTAGRAM:/UTM_REGISTRY.md` 14.10: не заняты.
Ссылка во втором комментарии к посту: тот же адрес с `utm_medium=social` и `utm_content=<слаг>-comment` (правило 17.08).
Перед сборкой: открыть Notion-реестр UTM `3b8f63741cd7816587baf23f1150d1be` (правило 21.09), потом `/nemax-utm`.

| # | Тема (банк) | Вар. A | Вар. B | Стадия | CTA сейчас | Первая строка капшена (EN, черновик) | Сторис (3 кадра) |
|---|---|---|---|---|---|---|---|
| 1 | #1 The number in the listing is not the number in the contract | **ЧТ 22.10.2026**, сторис ПТ 23.10 | ПН 19.10.2026, сторис ВТ 20.10 | TOFU | `Save this`; капшен закрывается вопросом «Which number were you shown first?» | Bayut says it in its own report: its figures use advertised prices, not the prices buyers actually paid. | tease: обложка / engage: **quiz** «Where does a portal's number come from? Listings / Contracts» / drive: стикера-ссылки нет (на 23.10 вести некуда), `sticker: none`, кадр «Save the post» |
| 2 | #10 AED 1.5m flat. AED 90,000 due in cash on the day | **СБ 24.10.2026**, сторис ВС 25.10 | СР 21.10.2026, сторис ЧТ 22.10 | MOFU | `Comment FEES` → dld-fees-dubai | You counted the rent. The first problem arrives before the first tenant does: the day of transfer. | tease / engage: **poll** «Did you count the fees as cash? Yes / No» / drive: link → `https://nemax-finance.com/article/dld-fees-dubai?utm_source=instagram&utm_medium=stories&utm_campaign=ig-buyer-q4&utm_content=buyer-transfer-day-cash` |
| 3 | #6 The rent is not what you keep | **ЧТ 29.10.2026**, сторис ПТ 30.10 | ПН 26.10.2026 ⚠️ занято Teaser 7 | TOFU | `Save this`; вопрос «What do you subtract first?» | A published figure divides one year of rent by the price. Nothing else goes into it. | tease / engage: **quiz** «Which cost is inside the published number? Service charge / None» / drive: `none` (после запуска карты: link → `/yield-map`) |
| 4 | #17 162,500 new homes are due in 2027 | **СБ 31.10.2026**, сторис ВС 01.11 | СР 28.10.2026, сторис ЧТ 29.10 | TOFU | `Comment EXIT` (живое; UTM партнёрский, см. вопрос 7) | Cavendish Maxwell counts 162,500 homes due in 2027. Savills counts more than 525,000 between 2027 and 2030. | tease / engage: **poll** «Buying to rent or to sell later?» / drive: link → `https://nemax-finance.com/article/dubai-supply-vs-exit-2026?utm_source=instagram&utm_medium=stories&utm_campaign=ig-buyer-q4&utm_content=buyer-supply-2027` |
| 5 | #3 213 buildings behind one average. 36 behind another | **ЧТ 05.11.2026**, сторис ПТ 06.11 | ПН 02.11.2026, сторис ВТ 03.11 | TOFU | `Save this`; если `/yield-map` к этой дате живая (проверить curl в день поста): `Comment MAP` | One community average rests on 213 buildings. Another rests on 36. | tease / engage: **quiz** «Which average moves more when one tower opens? 213 / 36» / drive: `none` или link → `/yield-map` после запуска |
| 6 | #12 Living abroad, the bank often funds about half | **СБ 07.11.2026**, сторис ВС 08.11 | СР 04.11.2026, сторис ЧТ 05.11 | MOFU | `Comment ABROAD` → non-resident-mortgage-dubai | You live abroad and buy a flat to let in Dubai. The bank's share is set by its own policy, and it is often about half. | tease / engage: **question** «What is your money waiting for?» / drive: link → `https://nemax-finance.com/article/non-resident-mortgage-dubai?utm_source=instagram&utm_medium=stories&utm_campaign=ig-buyer-q4&utm_content=buyer-nonresident-half` |
| 7 | #5 Six questions to ask before you plan the rent | **ЧТ 12.11.2026**, сторис ПТ 13.11 | ПН 09.11.2026, сторис ВТ 10.11 | TOFU → ступень 1 | `Save this`; после запуска карты `Comment MAP` (чек-лист = стр. 11) | Six questions. Ask them before you plan a single month of rent. | tease / engage: **poll** «Which one have you never asked? Source / Service charge» / drive: link → `/yield-map` только если 200, иначе `none` |
| 8 | #20 The flat works on paper. The cash is not ready on the day | **СБ 14.11.2026**, сторис ВС 15.11 | СР 11.11.2026, сторис ЧТ 12.11 | BOFU мягкий | `DM STRUCTURE` | The rent is planned. The flat is chosen. The money is still in another property. | tease / engage: **question** «When is your payment due?» / drive: **dm** `DM STRUCTURE` (или link → `https://apply.nemax-finance.com/?utm_source=instagram&utm_medium=stories&utm_campaign=ig-buyer-q4&utm_content=buyer-cash-not-ready`). 🔴 блокирован вопросом 5 |

**Что держит план:**
- каждый пост: 10 слайдов, капшен 1500–2150 знаков с хэштегами, жёсткий потолок 2200, 4–8 тегов,
  ноль `%` и ноль ссылок в капшене, ноль `—` на слайдах и не больше одного в капшене, ноль middot, только абсолютные даты
  («since 1 February 2025», «in Q3 2026», «June 2026»), никогда «last year / recently»;
- в капшене нет абзаца про стоимость (`nemax-caption-no-cost-paragraph`): длину добираем примером или «когда не подходит»;
- хэштеги из проверенных: `#NEMAXFinance #cofinancing #dubaiproperties #realestatedubai #dubaiinvestment #dubailife`
  (`#dubaigoldenvisa` только где тема рядом с резидентством, пост 6); не брать `#dubairealestate #realestate #investing #realestateinvesting #mortgageuae`;
- на слайде 1 тег аудитории `#DubaiProperty`; дисклеймер на последнем кадре — константа `/nemax-visual`;
- на постах с внешними цифрами строка источника на последнем слайде («Source: Savills / Q3 2026»), в JSON блок `sources` с URL и датой;
- новые слова (`FEES`, `ABROAD`) заводятся в `comment_autoreply.json` с `enabled:false` и включаются по твоему ок;
- гейты по порядку: `antiai_gate` → B2 (`plain_gate.py`) → компл. повторно → `nemax_sync.py --lint-only`.

---

## 5. Рилсы (6 идей)

По тирдауну: talking-head, лицо (≈ ×3), 90 секунд и дольше — верхний диапазон (0.323%), хук в первые 1,5 секунды,
CTA словом. Лицо: Макс. Если в кадре другой сотрудник, подпись «A NEMAX manager».
Сборка `/nemax-reel` (ffmpeg из слоёв Figma, Canva анимацию не умеет).

| # | Хук в первые 1,5 с (EN) | Что внутри | Длина | Источник | CTA |
|---|---|---|---|---|---|
| R1 | **"Ask the agent one question before you sign."** | Макс в кадре: «Where does this number come from?» → три ответа (listings / registered data / DLD records) → что делать с каждым | 90 с+ | Bayut метод (REF §2.1 **PRIMARY**), MAP стр. 04 | `Save this` / ⏳ `Comment MAP` |
| R2 | **"This is how you check a service charge in under a minute."** | Запись экрана Dubai REST: Services → Service Charge Index → project / usage / year. Голос за кадром. ⛔ Не говорить «free» | 60–90 с | DLD страница и листовка (REF §2.10 **PRIMARY**) | `Save this` |
| R3 | **"AED 1.5 million flat. Here is the cash you need on day one."** | Макс на доске: доля цены + transfer fee + agency fee = сумма дня трансфера; «since 1 February 2025» | 90 с+ | IDV PUBLISH-READY + REWORD, AED «illustrative» | `Comment FEES` ✅🆕 |
| R4 | **"213 buildings or 36. Which average would you trust?"** | Две колонки, одна новая башня двигает малое среднее | 60–90 с | Mendeley n (REF §2.3 **PRIMARY**) | `Save this` / ⏳ `Comment MAP` |
| R5 | **"A flat with a tenant and an empty flat are two different purchases."** | Продление против нового договора, что спросить у агента, чей договор и до какой даты | 90 с+ | MAP стр. 07; 🔴 первоисточник индекса аренды открыть до съёмки | `Save this` |
| R6 | **"The money is abroad. The transfer is in Dubai. Same week."** | История в третьем лице, без имён и сумм, ситуация из таблицы болей; NEMAX в конце как co-financing от AED 1 млн | 90 с+ | FUNNEL §2, MAP стр. 10–11. 🔴 обеспечение — вопрос 5 | `DM STRUCTURE` |

---

## 6. Чего НЕ использовать и открытые вопросы

### 6.1. Факты, которые в ленту не идут

**Из `individual-dubai-2026-06-28.md` (вердикты):**
- ⛔ MUST-DROP: средняя цена «AED 2,71 млн / +7,5% YoY»; «~12% дисконт оценки» (подкаст); любые цитаты Reddit как статистика (только как «ситуация»).
- ⚠️ REWORD, иначе не ставить: нерезидент «50–60%» только как «banks typically lend…», **политика банков, не норма CBUAE**, и в IG словами («about half»), не процентом;
  Form F: «can be forfeited», не «is forfeited»; правило о сборах 01.02.2025: ссылка на The National 25.01.2025, **никогда номер циркуляра**, не «published regulation».
- Не проверено, не ставить: макро 2025 «200 814 сделок / AED 543,9 млрд» (сверить с DLD); «69,6% сделок off-plan» (Med, вторичный); «~30% ипотечных запросов от новых экспатов» (Med); «bridge ~1–1,75%/мес» (это ставка, в IG запрещено навсегда).

**Из `yield-map-refresh-2026-10-13.md`:**
- ⛔ Пример «Discovery Gardens 9.06% в листингах против 7.41% в контрактах»: 7.41% больше не опубликован (REF §5 вопрос 3).
- ⛔ Апрельские средние Property Monitor 6.68 / 7.15 / 4.98 и сплит new lets 6.98 / renewals 6.40: страница переписана, онлайн их нет.
- ⛔ Слово «contracts» для колонки Property Monitor August 2026: на странице E&V так не написано, предложено «registered data».
- ⛔ Живой dataHabibi 6.4% по городу и его районные цифры против июньского Mendeley 8.16%: противоречие внутри источника, метод не описан.
- ⛔ Dubai Investments Park (4.89 / 8.53 / 9.61 / 9.7) и Dubai Production City: разброс почти пять пунктов, в таблицу не вошли.
- ⛔ «It is free» про Dubai REST: не подтверждено ничем.
- ⛔ Arabian Business «asking rents fall up to 22%» (403, провайдер не назван); статья Khaleej Times про «Q3» — это Q3 **2025**; страница Savills «Rents and Yields» — данные **2022**;
  Bayut «Home Loans» про три четверти сборов в ипотеке — старый текст под свежей датой.
- ⛔ Противоречия, которые нельзя подавать одной цифрой: аренда Q2 (CM −2.5% против Savills −8–10%), сдача Q2 (Savills 27 300 за квартал против CM 24 800 за полугодие), запуски Q2 (36 400 против 5 335), S&P «5–15%» (PRESS).
- ⛔ Тезис «affordable расходятся на полтора пункта, prime больше чем на два»: после обновления не держится.
- Любой процент из таблицы карты, Savills −10%, Savills −4.8% / −1.7%, CM −2.5%, ValuStrat: на слайд и в капшен **не идут** (правило про %). Тема, которой нужен такой процент, в банк не взята.

**Из памяти проекта:**
- ⛔ «Одобрение ипотеки 6–8 месяцев»; «ENBD 24 ч / ADCB 48 ч»; «DLD 30–60 минут»; «4 000–4 500 ипотек в месяц». Скорость против банка больше не аргумент (`nemax-mortgage-timeline-refuted`): «target 30-day closing» можно как условие, нельзя как «быстрее банка».
- ⛔ «Only one in five closes»; имена сотрудников, кроме Макса; любой намёк на лицензию (подписи, оси, плашки); «Loan-to-Value»; «loan / lending / lender / financing / fund»; «we» как субъект бренда; «me / tell me»; «no monthly payments»; относительные даты.
- ⛔ «Within 48 hours» из писем прогрева (FUNNEL §6): в ленту не ставить, пока это не подтверждённое условие продукта.

### 6.2. Темы, которые без процента не работают (в банк не взяты)

- «Самый доходный район Дубая» и любой рейтинг районов: смысл только в процентах.
- «Апартаменты против вилл» по доходности (6.66 / 5.06 / 4.45): то же.
- «Prime в плюсе год к году, но прогноз Savills −10%»: держится только на двух процентах.
- Пост-разбор таблицы карты целиком: это сама карта, в IG её показать нельзя. Только тизер к ней (темы 1–5).

### 6.3. Открытые вопросы к тебе

1. 🔴 **Где живёт контент покупателя:** вариант A / B / C / D из раздела 0. До ответа даты в разделе 4 — проект.
2. 🔴 **Слово «yield» в IG.** §5a держит `yields` в NEVER, `nemax-brand-stopwords` разрешает чужую цифру с источником. Можно ли название «The Dubai Yield Map» на CTA-слайде и в капшене?
3. 🔴 **AED-перевод чужой доходности** («AED 37,500 a year on an AED 1.5m flat», тема 2): это процент в дирхамах. Разрешаешь на слайде или только механизм?
4. 🔴 **Таблица карты: вариант A или B** (REF §5 вопрос 1), подпись «registered data» (вопрос 4), судьба колонки «Aug read» (вопрос 2). Темы 2 и 3 стоят на варианте A; при B тема 3 умирает.
5. 🔴 **Обеспечение.** Карта v3 и плейбук Маши v4: «we use the property you are buying as security». Плейбук v2 и таблица болей в `FUNNEL_BUYER.md` §2: нужен объект в ОАЭ под залог. Подтвердить у Макса. Блокирует темы 20, 21 и R6, и седьмую причину самой карты.
6. 🔴 **UTM-кампания.** Предлагаю `ig-buyer-q4` для ленты. В `UTM_REGISTRY.md` строка 13.10 стоит с `yield-map-q4` / `cta-discuss-deal`, в карте v3 кнопка `yield-map-buyer-q4` / `cta-discuss-purchase`. Две разные метки на одну кнопку.
7. 🔴 **Живые `EXIT` и `BRIDGE`** отдают ссылку с `utm_campaign=partner-teasers`. Под покупателя заводить отдельные слова или принять смешение?
8. 🔴 **Новые слова:** `FEES`, `ABROAD`, `VALUE`, `FINAL` (пары живые), `MAP` (после `/yield-map`), `CHECK` (после Purchase Check). Заводить с `enabled:false`?
9. 🔴 **Аудитория:** покупатель-инвестор = `borrower:individual`, а не «investors» (вне ленты по §0 скилла)?
10. 🔴 **Индекс аренды при продлении** (темы 9, R5): первоисточник в ресёче 13.10 не открыт. Нужен проход до поста.
11. 🔴 **Лицо в рилсах:** Макс готов к 6 роликам по 90 с? Без лица выигрыш рилса над каруселью пропадает.
12. **Суббота против ПН/СР.** Тирдаун держит субботу лучшей, у тебя каданс ПН + СР. Вариант A это использует, но решать тебе.
13. **Purchase Check** пока черновик: тема 16 и слово `CHECK` ждут страницу.
14. **Перекрытие P3.** Темы 10–15 пересекаются с уже вышедшими постами (`you-asked-cash-to-buy`, `teaser4-valuation-gap` от 08.10, `off-plan-handover`, `reason2-sell-before-buy` от 09.10). В план взяты только 10 и 12, с новым углом «план на аренду ломается деньгами». Темы 11 и 13 я бы не ставила раньше декабря, но это твоё решение.

---

## 7. Что я не делала

- Не открывала Notion (календарь, UTM-реестр) и Figma: по заданию трогать было нельзя. Поэтому занятость ПН/СР после 19.10 — **по памяти, не сверена**.
- Не писала готовые `post.json` / `stories.json` и полные капшены: это шаг `/nemax-content` по каждой теме, после твоих ответов на вопросы 1–5.
- Не заводила слова в `comment_autoreply.json` и строки в `UTM_REGISTRY.md`.
- Не прогоняла `antiai_gate` / `plain_gate.py` / `post_lint.py` по хукам: гейты считают слайды и капшен целиком, хуки отдельно не проверяются.
