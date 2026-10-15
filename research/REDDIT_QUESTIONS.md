# Вопросы покупателей с Reddit для Dubai Yield Map

Собрано 15.10.2026 скриптом проекта `reddit_research.py` (RSS, без API). Запросы: rental yield, ROI apartment,
net yield service charge, buy to let, worth buying apartment to rent, service charges rent, rent increase renewal,
transfer fee cash, JVC investment, listing price vs actual. Сабреддиты: r/DubaiRealEstate, r/dubai, r/UAE, r/abudhabi.
Окно: год. Найдено 1 093 поста, из них 612 вопросов, 14 тредов открыты целиком.

**Как отбирали.** Вопрос должен совпадать и с темой карты, и с тем, где NEMAX может помочь.
Не брали вопросы «где дешевле» и «банк или недвижимость», а также жалобы арендаторов и объявления агентов.
Reddit — источник вопроса, а не ответа: цифры из тредов в карту не идут, ников и ссылок в карте нет.

## В карте, стр. 11 «What buyers ask»

| # | Вопрос в карте | Откуда | Дата |
|---|---|---|---|
| 1 | Which area in Dubai gives the highest rental yield? | [r/DubaiRealEstate](https://www.reddit.com/r/dubairealestate/comments/1x43m0w/which_area_in_dubai_gives_high_rental_yield/) | 12.10.2026 |
| 2 | What is a realistic yield after costs? | [r/DubaiRealEstate](https://www.reddit.com/r/dubairealestate/comments/1vw0mup/help_trying_to_rank_dubai_sale_listings_by_net/) | 23.08.2026 |
| 3 | A listing shows a high gross ROI. What should I ask first? | [r/DubaiRealEstate](https://www.reddit.com/r/dubairealestate/comments/1x6605u/investors_opportunity_binghatti_luna_jvc_841/): объявление с «gross ROI», первый ответ под ним — «what are the service charges?» | 14.10.2026 |
| 4 | Can I raise the rent when my tenant renews? | [r/DubaiRealEstate](https://www.reddit.com/r/dubairealestate/comments/1x4qvze/renewing_a_tenant_this_winter_the_date_that/) и ещё больше десятка тредов про индекс аренды | 13.10.2026 |
| 5 | Why do I need more cash than the deposit? | [r/DubaiRealEstate](https://www.reddit.com/r/dubairealestate/comments/1x1efn9/why_does_nobody_tell_firsttime_buyers_in_dubai/) | 09.10.2026 |
| 6 | I already own a property. Can I use it to buy another one to let? | [r/DubaiRealEstate](https://www.reddit.com/r/dubairealestate/comments/1w72xtm/i_own_my_property_when_is_the_time_to_buy_another/) | 04.09.2026 |

## В теле причин

- Причина 01: «Buyers often ask which area gives the highest yield.» (вопрос 1)
- Причина 03: «A common question is what the yield is after costs.» (вопрос 2)

## Что ещё часто спрашивают (в карту не вошло)

- «Is 6.25% in the bank better than a 6% property yield?» — сравнение с вкладом, не наш продукт.
- «Would your first-year net rental income cover the purchase costs?» — ответ требует цифр, которых нет в первоисточниках карты.
- «Can I use projected rental income to qualify for the mortgage?» — вопрос про правила банка, нужен отдельный ресёч.
- Десятки вопросов арендаторов про рост аренды при продлении — голос арендатора, не покупателя.

✅ Ответ на вопрос 4 проверен 15.10.2026 по первоисточнику: Dubai Decree No. 43 of 2013, Art. 1 (максимальный рост аренды при продлении) и Art. 3 (средняя аренда по Rent Index RERA). Текст: портал законодательства Дубая dlp.dubai.gov.ae и PDF DLD, копии в `04_RESEARCH:/market_reports/rent-index-decree43-sources/`.
