# Руководство OpenAPI Шаг 3: Объект `servers`

| [*Шаг 1: объект* `openapi`](step1-openapi-object.md) | --> | [*Шаг 2: объект* `info`](step2-info-object.md) | --> | [**Шаг 3: объект** `servers`](step3-servers-object.md) | --> | [*Шаг 4: объект* `paths`](step4-paths-object.md) | --> | [*Шаг 5: объект* `components`](step5-components-object.md) | --> | [*Шаг 6: объект* `security`](step6-security-object.md) | --> | [*Шаг 7: объект* `tags`](step7-tags-object.md) | --> | [*Шаг 8: объект* `externalDocs`](step8-externalDocs-object.md) |

В объекте `servers` указывается базовый путь, используемый в ваших запросах API. Базовый путь - это часть URL, которая находится перед конечной точкой.

[Пример объекта `servers`](#sample)

[Опции URL сервера](#options)

[Отображение в Swagger UI](#appearance)

<a name="sample"></a>
## Пример объекта `servers`

Пример объекта `servers`

```
servers:
- url: https://api.openweathermap.org/data/2.5/
```

Каждая из конечных точек (называемых в спецификации `paths`) будет добавляться ​​к URL-адресу сервера, при отправке пользователями пробных запросов `Try it out`. Например, если одним из путей является` /weather`, то при отправке запроса Swagger UI представит путь к `{server URL}{path}` или [https://api.openweathermap.org/data/2.5/weather](https://api.openweathermap.org/data/2.5/weather).
<a name="options"></a>
## Опции URL сервера

Объект `servers` обладает гибкой настройкой. Можно указать несколько URL-адресов серверов, которые могут относиться к различным средам (тестовая, бета-версия, рабочая версия). При наличии нескольких URL-адресов серверов, пользователи могут выбирать среду в раскрывающемся списке серверов. Можно указать несколько URL-адресов серверов, например:

```
servers:
  - url: https://api.openweathermap.org/data/2.5/
        description: Production server
  - url: http://beta.api.openweathermap.org/data/2.5/
        description: Beta server
  - url: http://some-other.api.openweathermap.org/data/2.5/
        description: Some other server
```

В Swagger UI выбор из нескольких серверов осуществляется при помощи выпадающего списка

![multiservers](img/7.png)

Если указан один сервер все равно будет отображаться выпадающий список, но с одним вариантом.

В URL-адрес сервера также можно включать переменные, которые будут заполняться сервером во время выполнения. Кроме того, если для разных путей (конечных точек) требуются разные URL-адреса сервера, можно добавить объект `servers` в качестве свойства в объекте операции объекта `path`. URL-адрес локально объявленных серверов переопределяет URL-адрес глобальных серверов.

См. [Overriding Servers](https://swagger.io/docs/specification/api-host-and-base-path/) в разделе «Сервер API и базовый URL» (документы Swagger) для получения дополнительной информации.

<a name="appearance"></a>
## 👨‍💻 Отображение в Swagger UI

Вставим объект `servers` (первый пример кода выше, показывающий только один URL) в редактор Swagger, добавив к имеющемуся коду. Swagger UI будет выглядеть следующим образом:

![servers](img/8.png)


[🔙](step2-info-object.md)

[Go next ➡](step4-paths-object.md)
