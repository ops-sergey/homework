Занятие 1. Введение в виртуализацию
Задача 1.
Ответ:
Done.

Задача 2.
Выберите один из вариантов платформы в зависимости от задачи. Здесь нет однозначно верного ответа так как все зависит от конкретных условий: финансирование, компетенции специалистов, удобство использования, надежность, требования ИБ и законодательства, фазы луны.
Тип платформы:
•	физические сервера;
•	паравиртуализация;
•	виртуализация уровня ОС;
Задачи:
•	высоконагруженная база данных MySql, критичная к отказу;
•	различные web-приложения;
•	Windows-системы для использования бухгалтерским отделом;
•	системы, выполняющие высокопроизводительные расчёты на GPU.
Объясните критерии выбора платформы в каждом случае.
Ответ:
1. Высоконагруженная база данных MySql, критичная к отказу:
Для высоконагруженных баз, критичных к отказу лучше выбирать отдельные физические сервера для обеспечения высокой производительности баз данных, а также отказоустойчивости и надёжности. Также, физические сервера подходят для возможного дальнейшего масштабирования серверов.
2. Различные Web-приложения:
Для web-приложении можно использовать паравиртуализацию или виртуализацию уровня ОС. Данные типы платформ полезна для задач с умеренной нагрузкой, где требуется более эффективное использование ресурсов сервера. Также, они позволяют запускать несколько изолированных сред разработки на одном физическом сервере.
3. Windows-системы для использования бухгалтерским отделом:
В данном случае наиболее подходящим вариантом будут паравиртуализация или виртуализация уровня ОС, т.к. данные виды платформ позволяют запускать несколько виртуальных Windows-систем на одном сервере, при этом обеспечивая изолированное окружение и безопасность данных бухгалтерского отдела.
4. Системы, выполняющие высокопроизводительные расчёты на GPU:
Для выполнения высокопроизводительных расчетов на GPU наиболее подходящей опцией будет использование физических серверов либо специализированных платформ для обработки вычислений на GPU.

Задача 3.
Выберите подходящую систему управления виртуализацией для предложенного сценария. Опишите ваш выбор.
Сценарии:
1.	100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based-инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.
2.	Требуется наиболее производительное бесплатное open source-решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.
3.	Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows-инфраструктуры.
4.	Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.
Ответ:
1. Если мы рассматриваем инфраструктуру, в которой уже есть 100 виртуальных машин, то лучше вариантом считаю использование продукта VMware vSphere. У данного продукта богатый функционал, поддержка различных операционных систем, включая Windows и Linux, интегрированные средства для реализации программных балансировщиков нагрузки, репликации данных и автоматизированного создания резервных копий.
2. Для данного случая подойдёт решение Proxmox VE. Данный продукт бесплатный, он обеспечивает виртуализацию Linux и Windows, поддерживает управление нагрузкой, репликацию данных и создание резервных копий. Proxmox VE также обладает высокой производительностью и широкими возможностями по совместимости с различными операционными системами.
3. Тут требуется решения для виртуализации исключительно Windows-серверов. В данном случае подойдет Hyper-V, который является встроенной системой виртуализации для Windows. Hyper-V предлагает высокую производительность, бесплатно для использования с Windows Server, и является максимально совместимым решением.
4. В данном случае подойдёт платформа виртуализации VirtualBox. Она бесплатна, совместима с различными дистрибутивами Linux и обладает удобным интерфейсом для тестирования программного обеспечения на виртуальных средах.

Задача 4.
Опишите возможные проблемы и недостатки гетерогенной среды виртуализации (использования нескольких систем управления виртуализацией одновременно) и что необходимо сделать для минимизации этих рисков и проблем. Если бы у вас был выбор, создавали бы вы гетерогенную среду или нет?
Ответ:
Всё зависит от требований и целей организации.
Недостатком данной среды виртуализации является:
- Сложность в управлении и обслуживании. У каждой системы свои собственные настройки параметров и интерфейсов, что затрудняет управление и мониторинг инфраструктуры.
- Совместимость и интероперабельность: различные системы виртуализации могут иметь ограничения в совместимости и взаимодействии друг с другом, что может привести к конфликтам и проблемам в работе.
- Уязвимости безопасности: наличие нескольких систем виртуализации может увеличить поверхность атаки и уязвимости, так как каждая из них имеет свои собственные уязвимости.
- Снижение производительности: работа в гетерогенной среде виртуализации может привести к нерациональному распределению ресурсов и, как следствие, к снижению производительности.
Для минимизации рисков и проблем в гетерогенной среде виртуализации необходимо:
1) Задокументировать и стандартизировать процессы управления и мониторинга для всех систем виртуализации.
2) Проводить тщательное тестирование совместимости и интероперабельности перед внедрением новых систем виртуализации.
3) Обеспечить безопасность путем регулярного обновления и мониторинга всех систем, а также использованием комплексных методов защиты.
4) Оптимизировать распределение ресурсов и настройки каждой системы виртуализации для максимальной производительности.
Если бы у меня был выбор, я бы склонялся к созданию гомогенной среды виртуализации, поскольку это облегчит управление, повысит совместимость и безопасность, а также улучшит производительность системы в целом.
