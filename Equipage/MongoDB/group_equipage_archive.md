# group_equipage_archive

## Purpose
Хранит **снапшот группы экипажей** вместе с вложенными экипажами.

Используется для:
- архивирования групп
- восстановления структуры группы
- аудита изменений

---

## Fields

| Name              | Type                        | Description                          |
|------------------|-----------------------------|--------------------------------------|
| id               | String                      | MongoDB ID                           |
| groupId          | Long                        | ID группы (из PostgreSQL)            |
| groupName        | String                      | Название группы                      |
| colorHex         | String                      | Цвет группы                          |
| equipageArchives | List<[[equipage_archive]]>  | Список архивов экипажей              |
| archiveReason    | ArchiveReason               | Причина архивирования                |

---

## Relationships

- Embeds → [[equipage_archive]]

---

## Business Meaning

- НА ДАННЫЙ МОМЕНТ НЕ РАБОТАЕТ ТАК КАК НЕЛЬЗЯ УДАЛИТЬ КОЛОННУ С ЭКИПАЖЕМ ВНУТРИ
- При удалении или архивировании группы:
  - сохраняется сама группа
  - сохраняются все связанные экипажи (snapshot)
- Формируется **иерархический архив**:
  - Group
    - Equipages
      - Employees / Transports / Statuses


