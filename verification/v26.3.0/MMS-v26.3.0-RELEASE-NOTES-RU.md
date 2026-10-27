# MultiModelStudio 26.3.0

Выпуск добавляет управляемую функциональную память NMC-A и отдельный provider TensorRT-LLM,
обновляет справку и сохраняет явные границы безопасности для кандидатов и внешних runtime.

## Новые возможности

- Принятый на Windows/NVIDIA кандидат NMC-A `memory.public-v2-r16` доступен через пять
  read-only операций: `memory_context`, `memory_describe_schema`, `memory_list`,
  `memory_neighbors` и `memory_search`.
- Для NMC-A запрещены изменение памяти, выполнение инструментов, автоматическое продвижение и
  смена маршрута по умолчанию. Кандидат регистрируется и активируется отдельно.
- Добавлен provider TensorRT-LLM с явным описанием возможностей и диагностикой. Для выполнения
  требуется совместимый внешний NVIDIA runtime и модель; они не входят в поставку.
- Обновлены Windows-интерфейс, каталоги локализации и встроенная справка. Каталог интерфейса
  содержит 434 команды и 666 элементов Avalonia/WPF.

## Файлы

- **Windows x64:** `MMS-v26.3.0-Setup.exe` — рекомендуемый установщик без прав
  администратора; `MMS-v26.3.0-Windows-x64.zip` — переносимый архив.
- **Linux x64:** `MMS-v26.3.0-Linux-x64-self-contained.tar.gz`.
- **macOS Apple Silicon:** `MMS-v26.3.0-macOS-AppleSilicon-self-contained.tar.gz`.
- **macOS Intel:** `MMS-v26.3.0-macOS-Intel-self-contained.tar.gz`.

.NET включён в каждый пакет. Модели, внешние runtime, MCP-серверы, пользовательские данные,
веса моделей и учётные данные в поставку не входят.

## Проверка выпуска

- Ветка исходников: `release/26.3.0`; точный source commit:
  `dbb26a6d0211042c60bd768ff2d5507713da32c8`.
- Release-сборка обеих оболочек: **0 предупреждений, 0 ошибок**.
- Автономные тесты: **2991 PASS, 0 FAIL, 25 ожидаемых opt-in/live SKIP**.
- EF/SQLite runtime gate: **9 PASS, 0 FAIL**.
- Structure, product-version, bindings, localization parity и function-catalog gates: **PASS**.
- Архивы повторно прочитаны: self-contained runtime, архитектуры, macOS bundle и Unix
  executable bits подтверждены.
- Windows manifest независимо проверен прямой RSA-PSS/SHA-256 подписью. Fingerprint публичного
  ключа: `0fe634a186142df2443e605490b47a8dfd8af98671ebce4bee7150d10b7b55b3`.
- Linux и macOS проверены структурно и требуют физического запуска на соответствующей ОС.

## SHA-256

| Файл | SHA-256 |
|---|---|
| `MMS-v26.3.0-Setup.exe` | `a2d2249d7ba2f4aac9e66efeca10e9da8f768a938aed0ae073d644bc79b19e69` |
| `MMS-v26.3.0-Windows-x64.zip` | `8363cdc7d60ded634dc21594beeaf01c92adff026ddae7cd3bc0395b1debc60b` |
| `MMS-v26.3.0-Linux-x64-self-contained.tar.gz` | `a7f7355f188b0b0d8acd6a864771f157dffff1df2e06be327afae01d43d92238` |
| `MMS-v26.3.0-macOS-AppleSilicon-self-contained.tar.gz` | `2a71659b8ff53ffb0f4da01da48917d5f50fca07808ace27b692868669cc9f23` |
| `MMS-v26.3.0-macOS-Intel-self-contained.tar.gz` | `8d0c4a27f630c66da5d8ff08d9c1f11d727b934db8b3fac326987af0b7a1a866` |
