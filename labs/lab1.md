Navigator:
* [Workshop Description](https://ibm.github.io/workshop-quarkus-openshift-reactive-messaging/)
* Lab 1: Create your Work Environment
* Lab 2: [Deploy Kafka via Script](lab2.md)
* Lab 3: [Deploy Postgres via Operator](lab3.md)
* Lab 4: [Deploy Sample Application](lab4.md)
* Lab 5: [Reactive Messaging with MicroProfile](lab5.md)
* Lab 6: [Server Sent Events](lab6.md)
* Lab 7: [Vert.x Event Bus](lab7.md)
* Lab 8 (optional): [Use distributed Logging](lab8.md)

---

# Lab 1: Создайте свою Work Environment

Основные инструкции этого семинара предполагают, что вы будете использовать **Red Hat OpenShift 4.3** в **IBM Cloud**. Однако вы также можете использовать [CodeReady Containers](https://github.com/code-ready/crc) для локального запуска OpenShift.

Для использования **OpenShift** в **IBM Cloud** и **LogDNA** в лабораторной работе 8, требуется [IBM Cloud account](http://ibm.biz/nheidloff). Это бесплатно, не имеет срока действия, а для облегченной учетной записи кредитная карта не требуется.

На этом практическом семинаре мы будем использовать предварительно настроенный [OpenShift в IBM Cloud](https://cloud.ibm.com/kubernetes/catalog/openshiftcluster). Вы должны были получить информацию от своего лабораторного инструктора, чтобы получить доступ к одному из этих кластеров.

### Step 1: Set up Terminal

При использовании OpenShift в IBM Cloud для этого семинара настройка на стороне клиента не требуется. Вместо этого мы будем использовать **IBM Cloud Shell** (бета), который поставляется со всеми необходимыми интерфейсами командной строки CLIs (command line tools).

В своем браузере войдите в панель управления [IBM Cloud](https://cloud.ibm.com). Убедитесь, что вы выбрали свою учетную запись в списке учетных записей вверху **account list**, а затем щелкните значок **IBM Cloud Shell**.

![](../images/cloud-shell-launch.png)

Примечание. Ваше **workspace** включает 500 МБ **temporary storage**. Ваш сеанс закрывается через 30 минут бездействия. Если вы не используете Cloud Shell более часа, данные вашей рабочей области удаляются. Он также удаляется при достижении 4-часового непрерывного или 30-hour weekly usage limits.

Вот что вы должны увидеть:

![](../images/cloud-shell.png)

При локальном использовании **OpenShift** вам понадобится локальный терминал и следующие инструменты:

* [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [curl](https://curl.haxx.se/download.html)
* [oc](https://docs.openshift.com/container-platform/4.3/welcome/index.html)
* [mvn](https://maven.apache.org/ref/3.6.3/maven-embedder/cli.html)
* Java 9 or higher

### Step 2: Get the Code

В **IBM Cloud Shell** выполните следующую команду:

```
$ git clone https://github.com/IBM/cloud-native-starter.git
```

![](../images/cloud-shell-clone.png)

### Step 3. Get Access to OpenShift

Откройте [IBM Cloud Dashboard](https://cloud.ibm.com). В строке вверху переключитесь с вашей **own** account, учетной записи на **IBM account**, предоставленную вам инструктором из раскрывающегося списка в правом верхнем углу.

Выберите **'OpenShift'** в меню **burger menu** в верхнем левом углу, а затем **'Clusters'**.

![Select Open Shift in the menu](../images/openshift-console-launch1.png)

Кликните свой кластер.

![C](../images/openshift-console-launch2.png)

Open the OpenShift web console.

![Open the OpenShift web console](../images/openshift-console-launch3.png)

From the dropdown menu in the upper right of the page, click 'Copy Login Command'. 

![Key](../images/openshift-login1.png)

Click on 'Display Token', then copy and paste the command 'Log in with this token' into your terminal in the IBM Cloud Shell.

![Key](../images/openshift-login2.png)

Login to OpenShift in IBM Cloud Shell

```
$ oc login https://c1XX-XX-X.containers.cloud.ibm.com:XXXXX --token=xxxxxx'
```

![oc login in cloudshell](../images/openshift-login3.png)

---

__Continue with [Lab 2: Deploy Kafka via Script](lab2.md)__
