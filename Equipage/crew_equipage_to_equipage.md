
## Purpose
Связующая таблица между колоннами и экипажами.

---

## Columns

| Name               | Type   | Constraints | Description           |
| ------------------ | ------ | ----------- | --------------------- |
| id                 | BIGINT | PK          | ID                    |
| group_equipages_id | BIGINT | FK          | → [[group_equipages]] |
| equipage_id        | BIGINT | FK          | → [[equipages]]       |

---

## Relationships

- Many-to-One → [[group_equipages]]
- Many-to-One → [[equipages]]