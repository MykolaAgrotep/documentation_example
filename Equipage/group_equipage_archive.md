
## Purpose
Архив колонны.

---

## Columns

| Name      | Type    | Constraints | Description          |
|-----------|--------|------------|----------------------|
| id        | BIGINT | PK         | ID                   |
| name      | VARCHAR|            | Название             |
| color_hex | VARCHAR|            | Цвет                 |
| equipage  | BIGINT | NOT NULL   | ID экипажа           |

---

## Notes

- Используется для хранения истории/архива
- Нет внешних ключей → возможна денормализация
- НЕ понятно что он вообще делает в бд, лучше удалить.