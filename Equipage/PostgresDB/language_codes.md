
## Purpose
Справочник языков для мультиязычных текстов.

---

## Columns

| Name          | Type        | Constraints | Description          |
|--------------|------------|------------|----------------------|
| id           | INTEGER    | PK         | ID языка             |
| language_code| VARCHAR(5) | NOT NULL   | Код языка (UA, EN)   |

---

## Relationships

- Используется в [[type_operation_status_text]]

---

## Seed Data

- UA
- EN

---

## Notes

- Маленький справочник (enum-like таблица)