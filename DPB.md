# Launch DPB from a profile / Запуск DPB из профиля

## English

DPB integration in MultiABF preview169 supports PoE1/DPB1. DPB is a separate product: install your own supported DPB copy and complete its normal authentication/licensing as required. MultiABF does not include DPB, change its binaries or start bot actions automatically. Accepted version: DPB0.3.29.46. DPB2 is not covered by this release.

1. Open MultiABF **Settings → General**. Select the existing **DreamPoeBot.exe** in the optional DPB executable field and press **Save**. Select the executable in its installed folder, with its supporting files beside it. This setting is shared by profiles.
2. Create or select a **PoE1** profile and press **Start**. Wait for the game to be running. Both the ordinary Windows-user mode and the experimental separate standard-user mode are supported.
3. Open that profile’s **⋯ menu** and choose **Launch DPB**. Accept the Windows UAC request if it appears. MultiABF supplies the managed game PID and its game settings automatically. You do not need to copy PID or edit files.
4. DPB opens with private settings for this profile. Its normal authentication, if required, remains inside DPB. Starting DPB does not start the bot; bot operation is a separate action in DPB.
5. To finish, use **Stop** on the MultiABF profile. The owned game stops and its DPB receives a normal close request. Other profiles and independently launched DPB processes are not closed. You can also close DPB normally yourself.

### Why Launch DPB is unavailable

The action needs a running managed PoE1 profile, a saved valid DPB executable and no existing managed DPB launch for that profile. It is unavailable for a stopped/preparing profile, PoE2 or a profile whose DPB is already starting/running. Read the menu hint and profile **Diagnostics** for the reason. A running process alone is not proof of completed DPB initialization; diagnostics distinguish startup, observed initialization and errors.

Canceling UAC leaves the game running. If DPB does not close, check Diagnostics and close its window normally; MultiABF reports the unfinished shutdown. Do not start extra copies manually to bypass a reported active managed run.

### Files and updates

On first use, MultiABF creates a verified private copy of DPB application components under the profile data directory: profiles/<profile-id>/dpb/application. Saved DPB settings and logs belong to that profile. The selected original DPB installation is left unchanged. Other DPB profiles/logs are not copied; existing global settings can seed the private profile once. Keep credentials and DPB logs private.

Unchanged components are reused on later launches and after restarting MultiABF. When selected source components change, the private code copy is refreshed while its saved profile settings are retained. The accepted laptop copy used about44.7MiB per profile; your installation may differ. Stop the profile and DPB before updating or deleting its files. Normal profile deletion removes its owned DPB data after shutdown.

## Русский

Интеграция MultiABF preview169 предназначена для **PoE1/DPB1**. DPB устанавливается отдельно и использует собственную авторизацию и лицензию. MultiABF не распространяет DPB, не изменяет его бинарные файлы и не запускает действия бота автоматически. Проверенная версия DPB — **0.3.29.46**. Поддержка DPB2 этим релизом не подтверждена.

1. Откройте **Настройки → Общие**, выберите существующий **DreamPoeBot.exe** в поле DPB и нажмите **Сохранить**. Указывайте EXE из установленной папки DPB вместе с его компонентами. Путь задаётся один раз для всех профилей.
2. Создайте или выберите профиль **PoE1**, нажмите **Запустить** и дождитесь работающей игры. Поддержаны обычный пользователь Windows и экспериментальный отдельный стандартный пользователь.
3. Откройте меню **⋯** этого профиля и выберите **Запустить DPB**. Подтвердите UAC, если Windows его покажет. PID игры и путь к игровому конфигу передаются автоматически. Вручную исправлять файлы не нужно.
4. DPB откроется с отдельными настройками этого профиля. При необходимости выполните его обычную авторизацию внутри DPB. Сам бот автоматически не стартует.
5. Нажмите **Остановить** у профиля MultiABF: игра остановится, а запущенный для неё DPB получит обычный запрос закрытия. Другие профили и самостоятельно запущенные DPB не закрываются. DPB также можно закрыть вручную обычным способом.

Если команда недоступна, проверьте: путь DPB сохранён, профиль PoE1 уже работает и для него нет другого запуска DPB. Для PoE2 команда не поддержана. Причина доступна в подсказке меню и **Диагностике** профиля. Диагностика различает создание процесса и наблюдаемую инициализацию DPB.

Настройки и логи DPB хранятся отдельно внутри данных каждого профиля. При первом запуске создаётся проверенная копия компонентов; повторные запуски используют её снова. Изменение исходных компонентов обновляет копию с сохранением настроек. Оригинальная установка DPB остаётся без изменений. Отмена UAC оставляет игру работающей. Если DPB не закрылся, MultiABF покажет это в диагностике — закройте его окно обычным способом.

[Back to README](README.md) · [Troubleshooting](TROUBLESHOOTING.md)
