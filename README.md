Добавление новой темы
=====================

- Выбрать и согласовать имя темы.
- Создать папку `ut/<имя-темы>`.
- Добавить туда содержимое из `ut/rfi_default`.
- Поменять в `ut/<имя-темы>/theme.json` параметр `name` на `<имя-темы>`.
- Править `theme.json`, добавлять любую новую статику, подключать её
  через `cssFiles`, `jsFiles`.


Страницы
========

Можно изменять дизайн следующих страниц (соответсвующим параметром в
`theme.json`):
- Страница ввода карточных данных (`layout`)
- Страница успешной оплаты (`successLayout`)
- Страница проваленной оплаты (`errorLayout`)

Структура страниц задаётся в виде произвольного дерева из div'ов, где
в листах могут находиться:
- предопределённые блоки.
- статические фрагменты, заданные в конфигурации темы.
- пустые div'ы (если нет соответствующего фрагмента).


Предопределённые блоки
======================

Все предопределённые блоки имеют имена из заглавных букв. Доступны
следующие блоки:

- `FORM` - платёжная форма.
- `ERROR` - информация об ошибке (имеет смысл только для страницы
  неудачной оплаты).
- `SUCCESS` - информация об успешном платеже (соответственно только
  для страницы успешной оплаты).
- `AMOUNT` - `<div id="amount">` с суммой и валютой платежа.
- `ORDER_COMMENT` - `<div id="order-comment">` описание платежа,
  переданное ТСП при его инициации.
- `ORDER_ID` - `<div id="order-id">` идентификатор платежа, присвоенный банком.
- `SERVICE_NAME` - описание ТСП хранящееся в ИС банка.
- `LOGO` - `logo.png` в отдельном div'е.
- `PCI_LOGO` - `pci_logo.png` в отдельном div'е.
- `HTTPS_DISCLAIMER` - стандартный текст, про то что для безопасности
  используется HTTPS, а карточные данные - не хранятся.

Статические фрагменты
=====================

