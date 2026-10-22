# MultiModelStudio 26.2.1

Исправляющий выпуск устраняет сбой запуска общей Avalonia-оболочки на Windows, Linux и macOS.

## Исправления

- Экран подготовки компьютера больше не обращается к элементам `ExpertPreparation` и
  `PrimaryPreparation` до их появления в визуальном дереве.
- Подписка на события блока подготовки подключается и отключается вместе с экраном, без
  повторных обработчиков.
- Закреплённые байт-в-точность тестовые данные теперь сохраняют LF при Windows checkout.
- Быстрый автономный набор отделён от двух явно opt-in live-тестов и снова завершается без
  скрытых пропусков.

## Файлы

- **Windows x64:** `MMS-v26.2.1-Setup.exe` — рекомендуемый установщик без прав
  администратора; `MMS-v26.2.1-Windows-x64.zip` — переносимый архив.
- **Linux x64:** `MMS-v26.2.1-Linux-x64-self-contained.tar.gz`.
- **macOS Apple Silicon:** `MMS-v26.2.1-macOS-AppleSilicon-self-contained.tar.gz`.
- **macOS Intel:** `MMS-v26.2.1-macOS-Intel-self-contained.tar.gz`.

.NET включён в каждый пакет. Модели, внешние runtime, MCP-серверы, пользовательские данные
и учётные данные в поставку не входят.

## Проверка выпуска

- Точный source commit: `787c5bdbfe0b424fa9343e15598494541ecb85bc`.
- Avalonia Release: **0 предупреждений, 0 ошибок**.
- Запуск Windows-сборки с чистым профилем прошёл прежнюю точку падения: **PASS**.
- Fast: **2963 PASS, 0 FAIL, 0 SKIP**.
- Network: **20 PASS, 0 FAIL, 0 SKIP**.
- Structure и product-version gates: **PASS**.
- Архивы повторно прочитаны: self-contained runtime, архитектуры, macOS bundle и Unix
  executable bits подтверждены.
- Windows manifest подписан RSA-PSS/SHA-256. Fingerprint публичного ключа:
  `0fe634a186142df2443e605490b47a8dfd8af98671ebce4bee7150d10b7b55b3`.
- Linux и macOS проверены структурно и требуют физического запуска на соответствующей ОС.

## SHA-256

| Файл | SHA-256 |
|---|---|
| `MMS-v26.2.1-Setup.exe` | `3a9ba1aa1558558476e1950e1ab188e6b0957d59db4e5bf2b160f13be5430c01` |
| `MMS-v26.2.1-Windows-x64.zip` | `7eaeeb62ff17a2a929d1ba39973caec5ac193951fdc4724f765343ed6818145d` |
| `MMS-v26.2.1-Linux-x64-self-contained.tar.gz` | `ec9032087d67a8352ba0bc5530b2345e59f7a233a4d315305c11bfb7f64c49f6` |
| `MMS-v26.2.1-macOS-AppleSilicon-self-contained.tar.gz` | `1f0e86d4de5d0a19d43ed352d2340825afda15a903809abd131ed1ec168a6f78` |
| `MMS-v26.2.1-macOS-Intel-self-contained.tar.gz` | `0d6529837b55919dfdd616e0a2d5d5bdc4f3b373eeb226f705a4466266514ed1` |
