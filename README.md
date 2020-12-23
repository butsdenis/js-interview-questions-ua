# 300+ запитань з JavaScript для Junior, Middle та Senior

## Зміст

## Junior

1. [Загальні](#загальні)
1. [JS Core](#js-core)
1. [Функції](#функції)
1. [Front-end](#front-end)
1. [Верстка](#верстка)
1. [Angular](#angular)
1. [React](#react)
1. [Back-end](#back-end)
1. [Бази даних](#бази-даних)
1. [Інструменти](#інструменти)
1. [Практичні завдання](#практичні-завдання)

## Middle

1. [Загальні](#загальні-1)
1. [JS Core](#js-core-1)
1. [Функції](#функції-1)
1. [Front-end](#front-end-1)
1. [Верстка](#верстка-1)
1. [Angular](#angular-1)
1. [React](#react-1)
1. [Back-end](#back-end-1)
1. [Бази даних](#бази-даних-1)
1. [Інструменти](#інструменти-1)
1. [Практичні завдання](#практичні-завдання-1)

## Senior

1. [Загальні](#загальні-2)
1. [JS Core](#js-core-2)
1. [Функції](#функції-2)
1. [Front-end](#front-end-2)
1. [Angular](#angular-2)
1. [React](#react-2)
1. [Back-end](#back-end-2)
1. [Бази даних](#бази-даних-2)
1. [Інструменти](#інструменти-2)
1. [Практичні завдання](#практичні-завдання-2)

## Junior

1.  ### Загальні

    <details>
    <summary>1. Які методи HTTP-запитів ви знаєте?</summary>

    #### Найбільш поширені:

    `GET`

    Метод GET запитує представлення вказаного ресурсу. Запити, які використовують GET, повинні лише отримувати дані.

    `POST`

    Метод POST використовується для відправки об'єкта на вказаний ресурс, часто викликаючи зміну стану або побічних ефектів на сервері

    `PUT`

    Метод PUT замінює всі поточні представлення цільового ресурсу на корисне навантаження, що вказане в запиті.

    `DELETE`

    Метод DELETE видаляє вказаний ресурс.

    ***

    #### Інші:

    `HEAD`

    Метод HEAD запитує відповідь, ідентичну запиту GET, але без тіла.

    `CONNECT`

    Метод CONNECT встановлює тунель до сервера, ідентифікованого цільовим ресурсом.

    `OPTIONS`

    Метод OPTIONS використовується для опису варіантів зв'язку до цільового ресурсу.

    `TRACE`

    Метод TRACE виконує тест зворотного зв'язку по шляху до цільового ресурсу.

    `PATCH`

    Метод PATCH використовується для застосування часткових модифікацій в ресурсі.

    **Більш детально:**

    [MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)

    ***

    </details>

    <details>
    <summary>2. Які версії HTTP-протоколу вам відомі? *</summary>
    </details>

    <details>
    <summary>3. Які знаєте коди відповіді (стану) HTTP?</summary>
      
      **Коди згруповані в 5 класів:**

    - 1xx (інформаційні): в цей клас виділені коди, що інформують про процес передачі
    - 2xx (успішні операції): цей клас кодів вказує на те, що клієнтський запит був отриманий, зрозумілий сервером, прийнятий і успішно оброблений
    - 3xx (перенаправлення): коди цього класу повідомляють клієнту, що для успішного виконання операції необхідно зробити інший запит (як правило, по іншому URI)
    - 4xx (помилки клієнта): коди даного класу призначені для випадків, в яких клієнт робить невірні запити
    - 5xx (помилки сервера): коди відповідей цього класу відносяться до випадків, в яких сервер ідентифікує, що сталася помилка з його вини або він по якійсь причині не в змозі виконати запит

    ***

    **Основні**

    | Код відповіді | Назва коду                               | Опис відповіді сервера                                                                                                     |
    | ------------- | ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
    | 200           | OK                                       | Успішно оброблений запит.                                                                                                  |
    | 201           | Created (Створено)                       | Запит успішно виконаний і в результаті був створений новий ресурс.                                                         |
    | 202           | Accepted (Прийнято)                      | Запит прийнятий, але ще не оброблений.                                                                                     |
    | 400           | Bad Request (Неправильний запит)         | Ця відповідь означає, що сервер не зміг зрозуміти клієнтський запит з причини невірного синтаксису.                        |
    | 403           | Forbidden (Заборонено)                   | Сервер зрозумів запит, але він відмовляється його виконувати через обмеження в доступі для клієнта до зазначеного ресурсу. |
    | 404           | Not Found (Не знайдено)                  | Сервер не може знайти запитуваний ресурс.                                                                                  |
    | 503           | Service Unavailable (Сервіс недоступний) | Сервер не готовий обробляти запит. Сервер тимчасово не має можливості обробляти запити з технічних причин.                 |

    **Більш детально:**

    [UA](https://uk.wikipedia.org/wiki/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%D0%BA%D0%BE%D0%B4%D1%96%D0%B2_%D1%81%D1%82%D0%B0%D0%BD%D1%83_HTTP)

    [MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

    ***

    </details>

    <details>
    <summary>4. Що таке Cross-Origin Resource Sharing? Як усунути проблеми з CORS? **</summary>
      
      ***Cross-Origin Resource Sharing (CORS, перехресний обмін ресурсами)*** — це механізм, що за допомогою HTTP-заголовків дає переглядачеві дозвіл завантажувати ресурси з певного джерела на запит web-застосунка, отриманого з відмінного джерела. Web-застосунок виконує **перехресний HTTP-запит** коли потребує ресурсів з джерела (домен, протокол чи порт), відмінного від його власного.  
      >Приклад перехресного запиту: JavaScript-код web-застосунка, розміщеного на http://domain-a.com, намагається за допомогою AJAX-запиту отримати http://api.domain-b.com/data.json.

    **Більш детально:**

    [MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)

    ***

    </details>

    <details>
    <summary>5. Що таке cookie?</summary>

    **_Cookie_** - це дані, які зберігаються безпосередньо в браузері. Вони є частиною HTTP-протоколу, визначеного в специфікації RFC 6265. Cookie зазвичай встановлюються веб-сервером за допомогою заголовка `Set-Cookie`. Потім браузер буде автоматично додавати їх в (майже) кожен запит на той же домен за допомогою заголовка `Cookie`.  
    Один з найбільш частих випадків використання - це аутентифікація:

    - При вході на сайт сервер посилає у відповідь HTTP-заголовок `Set-Cookie` для того, щоб встановити куки зі спеціальним унікальним ідентифікатором сесії.
    - Під час наступного запиту до цього ж домену браузер посилає на сервер HTTP-заголовок `Cookie`. Таким чином, сервер розуміє, хто зробив запит. Ми також можемо отримати доступ до куки безпосередньо з браузера, використовуючи властивість [document.cookie](https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie).

    **Більш детально:**

    [WIKI_UA](https://uk.wikipedia.org/wiki/%D0%9A%D1%83%D0%BA%D0%B8)

    [MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)

    ***

    </details>

    <details>
    <summary>6. Який максимальний розмір cookie?</summary>

    Відповідно до специфікації [IETF cookie specification](https://www.ietf.org/rfc/rfc6265.txt), веб-браузери повинні забезпечувати такі мінімальні вимоги:

    - не менше 300 cookies;
    - принаймні 4096 байт на cookie;
    - принаймні 20 cookies на унікальний хост або доменне ім'я.

    | Browser | Cookie count limit per domain | Total size of cookies |
    | ------- | ----------------------------- | --------------------- |
    | Chrome  | 180                           | 4096                  |
    | Firefox | 150                           | 4097                  |
    | Opera   | 60                            | 4096                  |
    | Safari  | 600                           | 4093                  |

    ***

    </details>

    <details>
    <summary>7. Що означає директива use strict?</summary>

    [MDN_UA](https://developer.mozilla.org/uk/docs/Web/JavaScript/Reference/Strict_mode)
    </details>

    <details>
    <summary>8. Чим JS відрізняється під час роботи на front-end і back-end? *</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>9. Що таке статична і динамічна типізації?</summary>

    **_Динамічна типізація_** - прийом, широко використовуваний у мовах програмування і мовах специфікації, при якому змінна зв'язується з типом в момент присвоювання значення, а не в момент оголошення змінної. Таким чином, в різних ділянках програми одна і та ж змінна може приймати значення різних типів.

    ```javascript
    // Одразу по оголошенню змінна foo разом з початковим значенням отримує тип Number
    let foo = 42;
    console.log(foo + 1); // виводить 43
    // Змінна отримує нове значення й тепер має тип String
    foo = "bar";
    console.log(foo + 1); // виводить "bar1"
    // Разом із значенням true тип змінної foo обертається на Boolean
    foo = true;
    ```

    **_Статична типізація_** - прийом, широко використовуваний у мовах програмування, при якому змінна, параметр підпрограми, що повертає значення функції зв'язується з типом в момент оголошення та тип не може бути змінений пізніше (змінна або параметр будуть приймати, а функція - повертати значення тільки цього типу).

    ```ts
    // Одразу по оголошенню змінна foo отримує тип Number
    let foo: number;
    foo = "hello"; // Type 'number' is not assignable to type 'string'.
    ```

    **Більш детально:**

    [MDN_UA](https://developer.mozilla.org/uk/docs/Web/JavaScript/Data_structures)

    ***

    </details>

    <details>
    <summary>10. Як клієнт взаємодіє із сервером?</summary>

    Якщо коротко, клієнт посилає запит до сервера. Сервер приймає запит і відправляє відповідь. Клієнт її приймає й відображає отриману інформацію. В клієнт-серверній моделі сервер надає сервіс чи ресурси, котрі отримують клієнти, виконуючи запити. При цьому клієнт може бути чим завгодно: Мобільним-додатком, браузером або банкоматом. Перевага такого принципу в тому, що так підтримується розподіл інтересів. Якщо в вас є єдина машина-сервер, цього достатньо, а клієнти тим часом можуть бути різними.
    ![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/Client-server-model.svg/1920px-Client-server-model.svg.png "Client-server model")

    **Більш детально:**

    [WIKI_UA](https://uk.wikipedia.org/wiki/%D0%9A%D0%BB%D1%96%D1%94%D0%BD%D1%82-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%BD%D0%B0_%D0%B0%D1%80%D1%85%D1%96%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0)

    ***

    </details>

    <details>
    <summary>11. Що таке REST?</summary>

    Передача репрезентативного стану (**_англ. \_Representational State Transfer, REST_**) - це набір архітектурних обмежень, які утворюють ефективні, надійні та масштабовані розподілені системи. Система називається RESTful, коли дотримується цих обмежень. Головна ідея REST полягає в тому, що ресурс, наприклад, документ, передається разом зі своїм станом та зв'язками (гіпертекстом) за допомогою чітко визначених, стандартизованих операцій та форматів. Часто API або сервіси називають себе RESTful, коли прямо змінюють тип документа, як протилежність запуску команд в іншому місці. Через те, що HTTP, стандартний протокол Web, також передає документи та гіпертекстові посилання, прості HTTP API іноді називають RESTful API, RESTful сервісами, або просто REST сервісами, хоча вони не обов'язково дотримуються усіх обмежень REST. Початківці можуть припустити, що REST API означає HTTP-сервіс, який можна викликати за допомогою стандартних веб-бібліотек та інструментів.

    **Більш детально:**

    [WIKI_UA](https://uk.wikipedia.org/wiki/REST)

    [DOU](https://dou.ua/lenta/articles/rest-conception/)

    ***

    </details>

    <details>
    <summary>12. Поясніть поняття мутабельність / іммутабельність? Які типи є мутабельними й навпаки?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>13. Як шукати помилки в коді?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>14. Яких відомих людей зі світу JS знаєте? *</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### JS Core

    <details>
    <summary>15. Які існують типи даних у JS?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>16. Як перевірити, чи об’єкт є масивом?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>17. Як перевірити, чи число є скінченним?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>18. Як перевірити, що змінна рівна NaN?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>19. Чим відрізняється поведінка isNaN() та Number.isNaN()?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>20. Порівняйте ключові слова var, let, const.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>21. Що таке область видимості?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>22. Що таке деструктуризація?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>23. Для чого призначені методи setTimeout і setInterval?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>24. Порівняйте підходи роботи з асинхронним кодом: сallbacks vs promises vs async/await.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>25. Чи можна записувати нові властивості / функції в прототипи стандартних класів (Array, Object тощо)? Чому ні? У яких випадках це робити можна? Як убезпечити себе, якщо потрібно розширити прототип?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>26. Назвіть методи масивів, які пам’ятаєте, і скажіть, для чого вони потрібні.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>27. Які перебираючі методи масиву знаєте? У чому їхня відмінність?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>28. Як працюють оператори присвоєння / порівняння / рядкові / арифметичні / бітові тощо?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>29. Опишіть призначення і принципи роботи з колекціями Map і Set.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>30. Що означає глибока (deep) та поверхнева (shallow) копія об’єкта? Як зробити кожну з них?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### Функції

    <details>
    <summary>31. Яка різниця між декларацією функції (function declaration) та функціональним виразом (function expression)?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>32. Що таке анонімна функція?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>33. Розкажіть про стрілкові функції (arrow function). В чому полягають відмінності стрілкових функцій від звичайних?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>34. Що таке і для чого використовують IIFE (Immediately Invoked Function Expression)?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>35. Що таке hoisting, як він працює для змінних і функцій?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>36. Що таке замикання (closure) і які сценарії його використання?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>37. Як ви розумієте замикання? Що буде виведено в консолі у прикладі нижче?</summary>
    <div>

    ```javascript
    var f = function () {
      console.log(1);
    };

    var execute = function (f) {
      setTimeout(f, 1000);
    };

    execute(f); // Що буде виведено в консолі?

    f = function () {
      console.log(2);
    };
    ```

    </div>
    </details>

    <details>
    <summary>38. Що таке рекурсія?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>39. Що означає ключове слово this?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>40. Що таке втрата контексту, коли відбувається і як їй запобігти?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>41. Методи функцій bind / call / apply — навіщо і в чому різниця?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### Front-end

    <details>
    <summary>42. Що таке DOM?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>43. Порівняйте атрибути підключення скрипту async і defer в HTML-документі.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>44. Яка різниця між властивостями HTML-елементів innerHTML і innerText?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>45. Опишіть процес спливання (bubbling) подій у DOM.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>46. Як зупинити спливання (bubbling) події?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>47. Як зупинити дефолтну обробку події?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>48. Чому дорівнює this в обробнику подій (event handler)?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>49. Що таке LocalStorage і SessionStorage? Який максимальний розмір LocalStorage?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>50. Як отримати висоту блоку? Його положення щодо меж документа?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>51. Що таке webpack?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>52. Чим відрізняється dev-збірка від prod?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### Верстка

    <details>
    <summary>53. Що таке блокова модель CSS?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>54. Які способи центрування блокового контенту по горизонталі та вертикалі знаєте?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>55. Які підходи у верстці вам відомі (float, flex, grid, etc)?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>56. Як зробити додаток responsive?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>57. Які є принципи семантичної верстки?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>58. Навіщо потрібні префікси для деяких CSS-властивостей (-webkit-, -moz- тощо)?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>59. Як спростити написання кросбраузерних стилів?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>60. Практичне завдання: прокоментувати та виправити приклад поганого CSS або HTML.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>61. Що таке CSS-препроцесори? З якими працювали? Що нового вони приносять у стандартний CSS?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### Angular

    <details>
        <summary>62. Перерахуйте основні компоненти фреймворку (модуль, роут, директива тощо).</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>63. У чому різниця між компонентом і директивою?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>64. Розкажіть про життєвий цикл компонента.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>65. Перерахуйте часто використовувані хуки життєвого циклу компонента та розкажіть, для чого вони потрібні?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>66. У чому різниця між конструктором і ngOnInit-хуком?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>67. Як захистити роут від несанкціонованого доступу? Які механізми надає для цього фреймворк?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>68. Що таке Lazy loading, як і для чого використовується?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>69. Яке призначення RouterOutlet?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>70. Як компоненти можуть взаємодіяти один з одним?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>71. Як створити two-way binding властивість для компонента?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>72. Які типи форм є у фреймворку? У яких випадках і що краще використовувати?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>73. Які стани є у форми і як це можна застосувати?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>74. Навіщо потрібні сервіси? Як з ними працювати?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>75. Що таке singleton-сервіси? Яке їхнє призначення? Спосіб створення?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>76. Які є способи оголошення сервісів?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>77. Для чого потрібні модулі? Скільки їх має бути в проєкті?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>78. Навіщо потрібні загальні модулі (shared)?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>79. Які переваги типізації в TypeScript?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>80. Які можливості TypeScript можна використовувати для типізації (тут мають на увазі інтерфейси, типи, enum тощо)?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>81. Яка різниця між інтерфейсом і класом?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>82. У чому різниця між інтерфейсом і абстрактним класом?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>83. Яка різниця між інтерфейсом і типом?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>84. Що таке RxJS? Як він використовується у фреймворку? Які компоненти фреймворку тісно пов’язані з ним?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>85. Чим відрізняються Observable і Promise?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>86. Для чого потрібні Subjects? Які типи Subjects існують?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>87. Як зробити кілька послідовних запитів до API за допомогою HTTP-сервісу і RxJS?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>88. Яка різниця між switchMap, concatMap, mergeMap?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>89. Як можна конфігурувати Angular-застосунок?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>90. Навіщо потрібні environment-файли? Коли їх краще не використовувати?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>91. У чому різниця між «розумним» (smart) і «дурним» (dumb) компонентами? У яких випадках застосовується кожен з них?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>92. У чому різниця між NgForm, FormGroup і FormControl і як їх застосовують для побудови форм?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>93. Навіщо потрібен і як працює async pipe?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>94. Як стежити за розвитком фреймворку? Яких відомих людей, пов’язаних з Angular, знаєте / читаєте?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### React

    <details>
    <summary>95. Чи працювали з класовими компонентами? У чому їхня особливість?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>96. Які дані краще зберігати в стані компонента, а які передавати через пропси? Наведіть приклад.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>97. Чи ознайомлені з хуками? У чому їхні переваги? Чи доводилося робити свої і з якою метою?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>98. Чи ознайомлені з фрагментами та порталами? Навіщо вони потрібні?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>99. Коли й для чого використовують рефи?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>100. Які ви знаєте методи життєвого циклу компонента?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>101. В якому методі життєвого циклу компонента краще робити запити на сервер? Чому?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>102. В якому методі життєвого циклу компонента краще робити підписку і відписку від лістенера? Чому? Навіщо відписуватися?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>103. Чи був досвід роботи з контекстом? Коли його варто використовувати?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>104. У чому особливість PureComponent?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>105. Чи працював з мемоізованими селекторами (memoized selectors)? Для чого їх використовують і який принцип роботи?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>106. У чому бачите переваги бібліотеки React?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>107. Чому бібліотека React швидка? Що таке Virtual DOM і Shadow DOM?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>108. Навіщо в списках ключі? Чи можна робити ключами індекси елементів масиву? Коли це виправдано?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>109. В чому основна ідея Redux?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>110. Робота зі стилями в React.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>111. React — це бібліотека чи фреймворк? Яка різниця між цими двома поняттями.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>112. Чи можна використовувати jQuery разом з React? Чому так / ні?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>113. Що таке codemod?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>114. Чи доводилося налаштовувати проєкт React з нуля? За допомогою яких інструментів ви це робили?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>115. Перерахуйте всі бібліотеки, які використовували у зв’язці з React.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>116. Що найскладніше доводилося реалізовувати за допомогою React?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### Back-end

    <details>
    <summary>117. Що таке REPL?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>118. Що таке streams в Node.js?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>119. Що таке middleware?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>120. Для чого використовують функцію setImmediate?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>121. Навіщо потрібен app.param() в express?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>122. Що таке token based authentication?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### Бази даних

    <details>
    <summary>123. Напишіть простий запит для обчислення трьох авторів, у яких найбільше книг.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>124. Напишіть запит, який вибирає останні три коментарі для конкретного користувача для двох таблиць: коментарі та користувачі.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>125. Спроєктуйте просту схему бази даних для бібліотеки.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>126. Для чого використовують SQL-оператор HAVING?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>127. Навіщо використовують SQL-оператор LEFT JOIN?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>128. Чим відрізняється embed- від reference-зв’язку в MongoDB?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>129. В одному проєкті програмісти зберігають дані в MongoDB-колекції коментарів, використовуючи такі типи даних (дивіться нижче). Що поганого в цьому рішенні?</summary>
    <div>

    ```javascript
    id: ObjectID;
    text: string;
    author_id: string;
    created_at: Date;
    ```

    </div>
    </details>

    <details>
    <summary>130.У проєкті знадобилося внести зміни в структуру таблиць, додати кілька полів і індекси. Як програмісти будуть робити це на продакшені?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### Інструменти

    <details>
    <summary>131. Щоразу, коли ви робите pull, чомусь трапляється конфлікт в останньому рядку в усіх файлах, які ви редагували. Що відбувається?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>132. Що робить команда git fetch?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>133. Які git hygiene підходи ви знаєте?</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>134. Що таке CI/CD? Для чого це потрібно?</summary>
    <div>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

1.  ### Практичні завдання

    <details>
    <summary>135. Розкажіть, які є способи копіювання простого об’єкта типу obj = {a: 1, b: 2, c: 3}</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>136. Напишіть deep clone для об’єкта.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>137. Назвіть різні способи, як поміняти місцями значення двох змінних.</summary>
    <div>
    </div>
    </details>

    <details>
    <summary>
      <span>138. Менеджер попросив у задачі поміняти статуси з «active, inactive» на «active, removed», але в коді фігурують тільки цифри й незрозуміло, який статус відповідає якій цифрі. Як допомогти майбутнім програмістам не лізти в документацію за кодом? Питання ставлять на конкретному прикладі з кодом.</span>
    </summary>
    <div>
    </div>
    </details>

    <details>
    <summary>139. Необхідно зробити мініпроєкт — список користувачів з формою створення/редагування користувача. Вимоги нижче.</summary>
    <div>
      <ul>
        <li>Для зберігання користувачів використовуйте Firebase (це безкоштовно).</li>
        <li>Для стилізації використовуйте Bootstrap.</li>
        <li>Мінімальний набір полів користувача:
          <ul>
            <li>ім’я;</li>
            <li>прізвище;</li>
            <li>електронна пошта;</li>
            <li>телефон (у форматі +380 (XX) XXX-XX-XX);</li>
            <li>дата народження;</li>
            <li>буде плюсом — додавання аватара та можливість crop-картинки.</li>
          </ul>
        </li>
        <li>Список користувачів повинен мати можливість фільтрації та пагінацію.</li>
        <li>Проєкт має містити README-файл з кроками для запуску.</li>
      </ul>
    </div>
    </details>

    **[⬆ До змісту](#зміст)**

## Middle

1.  ### Загальні

    **[⬆ До змісту](#зміст)**

1.  ### JS Core

    **[⬆ До змісту](#зміст)**

1.  ### Функції

    **[⬆ До змісту](#зміст)**

1.  ### Front-end

    **[⬆ До змісту](#зміст)**

1.  ### Верстка

    **[⬆ До змісту](#зміст)**

1.  ### Angular

    **[⬆ До змісту](#зміст)**

1.  ### React

    **[⬆ До змісту](#зміст)**

1.  ### Back-end

    **[⬆ До змісту](#зміст)**

1.  ### Бази даних

    **[⬆ До змісту](#зміст)**

1.  ### Інструменти

    **[⬆ До змісту](#зміст)**

1.  ### Практичні завдання
    **[⬆ До змісту](#зміст)**

## Senior

1.  ### Загальні

    **[⬆ До змісту](#зміст)**

1.  ### JS Core

    **[⬆ До змісту](#зміст)**

1.  ### Функції

    **[⬆ До змісту](#зміст)**

1.  ### Front-end

    **[⬆ До змісту](#зміст)**

1.  ### Angular

    **[⬆ До змісту](#зміст)**

1.  ### React

    **[⬆ До змісту](#зміст)**

1.  ### Back-end

    **[⬆ До змісту](#зміст)**

1.  ### Бази даних

    **[⬆ До змісту](#зміст)**

1.  ### Інструменти

    **[⬆ До змісту](#зміст)**

1.  ### Практичні завдання
    **[⬆ До змісту](#зміст)**
