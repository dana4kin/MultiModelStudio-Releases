# MultiModelStudio 26.3.1

Патч исправляет ошибку завершения установщика Windows после успешной распаковки и проверки базы данных. Функции MultiModelStudio 26.3.0, включая управляемую функциональную память NMC-A и provider TensorRT-LLM, сохранены без изменений.

## Исправление

- Установщик Windows больше не освобождает межпроцессную блокировку из другого потока после асинхронной проверки кандидата.
- Чистая установка `MMS-v26.3.1-Setup.exe` физически проверена на Windows x64: код завершения 0, версия активирована, отдельная база SQLite создана, установленный интерфейс Avalonia запущен и корректно закрыт.
- Каталог безопасных операций памяти доступен в установленном интерфейсе. Изменяющие и потенциально опасные операции остаются отключёнными до явного разрешения пользователя.

## Файлы

- **Windows x64:** `MMS-v26.3.1-Setup.exe` — рекомендуемый установщик без прав администратора; `MMS-v26.3.1-Windows-x64.zip` — переносимый архив.
- **Linux x64:** `MMS-v26.3.1-Linux-x64-self-contained.tar.gz`.
- **macOS Apple Silicon:** `MMS-v26.3.1-macOS-AppleSilicon-self-contained.tar.gz`.
- **macOS Intel:** `MMS-v26.3.1-macOS-Intel-self-contained.tar.gz`.

.NET включён в каждый пакет. Модели, внешние runtime, MCP-серверы, пользовательские данные, веса моделей и учётные данные в поставку не входят.

## Проверка выпуска

- Ветка исходников: `release/26.3.1`; точный source commit: `d723c59809dbe5b0b8a13196f6b65285ca06d292`.
- Release-сборка: **0 предупреждений, 0 ошибок**.
- Автономные тесты: **2991 PASS, 0 FAIL, 25 ожидаемых opt-in/live SKIP**.
- EF/SQLite runtime gate: **9 PASS, 0 FAIL**.
- Structure, bindings, localization parity и function-catalog gates: **PASS**.
- Windows manifest подписан RSA-PSS/SHA-256. Fingerprint публичного ключа: `0fe634a186142df2443e605490b47a8dfd8af98671ebce4bee7150d10b7b55b3`.
- Windows Setup: **физический PASS** на чистом пути и отдельной базе.
- Linux и macOS проверены структурно и требуют физического запуска на соответствующей ОС.

## SHA-256

| Файл | SHA-256 |
|---|---|
| `MMS-v26.3.1-Setup.exe` | `9de8cc3de6d7a622a911647e8b677765f56c2cca59cda42f393e0a981eef6282` |
| `MMS-v26.3.1-Windows-x64.zip` | `40a6dcfb4156b249233d1ca0503d748c9a645c9a2d2ddb347fb6a6ffb50251b9` |
| `MMS-v26.3.1-Linux-x64-self-contained.tar.gz` | `c30da4b6443ea3f4a4f0934ad46b536476a962c922ea0cdeaa42224b20c5dacb` |
| `MMS-v26.3.1-macOS-AppleSilicon-self-contained.tar.gz` | `9a1e6865e1a92012d7f11208fc85868b51a1ddff35564ddf63969aff0ba5186c` |
| `MMS-v26.3.1-macOS-Intel-self-contained.tar.gz` | `cb44e7f4042dc496519d5b746f396140cedbe9333852bf9578f2088e790dd1c8` |
