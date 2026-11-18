# lekalo-java

Определяет Maven и Gradle по именам манифестов. Каталог с settings.gradle или settings.gradle.kts становится корнем Gradle workspace. Сервис передаёт наблюдения в `lekalo init --adopt`. Для выполнения нужен Node.js.

```yaml
schema: lekalo/runtime-config/v1
components: {}
services:
  discovery/java: gh/ichinya/lekalo-java
```

Выполните `lekalo runtime lock`, затем `lekalo init --adopt --dry-run`. Также можно установить `bin/discovery.cjs` как исполняемый файл и выбрать его через `command`. Пакет предоставляет операции `discovery.describe` и `discovery.inspect`. Проверки контрактов исходного кода потребуют отдельной реализации `check`.
