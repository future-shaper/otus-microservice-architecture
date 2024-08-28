## Приложение оформление заказов

Приложение отвечает на порут 8002

### Сборка проекта:
````
mvn clean package
````

### Сборка docker images:
````shell
docker build -t futureshaper/hw-07-app-order-docker:dockerfile .
````

### Запуск docker образа:
````shell
docker run --name hw07-order -p 8002:8002 -e logging.level.root='DEBUG' -e spring.datasource.url='jdbc:postgresql://postgres:5432/postgres' -e application.account-url='http://host.docker.internal:8001' -e destinationSend='order-notice' -e destinationListener='notice-order' -e spring.artemis.broker-url='tcp://jms-broker:61616' --network=hw-networks -d futureshaper/hw-07-app-order-docker:dockerfile
````

### Проверка network:
````shell
docker network ls
````