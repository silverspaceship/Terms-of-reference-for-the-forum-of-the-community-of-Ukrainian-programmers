# Next-Replace Product Requirements Document (Draft).

1. Блоги або статті
    > **plusxx:** <br>
    > Я особисто схиляюся в сторону саме структури блогів з можливістю підписки на конкретного автора, хоча можна робити й окремі статті.
2. Система тегів
    > **plusxx:** <br>
    > Побудована в моделі бази даних скоріше всього на зв’язках типу Many-to-Many.
      Тому де таблиця з трідами була пов'язана з таблицею тегів. А таблиця тегів в свою чергу пов'язувалася як Many-to-one з таблицею розділів,
      тому що до одного розділу може бути прив'язано багато тегів.
      Працювати це може так: при реєстрації новому користувачеві даються до вибору цікаві йому теги зі списку.
      При створенні нових трідів користувач повинен мати змогу вибрати готові теги, а також додавання своїх,
      нових тегів, котрі на стороні сервера будуть додаватися до таблиці тегів. Розділи потрібні для структуризації даних на першій сторінці форуму.

    > **P.Y.:** <br>
    > А якщо зробити так: є теги обов'язкові (вони ж розділи) і є теги додаткові (які користувач може довільно створювати сам). При створенні теми (тріду, обговорення, бесіди... — тут і далі називатиму це темою), має бути задано щонайменше 1 обов'язковий тег. Тегів може бути кілька, серед них можуть бути як обов'язкові, так і додаткові, але максимальну кількість тегів в одній темі варто обмежити, щоб запобігти спаму тегами для штучного привернення уваги.
      Обов'язкові теги-розділи структуровано в ієрархію розділів, яка відображається на головній сторінці — оскільки в кожній темі є 1 чи більше обов'язкових тегів, до неї можна дістатись, не вдаючись до пошуку та іншої магії.
      Модератори можуть перетворювати додаткові теги на обов'язкові, вбудовуючи їх в ієрархію розділів. Також вони можуть робити обов'язкові теги додатковими (фактично, видаляти розділ з ієрархії). Якщо внаслідок такої дії в деяких темах залишаються тільки теги, що стали додатковими, то до таких тем автоматично додається обов'язковий тег «все інше», який теж відображається як розділ у загальній ієрархії.
3. Темна тема форуму
    > **plusxx:** <br>
    > На початку можна додати лише темну, а потім допиляти ще кілька або кільканадцять.
4. Всі основні функції повинні працювати без JS
    > **plusxx:** <br>
    > Треба зробити так, щоб навіть з лінкса користувач міг притомно користуватись з ресурсу
      і одночасно додати всі можливі сучасні JS понти для користувачів, котрі не бояться JS.
      Ми повинні розуміти, що є люди, котрі нелюблять скриптів на стороні користувача,
      і часто їх параноя не безпідставна, і ми повинні їх поважати, але іншим потрібно дати
      повний можливий функціонал і швидкість, котре може дати JS.
5. Система карми
    > **plusxx:** <br>
    > Оцінювання є важливим стимулом. Лайки в соцмережах заставляють людей робити чудові речі. <br>
    > Тому нам потрібна система оцінювання користувачів. Ось мій варіант: <br>
    > * Лайки і дизлайки нараховуються лише постам, тобто при видаленні теми або посту всі лайки зникають.
    > * Дизлайки потрібні, щоб показати шкідливі розв'язання.
    > * Карма висвітлюється як сума всіх лайків і дизлайків плюс додаткові бали, див. нижче.
    > * Система оцінювання по спеціалізаціям. Після реєстрації користувач немає спеціалізації.
        Але коли користувач набере 100+ лаків, відповідаючи на питання з певним тегом, то цей тег стає його спеціалізацією.
        Можна мати кілька спеціалізацій.
        Всі лайки і дизлайки, котрі будуть відноситись до спеціалізації, будуть в карму додаватися(відніматися) подвійно.
        Можна додавати додаткові пункти за різні штуки, наприклад:
        за лінк на Github (+20 балів), за статтю, котра пройшла модерацію (+10 балів), за вказане місце роботи (+20 балів) і так далі.
    > * Висвітлення карми: Біля аватара висвітлюється загальна карма.
        Під постом карма пов'язана з кожним тегом, котрий стосується даної теми.
    > * Таким чином можемо показати компетенцію даного користувача в конкретній питанні.
    > * Ввести систему ачівок.
6. Удосконалений редактор постів
    > **plusxx:** <br>
    > Думаю, тут все зрозуміло. Треба лише вибрати найадекватніше рішення цього питання.
      Зробити тяжкою реєстрацію клонів. На початках ніяк. Забити на це і активніше модерувати.
      Однак якийсь механізм на майбутнє можна закласти, щоб активувати його пізніше.
7. Адаптивна верстка сторінок
    > **plusxx:** <br>
    > Тут думаю, все ясно, єдине пропоную використати Bootstrap або щось подібне.
8. Відповідь все погано однією кнопкою (див. нижче)
9. Розділ очікуючи на виправлення
    > **plusxx:** <br>
    > Якщо модератор бачить, що питання з формулюванням не правильно, він в один клік може кинути тему в розділ "очікує на виправлення",
      при чому в тему автоматично додасться славетний пост пана Коали "Все погано", котрий автоматично видаляється, коли користувач усе поправить і натисне відповідну кнопку.
      Тему в розділі "Очікує на виправлення" можуть бачити лише адміни, модератори і автор.
10. Посилання на конкретний пост
11. Удосконалений механізм пошуку по сайту
12. Емоджі
    > **plusxx:** <br>
    > Напевно питання з емоджі буде вирішуватись в самому кінці, але для мене ця ідея виглядає ок,
      якщо ми знайдемо, щоб хтось нам поробив спеціальні комп'ютерні емоджі.
13. Додати закриті (приватні) теми
    > **plusxx:** <br>
    > Навіщо це? Їх можуть використовувати групи студентів, котрі працюють над одним пет проектом, чи якісь хактивісти чи інші подібні групи.
14. Типу шелл для програмування (я так розумію, емулятор терміналу в браузері)
    > **plusxx:** <br>
    > Не вважаю цю задачу найбільш пріоритетною, але якщо є якесь притомне розв'язання, то хай би було.
15. Особисті повідомлення і повідомлення з закритих тем зберігаються в закодованому вигляді