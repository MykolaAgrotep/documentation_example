## Description
Тарифная сетка контракта с периодом действия и наборами тарифов.

## Fields

| Field            | Type                              | Description               |
| ---------------- | --------------------------------- | ------------------------- |
| id               | Long                              | Уникальный идентификатор  |
| validFrom        | Instant                           | Дата начала действия      |
| validTo          | Instant                           | Дата окончания действия   |
| active           | Boolean                           | Активна ли запись         |
| contract         | Contract                          | Связанный контракт        |
| priceValue       | BigDecimal                        | Основное значение тарифа  |
| changedBy        | String                            | Кто изменил               |
| priceUnit        | PriceUnit                         | Единица измерения цены    |
| warningCountries | List\<[[ContractWarningCountry]]> | Предупреждения по странам |
| tollRoads        | List\<[[TollRoadTariff]]>         | Тарифы платных дорог      |
| countryStays     | List\<[[CountryStayTariff]]>      | Тарифы за пребывание      |
| otherTariffs     | List\<[[OtherTariff]]>            | Прочие тарифы             |
