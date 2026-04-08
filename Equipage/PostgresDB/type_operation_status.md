## Purpose  
Справочник типов статусов операций (без локализации).  
  
---  
  
## Columns  
  
| Name      | Type         | Constraints | Description        |     |
| --------- | ------------ | ----------- | ------------------ | --- |
| id        | BIGINT       | PK          | ID статуса         |     |
| text_code | VARCHAR(100) | NOT NULL    | Код статуса (ENUM) |     |
  
---  
  
## Relationships  
  
- One-to-Many → [[type_operation_status_text]]  
- One-to-Many → [[operation_status]]  
  
---  
  
## Example Values  
  
- CREATED  
- WAITING  
- ON_THE_WAY  
  
---  
  
## Notes  
  
- Используется как enum через БД