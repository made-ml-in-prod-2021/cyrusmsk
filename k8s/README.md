# Homework 4

Открываем новое окружение:

```conda create --name hw4```

```conda activate hw4```

Используются результаты из Hw2 - из docker-hub скачивается image
```cyrusmsk/online_inference:v1```

Подготовка к работе в Windows (если использовать Google Cloud):
* Установить kubectl
* Установить Goodle Cloud SDK
* Прописать путь в переменную PATH

После этого можно выполнять команды _kubectl_ и _gcloud_.

Для проброски порта использовал команду из семинара ```kubectl port-forward pod/made-ml-hw4 8000:8000```

Поднятые Pod и результаты видны на скриншотах в папке.

Самооценка:
```
* Установил kubectl
* Развернул kubernetes в Google Cloud (https://cloud.google.com/kubernetes-engine) (5 баллов)
2) Написал просто манифест (online-inference-pod.yaml), на основе семинара (4 баллов)
2а) Добавил requests/limits (online-inference-pod-resources.yaml) (2 баллов)
9) Провел самооценку (1 - доп баллы)  

Итого: 12
```