# Тестовое задание FunBox
[https://dl.fun-box.ru/qt-js.pdf](https://dl.fun-box.ru/qt-js.pdf)

## Level I

>Q1
>
>Расскажите, чем, на ваш взгляд, отличается хорошее клиентское приложение от плохого с точки зрения пользователя, менеджера проекта, дизайнера, верстальщика, серверного программиста.

*Хорошее приложение - это...*

Для пользователя - удобство пользования (как бы каламбурно ни звучало) и быстрота работы приложения (скорость нынче в моде).

Для менеджера - хз, но наверное, возможность масштабировать. То есть, внедрить (и, конечно, продать) новые фичи.

Для дизайнера - когда дизайн чётко решает поставленные задачи, и ещё внешний вид при этом опрятный.

Для верстальщика - когда у приложения все элементы едины в рамках одного проекта, когда можно переиспользовать те или иные части вёрстки, а то и вовсе руководствоваться стайлгайдом.

Для программиста - приложение с хорошо продуманной логикой, когда известны все сущности и зависимости между ними.

---


>Q2
>
>Опишите основные особенности разработки крупных многостраничных сайтов, функциональность которых может меняться в процессе реализации и поддержки.
>
>Расскажите о своем опыте работы над подобными сайтами: какие подходы, инструменты и технологии вы применяли на практике, с какими проблемами сталкивались и как их решали.

Для подобных проектов важно придерживаться единых стандартов внутри команды. Зачастую, крупные многостраничные сайты проектируются, утверждаются, и разрабатываются довольно долго. В редких случаях может смениться человек на той или иной позиции. Важно создать такую инфраструктуру, при которой изменение функциональности в процессе разработки не приведёт к ситуации "ааааа, всё перевёрстывать с нуляяяяя". Разработчикам надо использовать проверенные методики и инструменты, постараться не тестировать новый функционал на таком крупном проекте, без согласования руководства и других участников команды. Верстальщикам надо придерживаться именования классов, одного препроцессора, одной системы сборки, и т. д. Можно создать стайлгайд и пинать каждый раз дизайнеров, чтобы они тоже старались ему следовать, и, по-возможности, переиспользовали элементы.

Но это теория. На практике, бывают сложности. Бывали проблемы нехватки времени, когда нет возможности задокументировать код, отрефакторить, и, как следствие, другому разработчику было сложно вникнуть в происходящее. Проблема всегда индивидуально внутри каждой команды, должна решаться сообща.

Вообще, в моей бывшей команде я создал заготовку для вёрстки (аналог boilerplate, но конкретно под наши нужды) - это решало многие проблемы, которые бывали ранее.

---

>Q3
>
>При разработке интерфейсов с использованием компонентной архитектуры часто используются термины Presentational Сomponents и Сontainer Сomponents. Что означают данные термины? Зачем нужно такое разделение, какие у него есть плюсы и минусы?

Для меня работа с компонентами, пока ещё, в новинку. Эти термины, их плюсы и минусы, - это мне ещё предстоит изучить и понять на практике.

---

>Q4
>
>Как устроено наследование в JS? Расскажите о своем опыте реализации JS-наследования без использования фреймворков.

Классическое наследование - через прототип. Пару раз применял. Ещё в паре случаев пользовался $.extend. В веб-студии, где я работал ранее, делали сайты, и там js был "простой", без классов, наследования, и прочих изысков, которые нужны для js-приложений.

---

>Q5
>
>Какие библиотеки можно использовать для написания тестов end-to-end во фронтенде? Расскажите о своем опыте тестирования веб-приложений.

На данный момент, я знаком только с юнит-тестированием, и поверхностно - с интерфейсным. end-to-end, как я полагаю, посерьёзнее уже. Мне это предстоит изучить.

---

>Q6
>
>Вам нужно реализовать форму для отправки данных на сервер, состоящую из нескольких шагов. В вашем распоряжении дизайн формы и статичная верстка, в которой не показано, как форма должна работать в динамике. Подробного описания, как должны вести себя различные поля в зависимости от действий пользователя, в требованиях к проекту нет. Ваши действия?

Зависит от договорённостей внутри команды, на мой взгляд. Если эти договорённости позволяют некую свободу действий, и разработчик не лишён "чувства прекрасного" (в состоянии сам сделать приятные элементы интерфейса и анимации), то и незачем напрягать дизайнера. Я бы реализовал простой но опрятный внешне вариант (принцип 20\80), и показал его коллегам-дизайнерам, вместе обсудили бы, и, либо приняли, либо доработали.

---

>Q7
>
>Расскажите, какие инструменты помогают вам экономить время в процессе написания, проверки и отладки кода.

Линтеры (и для стилей, и для js), система сборки, валидаторы. Есть хороший сервис для проверки текстов - yaspeller. Для проверки js-кода мне сильно помогает система отладочных сообщений, которую я сам реализовал под свои нужды (используется в заготовке для вёрстки). Юнит-тесты. Хотя, на моём предыдущем месте работы, не закладывали время на их написание, и я пользовался ими редко. А подход TDD мне по душе. Было бы интересно с таким поработать. Ещё пользуюсь логгером js-ошибок Sentry.

---

>Q8
>
>Какие ресурсы вы используете для развития в профессиональной сфере? Приведите несколько конкретных примеров (сайты, блоги и так далее).
>
>Какие ещё области знаний, кроме тех, что непосредственно относятся к работе, вам интересны?

Хабр, Медиум, StackOverflow, Tproger, Toster.

Насчёт областей знаний... Если имеется ввиду айтишка, то, пожалуй, интересна тема информационной безопасности. Если имеется ввиду в целом, то у меня сразу несколько основных увлечений: бег, резьба по дереву, фото, походы/сплавы.

---

>Q9
>
>Расскажите нам немного о себе и предоставьте несколько ссылок на последние работы, выполненные вами.

Портфолио в процессе создания. Там будет описание, что сделал, и ссылки, где можно посмотреть/покликать. Как только будет готово, смогу предоставить. В качестве "утешения", вот моя статья на Медиуме: [https://designpub.ru/оптимизация-главной-страницы-сайта-дыши-48e242f2c4be](https://designpub.ru/оптимизация-главной-страницы-сайта-дыши-48e242f2c4be) - там можно прикинуть, насколько мне порой интересно заниматься проектом.

Прошу извинить за дерзость, но мне лень писать о себе. Мой профиль в ВК открыт и в нём можно многое обо мне узнать: [https://vk.com/timbilalov](https://vk.com/timbilalov)

---

## Level II

Всё приложение уместилось в три файла (не стал уж жестить и впихивать всё в один html файл).

* index.html
* styles.css
* scripts.js

Сделано с помощью vue.js, так как реакт ещё предстоит изучить.