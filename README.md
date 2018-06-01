# Read Me

* Мотивация - что такое и зачем нужна изоморфность, cons/pros
* Отличие клиентского SPA от изоморфного, схемы работы, принципиальные отличия серверного и клиентского рендеринга с технической и архитектурной точек зрения
* Обзор технологий для реализации функционала серверного рендеринга \(отдельно для режимов разработки и прода\)
  * Node.js и Express для рендеринга JS-приложения и использования в качестве frontend-сервера
  * Webpack для компиляции кода приложения отдельно для клиента и для сервера
  * Babel для транспиляции кода приложения, в котором используются новейшие возможности языка, в диалект, который воспринимают все необходимые браузеры
  * Webpack-сервер для режима разработки, следящий за изменением кода в реальном времени, занимающийся перекомпиляцей только тех его участков, которые изменились, а также подключение middleware для hot-reloading приложения в браузере \(в целом рассказать про developer experience \(DX\) в контексте SPA и React\)
* Четыре Webpack-конфига \(отдельно для клиентского кода, отдельно для серверного, при этом для каждого есть два режима - development и production\)
  * Детальное рассмотрение каждого из конфигов, описываем необходимую и достаточную конфигурацию
  * Рефакторинг конфигов, как лучше организовать хранение файлов конфига в проекте, рассмотрение понятия переменных окружения, использование env-файлов
  * Структура проекта, алиасы, код-сплиттинг, клевые логи, крутые плагины, загрузчики стилей, картинок, svg и т.д., manifest.json и другие плюшки
* Описание процесса компиляции кода для разных режимов окружения \(dev, prod, test\), рассмотрение нескольких подходов в запуске и управлении этим процессом, как делать лучше с точки зрения масштабируемости/поддержки \(пишем скрипты на node.js\)
* Пошагово пишем пример приложения
  * Определение двух точек входа - client и server, отличия в рендеринге JSX
  * Подключение клиентского роутинга, рассмотрение и реализация нескольких подходов для постраничной загрузки данных на сервере и работы с этими данными в клиенте, фоллбеки \(в разрезе обычного JSON API\)
  * Подключение Redux-хранилища, настройка hot-reload для редьюсеров и redux sagas
  * Изоморфный фетчер данных
  * Реализация примера полноценной фичи, рассмотрение особенностей SSR в контексте реализации этой фичи
  * Стилизация компонентов \(демонстрация нескольких способов стилизации компонентов в React\), подключение styled-components с поддержкой серверного рендеринга
  * Аутентификация, защищенные маршруты, обработка редиректов
  * React-helmet и динамический head документа
* Итоги и куда развиваться дальше

