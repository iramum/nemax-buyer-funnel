# Как пишет Маша: разбор плейбука «7 Reasons Property Deals Fall Through»

Собрано 15.10.2026. Источник: текст плейбука v4 (05.10.2026), прочитан целиком.
По этим правилам написаны обе редакции Dubai Yield Map. Здесь они собраны, чтобы текст можно было
проверить по пунктам.

## 1. Читатель и голос

| Правило | Как у Маши | Пример из плейбука |
|---|---|---|
| Говорит с одним человеком | «you», «your buyer», «your client» | «Your buyer agrees on a price and plans to use bank financing…» |
| Начинает с его ситуации, а не с NEMAX | первая фраза каждой причины — что происходит с покупателем | «The buyer's other property has not sold.» |
| Спокойный тон, без продажи | нет восклицаний, нет «best», «fast», «unique» | «If they cannot pay, handover may be delayed.» |
| Осторожные глаголы | may, could, depending on | «…could face cancellation of the purchase… depending on the contract» |
| Честно, когда NEMAX не помогает | в причинах 4 и 7 хода NEMAX нет вообще | «they may need to consider a property that fits their total budget» |

## 2. Схема каждой причины

1. **Заголовок** — ситуация одной фразой: «The buyer is not ready for the handover payment».
2. **Абзац 1** — что происходит (2–3 короткие фразы).
3. **Абзац 2** — чем это грозит сделке.
4. **What to check** — повелительное наклонение: Check / Ask / Confirm.
5. **How the deal may be saved** — сначала обычные выходы, NEMAX последним и только если подходит.

## 3. Фраза

- 10–15 слов, одна мысль. Нет вставок в скобках и цепочек через запятую.
- Простые глаголы: pay, sell, wait, need, arrive, check.
- Термин с объяснением при первом упоминании: «No Objection Certificate (NOC)».
- Ни одного тире-разделителя внутри фразы, кроме подзаголовка обложки.
- Ни одной цифры без нужды: в плейбуке Маши почти нет чисел. В карте цифры есть, потому что карта о цифрах, но у каждой источник и дата.

## 4. Чем карта v2 (04.09) отличалась и что исправлено

| Карта v2 | Как стало (по Маше) |
|---|---|
| «Nobody is lying. They are counting different things.» — афоризм | «Four well-known sources publish yields for Dubai. They measure at different points of a deal, so their numbers rarely match.» |
| Фразы по 25–35 слов | средняя 13 слов, ни одной длиннее 30 |
| Читатель — абстрактный «a buyer» | «you» (покупатель) или «your buyer» (брокер) |
| Эссе по темам | семь причин по одной схеме |
| NEMAX на последней странице абзацем про SPV | NEMAX в причине 7 и в финале, словами Маши |

## 5. Проверка B2 (машинная)

`plain_gate.py` (стандарт B2 проекта с 12.10.2026): средняя фраза ≤ 16 слов, фраз > 25 слов ≤ 10%, > 30 слов ноль,
grade ≤ 9. Обе редакции проходят (цифры в README репо).
