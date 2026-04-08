## Description
Основная сущность контракта.

## Fields

| Field                  | Type                     | Description                  |
|------------------------|--------------------------|------------------------------|
| id                     | Long                     | Идентификатор                |
| companyId              | Integer                  | ID компании                  |
| contractNumber         | String                   | Номер контракта              |
| conclusionDate         | LocalDateTime            | Дата заключения              |
| endDate                | LocalDateTime            | Дата окончания               |
| includingExtensionDate | LocalDateTime            | Дата с учетом продления      |
| contractLocalName      | String                   | Локальное название           |
| individual             | Boolean                  | Индивидуальный               |
| customer               | Boolean                  | Является клиентом            |
| permanentExtension     | Boolean                  | Автопродление                |
| accountCompany         | String                   | Компания счета               |
| detailsForManager      | String                   | Комментарии для менеджера    |
| username               | String                   | Пользователь                 |
| changedBy              | String                   | Кто изменил                  |
| typeContract           | TypeContract             | Тип контракта                |
| stateContract          | StateContract            | Статус контракта             |
| tariffGrids            | List\<ContractTariffGrid>| Тарифные сетки               |
| isClosed               | Boolean                  | Закрыт ли контракт           |