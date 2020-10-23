Navigator:
* [Workshop Description](https://ibm.github.io/workshop-quarkus-openshift-reactive-messaging/)
* Lab 1: [Create your Cloud Environment](lab1.md)
* Lab 2: Deploy Kafka via Script
* Lab 3: [Deploy Postgres via Operator](lab3.md)
* Lab 4: [Deploy Sample Application](lab4.md)
* Lab 5: [Reactive Messaging with MicroProfile](lab5.md)
* Lab 6: [Server Sent Events](lab6.md)
* Lab 7: [Vert.x Event Bus](lab7.md)
* Lab 8 (optional): [Use distributed Logging](lab8.md)

---

# Lab 1: Deploy Kafka via Script

В этой короткой лабораторной работе вы развернете Kafka с помощью скрипта.

### Step 1: Deploy Kafka

Вызовите следующую команду:

```
$ ~/cloud-native-starter/reactive/os4-scripts/deploy-kafka-oc-only.sh 
```

В результате вы увидите это:

![kafka deployment](../images/kafka-deployment.png)


### Step 2: Verify the Installation 

На запуск всех Подов уходит пара минут. Вы можете проверить статус через **OpenShift web console**. На странице **'Pods'** выберите проект **'kafka'**.

![kafka deployment](../images/kafka-deployment2.png)

---

__Продолжить с [Lab 3: Deploy Postgres via Operator](lab3.md)__
