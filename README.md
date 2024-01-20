# Работу выполнила студентка Цепилова Серафима
# Развертывание веб-приложения в Kubernetes с использованием Minikube

## Подготовка окружения
Для начала мы установили Minikube и Docker, чтобы иметь возможность создать локальный кластер Kubernetes и собрать Docker image веб-приложения.
## Запуск Minikube
Затем мы запустили Minikube, указав, что хотим использовать его в качестве драйвера для создания локального кластера Kubernetes.
## Сборка Docker Image
Далее, мы собрали и проверили работу Docker image. Также залили на docker hub
https://hub.docker.com/repository/docker/simatsepilova/kuber_nx_home/general
```
docker build -t simatsepilova/kuber_nx_home:1.0.0 .
docker run -p 8000:8000 simatsepilova/kuber_nx_home:1.0.0
docker push simatsepilova/kuber_nx_home:1.0.0
```
## Пишем деплоймент (web-deployment.yaml в репе) и вносим изменения и проверяем работу (PNG со скрином в репе)
```
kubectl apply -f web-deployment.yaml
kubectl describe deployment web
```
