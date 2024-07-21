## ДЗ №3  Основы работы с Kubernetes (Часть 2)

##### Использовать nginx ingress контроллер, установленный через хелм, а не встроенный в миникубик:
kubectl create namespace m && helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx/ && helm repo update && helm install nginx ingress-nginx/ingress-nginx --namespace m -f nginx-ingress.yaml
##### Манифесты должны лежать в одной директории. Применяем их командой 
kubectl apply -f .
##### Проверяем в доступность в браузере
http://arch.homework/health либо http://arch.homework/otusapp/student_name/health
