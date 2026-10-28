# STATUS.md
Текущая веха: M1 (выполнена), переход к M2
Последний запуск: Workflow "Build IPA" #40658558598 в ветке codex/pr-build-m1 — УСПЕШНО
Что сделано:
- Форк willfaust/Madeira проверен (kabylbekerkhan-netizen/Madeira).
- Создана рабочая ветка `codex/pr-build-m1` (в соответствии с правилом "Работай в ветке, в main только после моего подтверждения").
- Добавлен remote `upstream` (https://github.com/willfaust/Madeira.git).
- Ветка `codex/pr-build-m1` отправлена в origin.
- Запущен GitHub Actions workflow Build IPA (ID запуска: 40658558598).
- Все джобы завершены успешно:
  - `plan`: 41с (ID 122715553676)
  - `fex`: 2м34с (ID 122715845028, артефакт `native-fex`)
  - `i386`: 10м30с (ID 122715844961, артефакт `native-i386`)
  - `llvm`: 22м52с (ID 122715845032, артефакт `native-llvm`)
  - `app`: 20м51с (ID 122725202053, артефакт `Madeira-ipa`)
- Артефакт `Madeira-ipa` скачан в `dist/Madeira.ipa` (размер 183 257 927 байт).
- Целостность подтверждена: 1402 файла внутри архива, бинарник `Payload/Madeira.app/Madeira` присутствует, `zipfile.testzip()` вернул `None` (0 ошибок).
- SHA256: `B91AF387764BD9F6D5BB829833862841725F73FC47F95A8CB6E30C5D41FB9618`.
Что пробовали и результат:
- Полный цикл компиляции и сборки из исходников в чистом форке на раннерах `xcode-27` занял 47 минут и завершился успехом без сбоев.
Следующий шаг:
- Веха M2: установка `Madeira.ipa` через SideStore на целевое устройство (iPhone 16 Pro Max, iOS 26.6.2), проверка зелёных статусов JIT и Memory+.
Блокеры:
- Нет.
