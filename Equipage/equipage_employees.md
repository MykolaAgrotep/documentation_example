
## Purpose
Связь экипажа с сотрудниками.

---

## Columns

| Name         | Type    | Constraints | Description          |
|--------------|--------|------------|----------------------|
| id           | BIGINT | PK         | ID                   |
| equipage_id  | BIGINT | FK         | → [[equipages]]      |
| employee_id  | BIGINT | NOT NULL   | ID сотрудника        |

---

## Relationships

- Many-to-One → [[equipages]]
