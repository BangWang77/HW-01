# Что такое GitHub и чем он отличается от Git
Как мы разобрались выше, [Git](/GITInfo.md) — это инструмент, позволяющий реализовать распределённую систему контроля версий.

[GitHub](https://github.com/) — сервис онлайн-хостинга репозиториев, обладающий всеми функциями распределённого контроля версий и функциональностью управления исходным кодом — всё, что поддерживает Git и даже больше. Также GitHub может похвастаться контролем доступа, багтрекингом, управлением задачами и вики для каждого проекта.

[Git-репозиторий](/Gitinit.md), загруженный на GitHub, доступен с помощью интерфейса командной строки Git и Git-команд. Также есть и другие функции: документация, запросы на принятие изменений (pull requests), история коммитов, интеграция со множеством популярных сервисов, email-уведомления, эмодзи, графики, вложенные списки задач, система @упоминаний, похожая на ту, что в Twitter, и т.д.

Кроме GitHub есть другие сервисы, которые используют Git, — например, Bitbucket и GitLab. Вы можете разместить Git-репозиторий на любом из них.

Чтобы работать с Git эффективнее, посмотрите [подборку шпаргалок: от основ до работы с GitHub](https://tproger.ru/articles/5-shpargalok-po-git-ot-osnov-do-raboty-s-github).

## Что такое система контроля версий
Чтобы лучше понимать, что такое Git и как он работает, нужно ещё знать, что такое система контроля версий.

Системы контроля версий (СКВ, VCS, Version Control Systems) позволяют разработчикам сохранять все изменения, внесённые в код. При возникновении проблем они могут просто откатить код до рабочего состояния и не тратить часы на поиски ошибок.

СКВ также позволяют нескольким разработчикам работать над одним проектом и сохранять внесённые изменения независимо друг от друга. При этом каждый участник команды видит, над чем работают коллеги.

## Типы систем контроля версий
Теперь вы знаете, что такое система контроля версий. Однако они тоже бывают разными. Существует три типа СКВ: локальная, централизованная и распределённая.

## Локальные системы контроля версий (ЛСКВ)

![lvcs-logo](/assets/LVCS-1.png)

В качестве метода контроля версий можно копировать файлы в отдельную директорию. Изменения сохраняются в виде наборов патчей, где каждый патч датируется и получает отметку времени. Таким образом, если код перестаёт работать, наборы патчей можно совместить, чтобы получить исходное состояние файла. Такой подход всё ещё распространён среди разработчиков.

## Централизованные системы контроля версий (ЦСКВ)
![CVCS-logo](/assets/CVCS-1.png)
ЦСКВ были созданы для решения проблемы взаимодействия с другими разработчиками. Такие системы имеют единственный сервер, содержащий все версии файлов, и некоторое количество клиентов, которые получают файлы из этого централизованного хранилища и там же их сохраняют. Тем не менее, такой подход имеет существенный недостаток — выход сервера из строя обернётся потерей всех данных. Кроме того, в таких системах может быть затруднена одновременная работа нескольких разработчиков над одним файлом.

## Распределённые системы контроля версий (РСКВ)
![DVCS=logo](/assets/DVCS-1.png)
Недостаток ЦСКВ был исправлен в РСКВ, клиенты которых не просто скачивают снимок всех файлов (состояние файлов на определённый момент времени), а полностью копируют репозиторий. Это значит, что у каждого клиента есть копия всего исходного кода и внесённых изменений. В этом случае, если один из серверов выйдет из строя, любой клиентский репозиторий может быть скопирован на другой сервер для продолжения работы. Ещё одним преимуществом РСКВ является то, что они могут одновременно взаимодействовать с несколькими удалёнными репозиториями. Благодаря этому разработчики могут параллельно работать над несколькими проектами. Именно поэтому Git сейчас так популярен.

#### [На главную](/readme.md).