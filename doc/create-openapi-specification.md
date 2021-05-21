# Практическое занятие: Создание спецификации OpenAPI

В [руководстве по OpenAPI](openapi-tutorial-overview.md) мы прошли 8 этапов создания документа в спецификации OpenAPI. Теперь стоит попрактиковаться сначала в редактировании, а затем и в создании документа спецификации OpenAPI.

#### Содержание раздела

[Практическое занятие: редакция существующего документа в спецификации OpenAPI](#edit)

[Создание документа в спецификации OpenAPI для выбранного API](#create)

<a name="edit"></a>
## 👨‍💻 Практическое занятие: редакция существующего документа в спецификации OpenAPI

Используем простой [API Sunrise and sunset times](https://sunrise-sunset.org/api), чтобы лучше ознакомиться с процессом редактирования файла спецификации OpenAPI. [API Sunrise and sunset times](https://sunrise-sunset.org/api) не требует аутентификации с запросами, поэтому здесь отсутствуют сложные рабочие процессы аутентификации (можно пропустить [объект `security`](step6-security-object.md)). В этом упражнении мы отредактируем некоторые из существующих значений в уже написанном документе спецификации OpenAPI.

Для редактирования спецификации OpenAPI:

1. Копируем код из [предварительно созданной спецификации OpenAPI](https://idratherbewriting.com/learnapidoc/assets/files/swagger-sunrise-sunset/openapi_sunrise_sunset.yml)

2. Вставляем содержимое YAML в [редактор Swagger](https://editor.swagger.io/).

3. Определяем каждый из объектов корневого уровня спецификации OpenAPI:

- [Шаг 1: Объект `openapi`](step1-openapi-object.md)
- [Шаг 2: Объект `info`](step2-info-object.md)
- [Шаг 3: Объект `servers`](step3-servers-object.md)
- [Шаг 4: объект `paths`](step4-paths-object.md)
- [Шаг 5: Объект `components`](step5-components-object.md)
- [Шаг 6: Объект `security`](step6-security-object.md)
- [Шаг 7: Объект `tags`](step7-tags-object.md)
- [Шаг 8: Объект `externalDocs`](step8-externalDocs-object.md)

4. В объекте `info`(в верхней части) внесите изменения в свойство `description` и посмотрите, как обновляется визуальный дисплей в правом столбце.
5. В объекте `parameters` внесите изменения в одно из свойств описания и посмотрите, как обновляется визуальный редактор.
6. Найдите указатель `$ref` в объекте `response`. Определите, на что он указывает в `components`.
7. Измените несколько интервалов таким образом, чтобы сделать спецификацию недействительной (например, вставить пробел перед информацией), и посмотрите на появившуюся ошибку. Затем верните неверный пробел.
8. Разверните раздел **Get** и нажмите `Try it out`. Затем нажмите `Execute` и посмотрите ответ.



<a name="create"></a>
## 👨‍💻 Создание документа в спецификации OpenAPI для выбранного API

[На практике 3 модуля мы искали опен-сорс проект API](../documenting-api-endpoints/find-open-source-project.md), которому нужна была документация. Сейчас попробуем создать спецификацию OpenAPI для этого API. В зависимости от API, с которым мы решили работать, можно будет использовать этот документ как часть своего портфолио.

Если этот опен-сорс проект не имеет API или API уже имеет спецификацию OpenAPI, можно найти другой API (возможно, из этого [списка из 100+ API](../Publishing-doc/API-doc-sites-list.md)) и создать спецификацию OpenAPI.

При создании спецификации пройдем по каждому шагу руководства по спецификации OpenAPI, чтобы создать документацию API:

- [Шаг 1: Объект `openapi`](step1-openapi-object.md)
- [Шаг 2: Объект `info`](step2-info-object.md)
- [Шаг 3: Объект `servers`](step3-servers-object.md)
- [Шаг 4: объект `paths`](step4-paths-object.md)
- [Шаг 5: Объект `components`](step5-components-object.md)
- [Шаг 6: Объект `security`](step6-security-object.md)
- [Шаг 7: Объект `tags`](step7-tags-object.md)
- [Шаг 8: Объект `externalDocs`](step8-externalDocs-object.md)

После создания проверяем нашу документацию в [редакторе Swagger](https://swagger.io/tools/swagger-editor/). Выполним запрос, чтобы убедиться, что все работает верно.


[🔙](step8-externalDocs-object.md)

[Go next ➡](swagger-ui-tutorial.md)
