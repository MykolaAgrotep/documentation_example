
## Purpose
Связь экипажа с транспортом.

---

## Columns

| Name         | Type    | Constraints | Description                  |
|--------------|--------|------------|------------------------------|
| id           | BIGINT | PK         | ID                           |
| equipage_id  | BIGINT | FK         | → [[equipages]]              |
| transport_id | BIGINT | NOT NULL   | ID транспорта                |
| type_of      | VARCHAR| NOT NULL   | → [[type_of_transports]]     |

