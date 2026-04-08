
## Purpose
Колонны (логическое объединение).

---

## Columns

| Name             | Type      | Constraints            | Description     |
| ---------------- | --------- | ---------------------- | --------------- |
| id               | BIGINT    | PK                     | ID              |
| name             | VARCHAR   |                        | Название        |
| color_hex        | VARCHAR   |                        | Цвет            |
| is_terminated    | BOOLEAN   | NOT NULL DEFAULT FALSE | Завершена       |
| termination_date | TIMESTAMP |                        | Дата завершения |
| date_add         | TIMESTAMP | NOT NULL               | Создана         |
| date_update      | TIMESTAMP | NOT NULL               | Обновлена       |

---

## Relationships

- Many-to-Many → [[equipages]] через [[crew_equipage_to_equipage]]