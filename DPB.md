# DPB profiles / DPB в профилях

## English

MultiABF 1.0.0 supports managed PoE1/DPB1 and PoE2/DPB2 launch. Install DPB separately with its supporting files and normal licensing. MultiABF supplies the owned game's PID and private game settings; launching DPB never starts a bot.

1. In Settings → General select four independent paths: PoE1, DPB1, PoE2, DPB2. Saved paths are absolute. Select the matching game when creating a profile.
2. Start the profile and wait for its game window. Use the DPB button at the upper right of its card. Accept Windows elevation if requested.
3. The footer distinguishes DPB startup, running and observed connection. Connection does not assert that every third-party plugin initialized successfully.
4. DPB settings/components are private to each profile. The installed source copy is preserved. Missing keyboard sections can be copied from the normal game config without copying login data or replacing existing bindings.
5. Stop closes that profile's owned game and DPB. Closing MultiABF stops its managed profiles/DPB; unfinished cleanup is shown as an error. Independent processes are excluded.

Game updates use the official standalone launcher, outside Sandboxie, before profile startup. Automatic game updates default On; disable them in General if you manage updates yourself. A running client blocks an update of its installation. Cancel waits for safe updater completion and does not start the profile. Steam installations use Steam updates. DPB and plugins are not updated by this feature.

On another computer choose that computer's game/DPB paths and create its own profiles. Copying files does not migrate Windows-bound credentials or recreate Windows accounts. Deleting a stopped profile also removes its application-created separate Windows user; the confirmation explicitly says so. Accounts/processes not owned by that profile are excluded.

## Русский

MultiABF 1.0.0 поддерживает запуск PoE1/DPB1 и PoE2/DPB2. DPB устанавливается отдельно вместе со своими компонентами и использует собственную лицензию. MultiABF передаёт PID управляемой игры и её приватные настройки. Автоматического Start бота нет.

1. В «Настройки → Общие» отдельно выберите PoE1, DPB1, PoE2 и DPB2. Пути сохраняются абсолютными. При создании профиля выберите нужную игру.
2. Запустите профиль и дождитесь окна игры. Нажмите DPB справа сверху на его карточке. При необходимости подтвердите повышение прав Windows.
3. Строка снизу различает запуск, работающий процесс и подтверждённое подключение DPB. Подключение не означает успешную инициализацию всех сторонних плагинов.
4. Компоненты и настройки DPB отдельны для каждого профиля. Исходная установка сохраняется. Недостающие секции клавиш берутся из обычного конфига игры; данные входа не копируются, существующие бинды сохраняются.
5. Stop завершает игру и DPB этого профиля. Закрытие MultiABF останавливает его управляемые профили и DPB; незавершённая остановка показывается как ошибка. Независимые процессы не затрагиваются.

Автообновление игры включено по умолчанию и управляется в общих настройках. Работает штатный загрузчик вне песочницы, до запуска профиля. Работающая игра блокирует обновление своей установки. Отмена ждёт безопасного завершения обновления и не запускает профиль. Steam обновляется через Steam. DPB и плагины эта функция не обновляет.

На другом компьютере выберите его пути игр/DPB и создайте локальные профили. Перенос файлов не переносит привязанные к Windows секреты и не создаёт пользователей Windows. При удалении остановленного профиля удаляется также отдельный пользователь Windows, созданный MultiABF для него; это указано в подтверждении. Чужие пользователи и процессы исключены.
