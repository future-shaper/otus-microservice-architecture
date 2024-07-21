ДЗ №2 Приложение в docker-образ и запушить его на Dockerhub

1. Прописываем в C:\Windows\System32\drivers\etc\hosts 127.0.0.1 arh.homework
2. Перезагружаем компьютер и проверяем ping arch.homework Если ок, то шаг 3
3. Создаем образ docker локально docker build --platform linux/amd64 -t hw02 .
4. Запускаем контейнер локально docker run -p 8000:80 hw02 Проверяем доступность в браузере. Если ок, то шаг 5
5. Присваиваем тег образу docker tag hw02 futureshaper/microservice-architecture-homeworks:hw02
6. Отправляем образ в docer hub    docker push futureshaper/microservice-architecture-homeworks:hw02
7. Запускаем образ из docer hub    docker run -p 8000:80 futureshaper/microservice-architecture-homeworks:hw02
8. Проверяем в браузере доступность http://arch.homework:8000/health

![img_1.png](img_1.png)
    
   
   
