
## Purpose
Хранит **историю изменений экипажа** (audit log).

В отличие от [[equipage_archive]]:
- хранит не snapshot, а **события изменений**

---
## Fields

| Name                 | Type                           | Description                |
| -------------------- | ------------------------------ | -------------------------- |
| id                   | String                         | MongoDB ID                 |
| equipageId           | Long                           | ID экипажа                 |
| actionType           | HistoryAction                  | Тип действия               |
| employees            | List<[[EmployeeReceivedDto]]>  | Список сотрудников         |
| transports           | List<[[TransportReceivedDto]]> | Список транспорта          |
| changedEmployeeId    | Long                           | Изменённый сотрудник       |
| changedTransportId   | Long                           | Изменённый транспорт       |
| changedTransportType | [[type_of_transports]]         | Тип изменённого транспорта |
| actionDate           | Instant                        | Дата действия              |

---
## Business Meaning

- Логирует изменения:
  - добавление/удаление сотрудников
  - изменение транспорта
  - изменения состава экипажа

---
## Notes

- Реализация **event-based audit log**
- Можно использовать для:
  - восстановления состояния
  - анализа изменений