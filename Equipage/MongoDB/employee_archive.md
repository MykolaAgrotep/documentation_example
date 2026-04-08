
## Purpose
Хранит данные сотрудника в момент архивирования экипажа.

---
## Fields

| Name       | Type   | Description   |
| ---------- | ------ | ------------- |
| employeeId | Long   | ID сотрудника |
| firstname  | String | Имя           |
| middleName | String | Отчество      |
| lastname   | String | Фамилия       |

---
## Notes

- Денормализованные данные (без связей)
- Используются только внутри [[equipage_archive]]