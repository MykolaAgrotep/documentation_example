## Description
Базовая сущность для хранения локализованного текста.

## Fields

| Field        | Type          | Description          |
|--------------|--------------|----------------------|
| id           | Long         | Идентификатор        |
| languageCode | LanguageCode | Язык                 |
| referencesTo | T            | Связанная сущность   |
| textValue    | String       | Текст                |