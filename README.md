### Мастер-класс: (Reactive Messaging) Реактивный обмен сообщениями с Quarkus на OpenShift

**in-memory** для отправка сообщений через **MicroProfile** и **Vert.x Event Bus**

> Этот **workshop** семинар  также документирован в более удобной для чтения и навигации версии с использованием [GitBook](https://www.gitbook.com). Вы можете получить доступ к этой версии с помощью этой **[link](https://ibm-developer.gitbook.io/reactive-messaging-with-quarkus-on-openshift/)**.

На этом **workshop-e** вы узнаете, как реализовать функциональность реактивного обмена сообщениями с помощью Java, [Quarkus](https://quarkus.io/), [Kafka](https://kafka.apache.org/), [Vert.x](https://vertx.io/) и [MicroProfile](https://microprofile.io/). Сквозной образец приложения будет развернут в  [Red Hat OpenShift](https://www.openshift.com/).

Код доступен в виде открытого исходного кода в рамках проекта [Cloud Native Starter](https://github.com/IBM/cloud-native-starter/tree/master/reactive).

Одним из преимуществ реактивных моделей **reactive models** является возможность обновлять веб-приложения, отправляя сообщения, а не запрашивая обновления. Это более эффективно и улучшает взаимодействие с пользователем.

На **workshop-e** используется образец приложения для демонстрации реактивной функциональности **reactive functionality**. Простое приложение отображает ссылки на статьи и информацию об авторе.

Статьи можно создавать через REST API. Веб-приложение получает уведомление и добавляет новую статью на страницу. 
Анимация показывает, как выполняются запросы **curl requests** внизу, которые используя **trigger** запускают обновления веб-приложения вверху.

<kbd><img src="images/demo-1-video-small.gif" /></kbd>

Следующая диаграмма объясняет поток между различными компонентами и микросервисами.

Клиент API 'Submissions' запускает по triggers REST API 'Articles' service для создания новых статей. 
'Articles' service отправляет сообщение сервису 'Web-API' service через 'Kafka'. 
'Web-API' предоставляет конечную точку потоковой передачи **streaming endpoint**, которую использует веб-приложение 'Web-App'.

<kbd><img src="images/demo-1-small.png" /></kbd>

## Objectives

После завершения этого **workshop**а вы поймете следующие реактивные функции **reactive functionality**:
* Отправка и получение сообщений используя **Kafka messages** происходит через **MicroProfile**
* Отправка событий из микросервисов в веб-приложения через, **Server Sent Events**
* **in-memory** для отправка сообщений через **MicroProfile** и **Vert.x Event Bus**

Этот workshop для начинающих занимает один час.

* Целью этого workshop является не объяснение всех аспектов реактивного программирования, а объяснение core reactive principles и развертывание полного реактивного приложения, которое вы можете более подробно изучить после семинара. *


## Get Started

Это лабы, для этого **workshop**, пройдите их все по порядку, начните с **lab 1**:

* Lab 1: [Create your OpenShift Environment](labs/lab1.md)
* Lab 2: [Deploy Kafka via Script](labs/lab2.md)
* Lab 3: [Deploy Postgres via Operator](labs/lab3.md)
* Lab 4: [Deploy Sample Application](labs/lab4.md)
* Lab 5: [Reactive Messaging with MicroProfile](labs/lab5.md)
* Lab 6: [Server Sent Events](labs/lab6.md)
* Lab 7: [In-Memory Шина событий Vert.x Event Bus](labs/lab7.md)
* Lab 8 (optional): [Use distributed Logging](labs/lab8.md)

### Что изучить дальше

[Блоги от IBM Cloud](https://github.com/IBM/cloud-native-starter/tree/master/reactive#blogs), а также [презентация](images/ReactiveMicroservices.pdf) описывают функциональность более подробно.

Есть второй **workshop**, в котором используется тот же образец приложения. Этот **workshop** называется  [Reactive Endpoints with Quarkus on OpenShift](https://github.com/gridgentoo/workshop-quarkus-openshift-reactive-endpoints) и фокусируется на реактивных API и вызовах API.
