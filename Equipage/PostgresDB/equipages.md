
## Purpose
Основная таблица экипажей, хранит информацию об экипаже (группе сотрудников и транспорта), привязанной к компании. Используется для управления составом экипажа и его статусом.

---

## Columns

| Name             | Type      | Constraints              | Description              |
|------------------|----------|--------------------------|--------------------------|
| id               | BIGINT   | PK                       | ID экипажа               |
| company_id       | BIGINT   | NOT NULL                 | Компания                 |
| is_blocked       | BOOLEAN  | NOT NULL DEFAULT FALSE   | Заблокирован ли экипаж   |
| is_terminated    | BOOLEAN  | NOT NULL DEFAULT FALSE   | Завершён                 |
| termination_date | TIMESTAMP|                          | Дата завершения          |
| date_add         | TIMESTAMP| NOT NULL                 | Дата создания            |
| date_update      | TIMESTAMP| NOT NULL                 | Дата обновления          |

---

## Relationships

- One-to-Many → [[equipage_employees]]
- One-to-Many → [[equipage_transports]]
- One-to-Many → [[operation_status]]
- Many-to-Many → [[group_equipages]] (через [[crew_equipage_to_equipage]])

---
## Business Rules

- Экипаж может быть:
  - активным
  - заблокированным
  - завершённым

---

### is_blocked

- `true` → экипаж **закреплён за каденцией**
- Такой экипаж:
  - ❌ нельзя удалить
  - ❌ нельзя изменять
- Используется для защиты данных, участвующих в каденции

---

### is_terminated

- `true` → экипаж считается **удалённым (soft delete)**

- При удалении:
  - создаётся снапшот в MongoDB ([[equipage_archive]]])
  - сохраняются:
    - компания
    - транспорт
    - сотрудники
    - статусы

