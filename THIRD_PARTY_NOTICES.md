# Компоненты третьих лиц / Third-Party Notices

MultiModelStudio является проприетарным ПО (см. `LICENSE.md`). Перечисленные ниже компоненты
принадлежат третьим лицам и используются на условиях их собственных лицензий. Эти лицензии не
распространяются на код MultiModelStudio и не ограничиваются `LICENSE.md`.

MultiModelStudio is proprietary software (see `LICENSE.md`). The components below belong to third
parties and are used under their own licenses, which neither extend to MultiModelStudio code nor are
restricted by `LICENSE.md`.

## Пакеты NuGet (из `*.csproj`)

| Компонент | Версия | Лицензия | Правообладатель |
|---|---|---|---|
| Avalonia, Avalonia.Desktop, Avalonia.Fonts.Inter, Avalonia.Themes.Fluent | 11.3.20 | MIT | AvaloniaUI OÜ and contributors |
| Microsoft.EntityFrameworkCore, .Sqlite, .Design | 8.0.0 | MIT | Microsoft Corporation / .NET Foundation |
| Microsoft.Extensions.DependencyInjection, Microsoft.Extensions.Hosting | 8.0.0 | MIT | Microsoft Corporation / .NET Foundation |
| NAudio | 2.2.1 | MIT | Mark Heath (текст: `docs/NAUDIO_LICENSE.txt`) |
| Inter (шрифт, через Avalonia.Fonts.Inter) | — | SIL Open Font License 1.1 | Rasmus Andersson |
| xunit, xunit.runner.visualstudio, Microsoft.NET.Test.Sdk | 2.8.x / 17.10.0 | Apache-2.0 / MIT | .NET Foundation, Microsoft (только тесты) |
| .NET Runtime / SDK 8 | 8.0.x | MIT | Microsoft Corporation / .NET Foundation |

## Комплектные и внешние компоненты

| Компонент | Лицензия | Примечание |
|---|---|---|
| SampleMcpServer | MIT (текст: `docs/SAMPLEMCP_LICENSE.txt`, манифест: `docs/SAMPLEMCP_BUNDLE.json`) | комплектный MCP-сервер, **в репозиторий не входит** |
| llama.cpp / llama-server | MIT | внешний рантайм, **в репозиторий не входит**, скачивается или собирается пользователем |
| MOTEKA Runtime | MIT | отдельный репозиторий `moteka`, **в репозиторий не входит** |
| tesseract (OCR) | Apache-2.0 | внешний опциональный CLI, вызывается через `Process` |
| nvidia-smi | проприетарная (NVIDIA) | внешний опциональный CLI, вызывается через `Process` |
| Модели машинного обучения (GGUF, safetensors и др.) | лицензии их авторов | **в репозиторий не входят**; ответственность за соблюдение лицензий моделей несёт пользователь |

Список составлен по состоянию на 18.09.2026 по файлам `*.csproj` и `docs/`. При добавлении зависимости
запись добавляется сюда в том же коммите.

## Опциональные классификаторы памяти, 23.09.2026

[multilingual MiniLMv2 L6](https://huggingface.co/MoritzLaurer/multilingual-MiniLMv2-L6-mnli-xnli)
и [mDeBERTa-v3-base MNLI/XNLI](https://huggingface.co/MoritzLaurer/mDeBERTa-v3-base-mnli-xnli)
от MoritzLaurer — MIT по официальным карточкам. Веса и Python-зависимости не распространяются
в репозитории/архиве исходников. Ревизии, хеши и использованные версии ONNX Runtime/tokenizers —
`tools/MemoryClassifier/README.md`. Сохранять лицензии отдельно установленного комплекта.

## Скачиваемые пакеты памяти M-28

Базовая поставка не содержит следующие бинарные зависимости. По запросу пользователя загрузчик получает оригинальные архивы и сохраняет входящие в них лицензии: Python 3.12.10 (PSF), ONNX Runtime 1.20.1 (MIT), tokenizers 0.22.2 (Apache-2.0), NumPy 2.4.3 (BSD-3-Clause), packaging 25.0 (Apache-2.0/BSD-2-Clause), flatbuffers 25.2.10 (Apache-2.0), protobuf 5.29.5 (BSD-3-Clause), sympy 1.13.3 и mpmath 1.3.0 (BSD-3-Clause), coloredlogs 15.0.1 и humanfriendly 10.0 (MIT). Версии/URL/SHA закреплены в каталоге MemoryModules/catalog.json. Модели: intfloat/multilingual-e5-small (MIT) и MoritzLaurer/mDeBERTa-v3-base-mnli-xnli (MIT), исходные карточки на Hugging Face.
