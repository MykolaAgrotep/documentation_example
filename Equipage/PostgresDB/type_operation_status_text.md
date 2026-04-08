
## Purpose
Хранит локализованные значения статусов.

---

## Columns

| Name             | Type         | Constraints | Description                 |
| ---------------- | ------------ | ----------- | --------------------------- |
| id               | BIGINT       | PK          | ID                          |
| language_code_id | INTEGER      | FK          | → [[language_codes]]        |
| references_to_id | INTEGER      | FK          | → [[type_operation_status]] |
| text_value       | VARCHAR(100) | NOT NULL    | Перевод статуса             |

---

## Relationships

- Many-to-One → [[language_codes]]
- Many-to-One → [[type_operation_status]]

---

## Notes

- Реализация i18n через таблицу
- Перевод статусов на несколько языков через бд