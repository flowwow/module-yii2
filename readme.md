# Codeception Module Yii2

A Codeception module for Yii2 framework

[![Actions Status](https://github.com/Codeception/module-yii2/workflows/CI/badge.svg)](https://github.com/Codeception/module-yii2/actions)
[![Latest Stable Version](https://poser.pugx.org/codeception/module-yii2/v/stable)](https://github.com/Codeception/module-yii2/releases)
[![Total Downloads](https://poser.pugx.org/codeception/module-yii2/downloads)](https://packagist.org/packages/codeception/module-yii2)
[![License](https://poser.pugx.org/codeception/module-yii2/license)](/LICENSE)

## Installation

```
composer require "codeception/module-yii2" --dev
```

## Documentation

- [Getting started](https://codeception.com/for/yii)
- [Module documentation](https://codeception.com/docs/modules/Yii2)
- [Changelog](https://github.com/Codeception/module-yii2/releases)

### Сборка мусора

Параметр `gcMemoryThresholdMb` задаёт абсолютный порог памяти для принудительной
сборки мусора. По умолчанию используется **2048 МиБ (2 ГиБ)**;
1 МиБ равен 1024 × 1024 байт.

Пример настройки в `functional.suite.yml`:

```yaml
modules:
    enabled:
        - Yii2:
            configFile: 'path/to/config.php'
            gcMemoryThresholdMb: 2048
```

При сбросе приложения модуль проверяет `memory_get_usage(true)` — объём памяти,
зарезервированной менеджером PHP, включая неиспользуемые страницы. Если значение
достигло порога или превысило его, вызывается `gc_collect_cycles()`.
Автоматическая сборка мусора PHP продолжает работать независимо от этой проверки.
## License

`Codeception Module Yii2` is open-sourced software licensed under the [MIT](/LICENSE) License.

© Codeception PHP Testing Framework
