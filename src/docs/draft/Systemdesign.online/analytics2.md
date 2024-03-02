## История для затравки - сложные информационные системы делать сложно

	{СЛАЙД про большую системы и сложности её создания}
### Представьте, что вам нужно сделать большую систему для большой организации
Системы из моего опыта - 
- Система управления документооборотом в министерстве ...
- Система управления правами доступа сотрудников в организации на несколько десятков тысяч человек... 
- Система управления оборудованием большого бизнес-центра или жилого здания на несколько тысяч жителей...
- Система автоматизации продаж цифровых и не только продуктов, от разных поставщиков...

В команде - несколько десятков человек разных специальностей. 
Среди заказчиков - тоже много разных интересантов. Как привести проект к успеху?

### Водопад vs гибких итерационных подходов = Предсказуемо, но долго vs Быстрое начало но полная непредсказуемость потом
В прошлом веке активно применялся подход "водопад" - последовательное, поэтапное проектирование и последующее воплощение всей системы целиком. Это круто, но уж очень долго ждать результата.

	Водопад - старое унылое Г
	Так давно уже никто не делает
	
Поклонники современных гибких подходов говорят - надо начинать с малого и постепенно/итеративно наращивать функциональность. 

	Архитектура - для трусов
	Начнем с малого, потом доделаем. 

Это и правда работает для относительно небольших систем и продуктов. С большими системами тоже работает, но там все не так просто - возникает масса вопросов,  на которые никто не хочет отвечать, и сложностей, которые непонятно как решать.
	
	Требований таких не было. Теперь все надо переделывать. Приходите через год.
	
### Ключевые вопросы и сложности
Главные вопросы, которые возникают между командой и заказчиком
- что такое это малое, с чего можно начать? 
- что делать дальше?
- когда и что будет готово?


> Частая картина, что сделали это самое малое, все на него посмотрели, кивнули и команда довольная едет дальше. А потом вдруг кто-то приходит и говорит "упс" и оказывается, что все, что делали полгода -  это не то что нужно. Из моей практики - делали новую версию системы документооборота. Делали примерно год. Получилось стильно, красиво, технически продвинуто, только неприменимо - там отсутствовали важные, но неочевидные функции с точки зрения практической работы. И еще полтора года систему дорабатывали, чтобы можно было её реально использовать.

Главный технический риск - решения, которые принимаются на ранних этапах в условиях отсутствия информации, могут принести проблемы на последующих шагах. Именно на борьбу с этим риском был нацелен водопад - сначала пройти до конца, а потом уже принимать важные решения. 
Никогда такого не было - и вот опять. Система упирается в архитектурные ограничения, которые не позволяют обрабатывать больше, быстрее и т.п.

> 
> Отчасти поэтому на больших системах выживают микросервисные архитектуры. Они не очень-то производительны сами по себе, зато масштабируемость в них заложена "генетически". Главное их преимущество, которое гарантирует выживаемость - это то, что замена и переделка одного-двух микросервисов не требует переделки всей системы. Это если вы "правильно" разбили на контексты и сервисы. 
> 
> Именно про это говорит DDD, но тут подстава в том, что подход призван решать проблемы во-первых, сильно до их возникновения, а во-вторых, при его применении те проблемы, который он призван решать, просто не возникают. Но это не значит, что не будет других проблем :)
> Поэтому (как и с многими другими методологиями превентивного характера) у тех, кто не столкнулся непосредственно с проблемами, которые предотвращает DDD, может возникнуть ощущение, что DDD - это нудная заумь, придуманная непонятно зачем, которая создает сложности здесь и сейчас (например дублирование кода при разделении моделей по контекстам) ради решения гипотетических будущих проблем, которых никто не видел и которые еще может быть не возникнут....
> 
> Эволюционно такая модель более устойчива в условиях меняющегося мира, чем большие динозавры, которые не смогли пережить ледниковый период.
## Тема для разговора: подход к организации работ по созданию сложных систем
### Почему я считаю это важным... 
Хорошие программы  хорошо подходят к окружающему миру. Программа не возникает сразу, её изготавливают постепенно. Изготовление требует времени и ресурсов. При создании больших и сложных систем каждый делает свой маленький кусочек. Эффективная работы команды без хорошего информационного обмена невозможна. Т.е. каждый по отдельности может вкладываться изо всех сил, индивидуальные метрики зашкаливают, джира ломится от закрытых тасков, а толку чуть...

Большую систему не может сделать один человек. Чем больше система - тем больше народу нужно. Каждый делает свою часть работы для того, чтобы изменения произошли. Архитектор проектирует, программист - пишет код, тестировщик его проверяет, аналитик - анализирует, инженеры что-то разворачивают и настраивают... 
И как-то все это складывается в общий результат... каждый раз воспринимаю это как чудо :)  
### Почему я про это рассказываю
Я в ИТ с 1996 года. Я писал и на С, и на Питоне. Был фулстек-разработчиком (тогда это называлось просто "программист"), руководителем проектов, архитектором и менеджером продукта. Пару раз чуть не стал руководителем отдела системного анализа :) Работал в продуктовых командах и больших интеграционных проектах.
Я каждый раз подходил к задаче создания продукта или решения в разных ролях, но хорошо помнил при этом, как устроена жизнь в "другом домене". Поэтому старался учитывать интересы разных сторон и в итоге у меня сложился комплекс взаимосвязанных практик, целостный подход к организации работ по созданию таких систем.

Это, безусловно, не единственно-правильный подход, у него масса ограничений (в частности, он требует вовлеченности и осознанности на всех ключевых ролях, чего довольно трудно добиться). 
Но этот тот способ, который мне понятен и кажется, это работает, хотя для неподготовленного зрителя  местами может показаться сложным. 

Сегодня я акцентируюсь на той части этого подхода, которая касается аналитиков

## Информационные системы - это способ изменения мира

Сначала давайте подумаем, а зачем мы с вами делаем информационные системы?
Смысл всякой деятельности лежит вне её пределов» — **это притча от Владимира Тарасова**.
«Цель любой деятельности лежит за пределами этой деятельности» [Радислав Гандапас](https://mybook.ru/author/radislav-gandapas/ "⭐️Радислав Гандапас")

Цель проектной/продуктовой **команды** - не создание ПО или продукта, а, не побоюсь этих громких слов - изменение мира путем создания и запуска продукта. Программное обеспечение - это лишь средство, инструмент этого изменений. Если продукт создан, система запущена, а изменения не произошли - цель не достигнута.

> [!hint]
> Магазины наводнили поддельные елочные игрушки. Они выглядят как настоящие, только радости от них никакой - иллюстрация к тезису, про необходимость достижения внешней цели.

### У разных стейкхолдеров - разные интересы
Давайте коротко пробежимся по процессу создания информационной системы. Вот, к примеру, я недавно занимался проектированием системы, автоматизирующей процесс заказа доставки товаров при покупке.

С одной стороны, есть бизнес-заказчики, которые говорят что примерно хотят. И, конечно, они хотят сразу все - клиент выбирает любой товар, выбирает как его доставить и ему кто-то как-то его доставляет - магия работает. Как это будет работать и за счет чего - их не очень волнует.

С другой стороны - есть менеджеры проекта. Они спрашивают - когда и что будет готово. При этом их тоже не очень интересует как именно, их интересует что и когда (иногда еще - сколько это стоит)

Есть архитекторы и разработчики. Они спрашивают - что надо делать-то? И еще покритиковать любят, "а почему именно так?". 

И это "что" для разработчиков - оно совсем не такое, как для бизнеса. 
- В первом случае мы говорим "Клиент нажимает кнопку и получает список магазинов, где он сможет забрать прямо сейчас". 
- Программисту фронта мы говорим, сделай формочку, которая по нажатию на кнопочку дернет вот этот API и выведет содержимое на экран. 
- Программисту бэка - сделать такой метод в API, который будет делать вот такой запрос в базу. 
- А еще троим программистам других сервисов - еще какие-то задачи, чтобы данные в БД сформировались правильным образом.

Как это все увязывается и синхронизируется между собой?

## Системная модель проекта и виды представлений

### Уровни рассмотрения системы 
- Уровень надсистемы - что происходит в окружении, какую проблему решаем, как планируем решать
- Система в надсистеме - система, её заинтересованные стороны, пользователи, входы и выходы
- Архитектура системы - структура системы, из чего состоит, как увязана
	- Функциональная структура
	- Композитная структура
- Уровень проекта - задачи, изменения

### Аналитика - искусство разделения на части в процессе познания
Анали́тика (др.-греч. άναλυτικά, букв. — «искусство анализа») — часть искусства рассуждения — логики, рассматривающая учение об анализе — операции мысленного или реального расчленения целого (вещи, свойства, процесса или отношения между предметами) на составные части, выполняемая в процессе познания или предметно-практической деятельности человека.
[Аналитика — Википедия (wikipedia.org)](https://ru.wikipedia.org/wiki/%D0%90%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0)

Аналитик - это специально обученный человек, который владеет навыками видеть, выявлять в окружающей его (или планируемой, воображаемой) действительности определенные типы структур и умеет описывать, оформлять эти структуры в определенных нотациях. 

### Аналитические описания - это основа эффективных коммуникаций  
И вот тут мы плавно приходим к тому, какую задачу решает аналитик в команде и как именно он это делает. Аналитик, как человек со структурным взглядом, способен описать с помощью подходящих нотаций, фактически - сделать модель,  формально и строго описать все нужные представления и связать их в единую связанную систему. 

{тут нужна картинка с трассировкой от запросов бизнеса до задач, элементов структуры, функций и объектов данных + рядом диаграмму импакт маппинга}

Эти описания помогают договариваться, благодаря им:
- Заказчики/Бизнес понимают, что ожидается, какие изменения произойдут
- Архитектор понимает, какие потребности бизнеса нужно решить, может подбирать подходящие решения и формулировать задачи на изменения в ПО и ландшафте
- Разработчики понимают, какие задачи им нужно делать и как эти задачи связаны с планируемыми изменениями.
- Менеджер, благодаря связи задач и планируемых изменений, может прогнозировать сроки и приоритезировать задачи
- 
## Разберем эти модели более подробно
У меня нет цели сделать исчерпывающий рассказ про все виды моделей/нотаций. Расскажу про те, которые использовал и от которых видел реальную пользу.
### Моделирование ожидаемого изменения

#### UseCases - точки соприкосновения системы с окружающим миром
Цель моделирования - выявить точки контакта разрабатываемой системы с окружающей действительностью, которые мы планируем реализовать/изменить. К примеру, сейчас житель, заезжая на парковку, выходит из машины, идет к охране, показывает свой паспорт с пропиской и ему открывают шлагбаум.
Мы хотим сделать так, чтобы шлагбаум открывался автоматически, если в машине есть пропуск.
Неопытный аналитик нарисует один UseCase - Машина с пропуском внутри проезжает через шлагбаум.
Опытный задумается - а откуда пропуск взялся в машине. Появится useCase "Выдача пропуска". Тут стоит задуматься о восстановлении пропуска при утере, а также про отзыв пропуска. На горизонте замаячили пропуска для гостей..., сценарии для VIP клиентов - загорается приветственная запись.
И вот мы уже можем договариваться с бизнесом/продакт-owner-ом о границах MVP.
В идеале - каждый кейс связан с потребностью, интересом какого-то стейкхолдера.
Границы одной диаграммы определяют полезность содержательного инкремента. На одной диаграмме должен помещаться полезный бизнес-кейс целиком. На этой диаграмме должны быть видны точки касания с системой  ключевых заинтересованных лиц, причем не только те, которые на поверхности, но и не всегда очевидные - например, тут могут быть кейсы, порождаемые нормативными актами, отчеты для бухгалтерии и т.п. Не все кейсы попадут в MVP, но понимание, что они понадобятся - оказывает сильное влияние на архитектуру.
#### UserStory - полезные инкременты/приращения системы
UseCase на этих диаграммах не содержит деталей, это количественное, а не качественное описание скоупа, он моделирует факт контакта, но не говорит о том, как именно происходит контакт предполагаемой системы с окружением. Для моделирования деталей, а также планирования постепенного усложнения системы мне нравится использовать User Story Map.
Границы одной карты совпадают с границами UseCase диаграммы, колонки - юзкейсы, а карточки - отдельные UserStories. Карточки составляют бэклог, а строчки позволяют моделировать инкременты. Это - предмет обсуждения и переговоров между менеджерами, бизнесом и разработкой. Оценки тут пока очень приблизительные, но уже позволяют делать грубое, приблизительное планирование.
Одна Story - это полезное изменение, улучшение одного UseCase.
Одна строка StoryMap - это осмысленный инкремент, состоящий из набора историй, которые вместе создают качественное улучшение бизнес-кейса. Ну, или количественное, когда мы реализуем первые истории.
{тут нужен пример стори мапа}


### Моделирование ожидаемого поведения
#### Информационные потоки и интерфейсы взаимодействия
И вот мы уже как никогда близки к формулированию требований к системе. Мы определили ситуации контакта внешнего мира с системой, примерно обрисовали, что там должно происходить, пора посмотреть на то, как это влияет на саму систему.
Вот тут я предлагаю моделировать информационную систему как насос. Т.е. это такой черный ящик, в который информация через какие-то отверстия/каналы/интерфейсы попадает, там внутри эта информация как-то переваривается/преобразуется/накапливается, а потом через другие интерфейсы(UI/сообщения/события/вызовы) выводится внешним потребителям.
Модель информационных потоков позволяет идентифицировать точки/интерфейсы на теле информационной системы, необходимые для реализации кейсов/историй, и даже слегка прикоснуться к её анатомии - понять какие функции внутри системы должны возникнуть, чтобы кейсы могли быть реализованы. Мы уже понимаем не только какие кейсы/сценарии должны быть реализованы - мы уже можем обсуждать какие функции должна реализовывать наша система (пока не очень понимая как именно).

Для такого моделирования я использую что-то вроде Activity Diagram, с портами для ввода/вывода информации и внутренними Activity для выявления функций. Можно использовать EventStorming нотацию (да и сам процесс), фактически это то же самое, только информационные потоки представляются в виде потоков событий.

Эта диаграмма позволяется нам явно перечислить:
- Интерфейсы, осязаемые точки информационного обмена нашей системы с внешним миром
- Входные/выходные потоки данных
- Функции системы, необходимые для реализации наших кейсов/историй
- Трассировку/связь функций с кейсами 

#### Моделирование бизнес-процессов как альтернативный подход
Иногда удобно моделировать не систему целиком, а путь, который проходит информация или клиент, взаимодействуя с системой, пошаговый процесс обработки запроса.
Внешне Business Process Diagram и Activity Diagram очень похожи, но они моделируют разные вещи. Покажу разницу на примере гамбургера
Бизнес процесс приготовления гамбургера:
- Заказ -> сборка -> ожидание -> получение
Activity Diagram кухни изготавливающей гамбургеры
- Прием заказов
- Жарка котлет
- ну и т.п.

#### Моделирование предметной области
Итак, мы уже определились примерно с тем, что именно нам нужно сделать. Пора приступать к детальному дизайну "точек информационного обмена": форм, API, схем БД и т.п. И тут нас часто ждет засада, что понятные, казалось бы слова пока мы говорим "в общем" оказываются очень скользкими и неподатливыми, когда мы начинаем говорить "конкретно".

> [!example] Пример из практики. 
> Вот есть понятное всем слово подъезд. На входе в подъезд есть кодовый замок. Сделали такую удобную фичу - когда житель входит в подъезд по карточке, то к нему приезжает лифт и сразу везет его на нужный этаж. Модель понятная. У подъезда есть лифтовая группа, при проходе считывается номер карты, и отправляется команда соответствующей лифтовой группе. Реализовано все было на уровне контроллера. Но вот в одном здании оказалось, что есть один вход (подъезд) на две СЕКЦИИ здания, в каждой из которых свой лифт. Заложенная в контроллер модель "Подъезд ИМЕЕТ одну лифтовую группу" оказалась неверна. 

Чтобы корректно и непротиворечиво описывать требования к интерфейсам и функциям (=правилам) обработки информации, нам нужно эту информацию смоделировать, тогда мы получим набор понятий, позволяющих явно и непротиворечиво описывать то, что происходит в предметной области и что мы с этим собираемся делать.

Я сторонник DDD подхода, когда драйвером для таких моделей является терминология и понятия автоматизируемой предметной области. Способ моделирования - это своего рода глоссарий терминов и сущностей, их атрибутов и связей между ними. Дальше эти слова используются в проектировании схем данных, прототипов API, интерфейсов.

	{СЛАЙД: Диаграмма сущностей на Plantuml}

Инструментально я довольно долго использовал для такого моделирования PlantUML, но ему не хватает удобства моделера. Был опыт моделирования в Archimate. там неплохо удается моделировать сущности и отношения, но нет возможности моделировать атрибуты. В текущем проекте в основе всех коммуникаций лежит GraphQL, так что мы используем GQL-схему сразу для моделирования сущностей. При необходимости это описание достаточно легко конвертировать в другие форматы, я, в частности, писал генераторы Go-моделей, JSON схем и даже PlantUML диаграмм, чтобы вставлять их в документацию.

	{СЛАЙД: Диаграмма сущностей на GraphQL + картинка}

Но там тоже не всегда удобно получается именно в части моделирования, всё таки это это не инструмент моделирования (когда ты не знаешь сразу, что тебе нужно и ищешь, экспериментируешь, приближаясь к цели), а описания уже известной и понятной модели. Не хватает инструментария рефакторинга.

Модель предметной области - задает DSL, в терминах которого описываются контракты API, требования к формам и функциям.  используют термины DSL. При изменении модели мира, очевидно, придется менять использующие затронутые термины функции и контракты системы. Вот для того и придуманы ограниченные контексты и изоляция, чтобы такие изменения не расползались по всей системе.
{Картинка - набор доменов из ИЗ} 

Слова из DSL используются для обозначения сущностей во всех представлениях - Схемах БД, событиях, API и т.п., чтобы подчеркнуть, что это одно и то же понятие.

	{СЛАЙД: Кусочек модели и воплощение модели в схеме БД, названиях API, событиях}
	{+привести пример, когда одно и то же понятие называется по разному в разных местах)

В микросервисной архитектуре принято изолировать контексты между собой путем разделения на сервисы. Т.е. границы контекстов проходят между сервисами, т.е. если мы тронем модель, то зацепим только связанные по этой части моделей сервисы. Но даже если вы не делаете микросервисы, то делить по контекстам все равно нужно - пусть это будут модули, пакеты, компоненты или что там еще.

### Непрерывное развитие

Вот мы и подобрались к самому интересному. Как же обеспечить предсказуемость, сравнимую с водопадом, с гибкостью и скоростью адаптаций? С помощью тонкого баланса между понятными и непонятными вещами.
{Иллюстрация с иллюзорным островом в океане и ближайшей кочкой, на которую мы прыгаем}

	{СЛАЙД: процесс создания MVP - от идеи через кейсы,StoryMap и Backlog }
	При этом указываем накопленные в процессе артефакты/модели
	
На начальном этапе, когда продукта, решения, системы еще нет, мы тратим определенное количество времени на то, чтобы выявить точки касания - UseCase-ы системы. Не надо гнаться за глубиной проработки, важно их явно перечислить и принять решение - делаем/не делаем сейчас/ не делаем вообще. Не нужно пытаться все юзкейсы вставить на одну диаграмму, нужно их раскидывать, группировать в полезные бизнес-кейсы - так сформируются относительно независимые субдомены, которые можно будет поставлять по отдельности.
Собрали, договорились об MVP - отлично, запустили процесс Story Mapping для проработки глубины и этапности реализации каждого кейса с учетом трудоемкости. Сделали - отлично, можно запускать в работу. НФТ и общее концептуальное архитектурное решение уже можно начинать прорабатывать параллельно, после того как перечислены юзкейсы. Детали реализации зависят от того, как разложится карта историй.


Итак, работы по MVP запустили. Что дальше? А дальше у нас в каждый момент времени есть модель юзкейсов, карта историй (=бэклог задач, сгруппированный в набор полезных инкрементов), модель предметной области и функциональная модель системы. 
У нас могут быть инкременты вида:
- Включить в систему новые юзкейсы
	- Проводим работы по планированию историй -> задачи в бэклог
	- Дальше спокойно планируем полезные инкременты из задач в бэклоге
- Реализация полезных инкрементов
	- Моделирование изменений предметной области
	- Моделирование изменений функциональной модели
		- Уже на этом этапе мы можем увидеть, есть ли уже нужные нам функции, можно ли имеющиеся функции чуть-чуть подтюнить, или речь идет о создании принципиально новых возможностей.
	- Моделирование соответствующих архитектурных/технических изменений => Задачи в разработку
		- Качественные изменения - придание системе принципиально новых качеств (функций или качественное изменение НФТ) за счет новых компонентов или архитектурных решений (новые сервисы, новые сущности, новые функции). 
			- Стоят качественно дороже
			- Выполняются долго
			- Несут риски
		- Количественные изменения - наращивание функциональности, удобства за счет развития существующих компонентов - Добавить атрибуты имеющимся сущностям, уточнить/скорректировать имеющиеся бизнес-правила, добавить улучшения на фронте без изменения бизнес-модели.
			- Выполняются за предсказуемые сроки/ресурсы
			- Несут меньше рисков (тут они тоже бывают, но маловероятны)
---

	{СЛАЙД: Большая функциональная модель активностей, артефактов и ролей}
	Как и за счет каких активностей возникают и реализуются новые инкременты

Этот процесс (или правильнее сказать деятельность?) не столько итеративный (хотя разработку понятных инкрементов вполне можно организовать именно итеративно), сколько непрерывно эволюционный. 

Активности, связанные с моделями могут выполнять разные люди, я тут обозначил по цвету где, на мой взгляд, больше аналитическая работа (где требуется общие знания по информационным системам, навыки системного анализа), а где архитектурная (в том  смысле, что ближе к технике и требует соответствующих навыков, знаний и опыта). В общем-то, все эти активности может выполнять и архитектор, и аналитик, и даже разработчик. Это все может делать один человек, тогда такие или похожие модели будут возникать, просто они будут неформальные, нечеткие и жить в одной голове :), и этот процесс будет крайне трудно масштабировать. Выведение моделей из тени в реальные артефакты/документы даёт возможность масштабировать процесс создания сложных частей за счет разделения активностей по типам и, например, по субдоменам, назначения их разным исполнителям.

На каждой части этой производственной системы свои ручки/регулировки для управления направлением развития системы 
- идти широким фронтом по всем юзкейсам или вкладываться в детальные развития определенных областей. 
- Сколько ресурсов пустить на инвестиции в придание новых качеств и функций, которые позволят системе/продукту развиваться линейно и предсказуемо 
- 
Но это всё уже другая история, больше интересная менеджерам.


В заключение
  - Краткий обзор рассмотренных видов моделей и связей между ними
  - Роль прослеживаемости и трассировки изменений

