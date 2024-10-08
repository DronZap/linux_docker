# linux_docker
Создаем файлы Dockerfile и index.html и билдим образ
```
docker build .
```
Смотрим созданный образ 
```
docker images
```
![image](https://github.com/user-attachments/assets/7817612a-d037-411b-9780-f62c9b777430)

Запускаем контейнер
```
docker run -d -p 80:80 813
```
Смотрим работающие контейнеры
```
docker ps
```
![image](https://github.com/user-attachments/assets/8ca3c695-9536-48c3-95f7-9d7eeaeac739)

Проверяем, что nginx работает и отображает кастомную страницу

![image](https://github.com/user-attachments/assets/ac3e37bc-be0f-4d82-bbfc-21f44d291482)

Загружаем образ в docker hub
```
docker tag 813 dron23/dron23:nginx
docker push dron23/dron23:nginx
```
![image](https://github.com/user-attachments/assets/b539d411-e87e-4349-8c95-4887c5c65374)

Ссылка на doker hub:
https://hub.docker.com/r/dron23/dron23

2. Отличие образа от контейнера
   Контейнеры создаются из образов, образ - шаблон для создания контейнеров. Несколько контейнеров могут использовать один и тот же образ. Сам по себе Docker образ невозможно «запускать», запускаются контейнеры, внутри которых работает приложение.
3. Можно ли в контейнере собрать ядро?
В контейнере можно собрать ядро, например:
https://hub.docker.com/r/docker/for-desktop-kernel
