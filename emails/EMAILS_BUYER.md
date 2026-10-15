# Письма прогрева для покупателя

Собрано 14.10.2026 по образцу брокерской цепочки (`DEAL_RESCUE_PLAYBOOK_v3_copy.md`, раздел «Письма прогрева»).

**Кому:** скачал карту и ответил «Just researching», или не ответил на вопрос.
**Кому НЕ цепочка:** «Yes, this month» и «Yes, within 3 months». Им сразу личный контакт:
звонок или WhatsApp в течение 48 часов.

Отправитель «NEMAX team», не личное имя. Тон спокойный, без продажи. В письмах «we» допустимо:
это не пост в ленте. Ни одного процента доходности в письмах: цифры только в карте, с источником.
Метка ссылок: `utm_source=email&utm_medium=email&utm_campaign=yield-map-buyer-q4&utm_content=<письмо>`.

| День | Канал | О чём | utm_content |
|---|---|---|---|
| 0 | email | карта ещё раз + один вопрос | e0-map |
| 2 | WhatsApp | короткий вопрос, если дал телефон | wa2 |
| 3 | email | цифра в объявлении и цифра в договоре | e3-listing |
| 7 | email | сборы в день сделки | e7-fees |
| 14 | email | банк оценил ниже цены | e14-valuation |
| 21 | звонок | разбор, а не продажа | — |
| 30 | email | Purchase Check | e30-check |
| 45 | email | нерезидент: сколько своих денег нужно | e45-nonresident |
| 60+ | email, раз в квартал | обновлённая карта | q-update |

---

## Email 1, день 0

**Subject:** Your Dubai Yield Map

Hi {{FirstName}},

Here is your Dubai Yield Map again, in case the first link got buried: {{MapLink}}

One quick question. Are you buying a property right now? If the money for it depends on another sale, a transfer from abroad or the bank's valuation, reply with a couple of lines. We will come back in writing within 48 hours.

If not, keep the map. Page 03 is worth opening before you look at the next listing.

NEMAX team

## WhatsApp, день 2

Hi {{FirstName}}, this is the NEMAX team. You downloaded our Dubai Yield Map. If you are buying now and the money for it is not ready by the payment date, reply CHECK and we will look at it. If not, no need to reply.

## Email 2, день 3

**Subject:** The number in the listing

Hi {{FirstName}},

Most property portals calculate yield from asking prices and asking rents. Registered data often shows a lower figure for the same community.

On an AED 1.5 million apartment, that gap can be more than AED 20,000 of rent a year. Page 04 of the map shows one community where this happens, and how to check which number you were given.

Before you plan your income, ask the agent one question: where does this yield figure come from?

NEMAX team

## Email 3, день 7

**Subject:** The cash you need on transfer day

Hi {{FirstName}},

Since 1 February 2025, UAE banks have been told not to include the DLD transfer fee and the agency fee in the mortgage. Both are paid in cash on the day of transfer, together with your own share of the price.

If part of your money is in another property or in an account abroad, check the dates now, not in the last week.

When the money is not ready in time, NEMAX can co-finance the purchase. The smallest amount of capital is AED 1 million, and the property you are buying is used as security.

NEMAX team

## Email 4, день 14

**Subject:** When the bank values the property lower

Hi {{FirstName}},

The bank lends on the lower of the agreed price and its own valuation. If the valuation comes in below the price, you need to cover the difference in cash.

Ask the agent whether a bank valuation has been done recently in the same building. If it has not, plan for a gap before you sign.

If you already own a property in the UAE, there may be another way to cover that gap. Reply and tell us about your purchase.

NEMAX team

## Звонок, день 21

Не продажа, а разбор. Первая фраза:

> Hi {{FirstName}}, this is {{Name}} from NEMAX. You downloaded our Dubai Yield Map a few weeks ago. I'm not calling to sell you anything. If you are buying in Dubai, we can look at whether your money is ready for the payment dates. It takes fifteen minutes. Is there a purchase on your table right now?

Если «нет»: «No problem. If one comes up, reply to any of our emails and we will look at it within 48 hours.»

## Email 5, день 30

**Subject:** Is your purchase still on?

Hi {{FirstName}},

If you are still looking at a purchase in Dubai, the 2-Minute Purchase Check takes eight questions. It shows whether your money is ready for the payment dates: {{CheckLink}}

When you are ready to apply: apply.nemax-finance.com

NEMAX team

## Email 6, день 45

**Subject:** Buying from abroad

Hi {{FirstName}},

If you do not live in the UAE, banks often ask for a larger share of your own money than a resident would pay. It is bank policy, not a Central Bank rule, so it differs from bank to bank.

Check the offer from at least two banks before you sign. If the gap is still too large, NEMAX looks at the property, not at your residency.

NEMAX team

## Раз в квартал, день 60+

**Subject:** The Dubai Yield Map, updated

Hi {{FirstName}},

We have updated the Dubai Yield Map with the latest published figures. Some numbers have moved, and the dates are on every page: {{MapLink}}

NEMAX team

---

## 🔴 Что проверить до отправки

- `{{MapLink}}`: PDF карты ещё не залит в Webflow Assets, страница `/thank-you/yield-map` 404.
- `{{CheckLink}}`: Purchase Check собран черновиком (`PURCHASE_CHECK_v1.pdf`), на сайт не залит.
- С какого адреса уходят письма: Brevo на бесплатном тарифе не даёт автоматизаций, домен отправителя ждёт DKIM.
- «around AED 20,000»: это Dubai Silicon Oasis, 1,54 п.п. × AED 1,5 млн = AED 23,100. Расчёт наш, иллюстративный.
- Email 6, «banks often ask for a larger share»: по проверенному ресёчу 28.06 нерезиденту банки обычно дают 50–60%. Это политика банков, не норма ЦБ, поэтому формулировка без цифры.
- Email 3, «the property you are buying is used as security»: это формулировка Маши, она до сих пор не подтверждена у Макса. Подтвердить до отправки.
