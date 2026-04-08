
## Purpose
Хранит историю оперативных статусов экипажа на момент архивирования.

---

## Fields

| Name       | Type          | Description              |
|------------|--------------|--------------------------|
| id         | Long         | ID статуса               |
| typeStatus | String       | Тип статуса              |
| statusDate | LocalDateTime| Дата статуса             |
| dateAdd    | LocalDateTime| Дата создания            |

---

## Notes

- Используется для восстановления timeline