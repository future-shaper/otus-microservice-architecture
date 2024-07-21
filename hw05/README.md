## ДЗ №5 Prometheus. Grafana
##### На выходе должно быть:
0) скриншоты дашборды с графиками в момент стресс-тестирования сервиса. Например, после 5-10 минут нагрузки.
1) json-дашборды.

##### Команды для запуска
helm dependency build ./helm
helm install app ./helm
kubectl port-forward service/app-grafana 9001:80
##### JSON модель дашборда находится в файле 
./dashboard.json
##### Скриншот дашборда после тестирования в файле 
dashboard.png

