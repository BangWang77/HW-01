Команда `git add` производит добавление всех файлов в проекте в отслеживаемые. Это удобно, если требуется отслеживать несколько файлов.

Однако иногда существуют файлы, которые нельзя добавлять в репозиторий. Это могут быть локальные настройки проекта, учётные данные, сведения об ошибках, библиотеки, промежуточные результаты компиляции и другие. Такие файлы требуется добавлять в игнорируемые для GIT.

## Описание файла
Файл с описанием файлов, для которых не должно вестись отслеживание версий, имеет расширение `.gitignore`. Файл `.gitignore` представляет собой текстовый файл с перечнем шаблонов файловых имён, которые не должны отслеживаться.

Основные правила синтаксиса этого файла:

1. Одна строчка — один шаблон.

1. Пустые строки игнорируются.

1. Чтобы написать комментарий, в начале строки укажите знак `#`.

1. Символ `/` в начале строки указывает, что правило применяется ТОЛЬКО к файлам и каталогам, которые располагаются в том же каталоге, что и сам файл `.gitignore`.

1. Доступно использование спецсимволов:

  * Звёздочка `*` заменяет любое количество символов (в том числе и ноль). Например, правило *.avi будет игнорировать все файлы с расширением `.avi`;

* Знак вопроса `?` заменяет любой 1 символ. Можно размещать в любом месте правила;
* Две звёздочки `**` используются для указания любого количества подкаталогов. Например, `alex/**/account.txt` — будут игнорироваться все файлы в каталоге alex и во всех вложенных в него каталогах;
* Восклицательный знак ! в начале строки означает инвертирование правила;
* Символ `\` используется для экранирования спецсимволов;
* Символ `/` используется для разделения уровня каталогов`.
img`

В проекте может быть создано любое количество файлов .gitignore, однако обычно достаточно одного файла в корне проекта.

[На главную](/readme.md)