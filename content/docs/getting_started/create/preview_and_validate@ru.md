---
$title: Предварительный просмотр и проверка
---

Вы можете предварительно просмотреть страницу AMP так же, как и любой другой сайт со статическими страницами HTML. Для этого не требуются операции сборки или предварительной обработки. Воспользуйтесь одним из следующих способов:

  - **Откройте страницу непосредственно в браузере из файловой системы** (некоторые элементы могут не работать из-за ошибок запросов XMLHttpRequests).
  - **Используйте локальный веб-сервер, например, Apache 2 или Nginx**.
    *(Совет. Для быстрого создания веб-сервера запустите команду `python -m SimpleHTTPServer`.)*

Затем следует убедиться, что ваша страница AMP **действительно имеет допустимую разметку AMP**, в противном случае она не будет обнаруживаться и распространяться другими платформами, такими как Google Поиск. Для проверки:

  1. Откройте страницу в своем браузере.
  1. Добавьте к адресу URL "`#development=1`", например, `http://localhost:8000/released.amp.html#development=1`.
  1. Откройте [консоль Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/debug/console/) и проверьте наличие ошибок.

[Ознакомьтесь с дополнительной информацией о проверке](/ru/docs/fundamentals/validate.html) и способах устранения ошибок.

<div class="prev-next-buttons">
  <a class="button prev-button" href="/ru/docs/getting_started/create/presentation_layout.html"><span class="arrow-prev">Предыдущий</span></a>
  <a class="button next-button" href="/ru/docs/getting_started/create/prepare_for_discovery.html"><span class="arrow-next">Следующий</span></a>
</div>
