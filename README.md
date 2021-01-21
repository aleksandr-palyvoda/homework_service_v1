### Запуск проекта
#### команда установки БД из helm, вместе с файлом values.yaml:
  helm install pg bitnami/postgresql -f db_values.yaml
#### команда запуска манифестов кубернетеса:
  kubectl apply -f secrets.yml -f configmaps.yml -f deployment.yaml -f service.yaml -f ingress.yaml
#### команда запуска тестов:
  newman run tests/aleksandr-palyvoda-tests.postman_collection.json