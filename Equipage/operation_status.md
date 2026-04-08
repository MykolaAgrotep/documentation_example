
## Purpose
История оперативных статусов экипажа.

---

## Columns

| Name         | Type      | Constraints              | Description                |
|--------------|----------|--------------------------|----------------------------|
| id           | BIGINT   | PK                       | ID                         |
| equipage_id  | BIGINT   | FK                       | → [[equipages]]            |
| status_id    | BIGINT   | FK NOT NULL              | → [[type_operation_status]]|
| status_date  | TIMESTAMP|                          | Дата статуса               |
| is_terminated| BOOLEAN  | NOT NULL DEFAULT FALSE   | Завершён                   |
| date_add     | TIMESTAMP| NOT NULL                 | Создан                     |
| date_update  | TIMESTAMP| NOT NULL                 | Обновлён                   |

---

## Relationships

- Many-to-One → [[equipages]]
- Many-to-One → [[type_operation_status]]
