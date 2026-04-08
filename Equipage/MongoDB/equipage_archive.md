
## Purpose
Хранит **снапшот экипажа** в момент удаления или архивирования.

---

## Fields

| Name              | Type                          | Description                          |
|------------------|-------------------------------|--------------------------------------|
| id               | String                        | MongoDB ID                           |
| equipageId       | Long                          | ID экипажа (из PostgreSQL)           |
| company          | CompanyDto                    | Данные компании                      |
| transportArchives| List<[[transport_archive]]>   | Архив транспорта                     |
| employeeArchives | List<[[employee_archive]]>    | Архив сотрудников                    |
| statusArchives   | List<[[operation_status_archive]]> | Архив статусов               |
| archiveReason    | ArchiveReason                 | Причина архивирования                |

---

## Notes

- Полный snapshot состояния экипажа
- Используется при `is_terminated = true`
- Источник истины после удаления из основной БД