# Выполнение работы
Для лабараторной работы используем Docker для Windows с WSL.

- Создаем две папки для наших контейнеров:

/d/Repositories/lab4/container-1
/d/Repositories/lab4/container-2

- Создаем наш докерфайл и прописываем в него:
  <img width="881" height="509" alt="image" src="https://github.com/user-attachments/assets/b9ab14f1-f7b7-4342-ba37-f6b4a6b28ef7" />
-  Копируем
 cp Dockerfile ../container-2
- Проверяем работу контейнеров:

docker build -t container-1 .
dcoker run -it --name con1 container-1

<img width="1020" height="599" alt="image" src="https://github.com/user-attachments/assets/5487d64c-ed66-4fdd-9336-e98b4a32c599" />
- Создаем нашу сеть и присоединяем контейнеры:

docker network create myNet
docker network connect myNet con1
docker network connect myNet con2

<img width="561" height="329" alt="image" src="https://github.com/user-attachments/assets/4039cb15-57cf-429c-9ecf-ad3ce77bcbbf" />
<img width="560" height="331" alt="image" src="https://github.com/user-attachments/assets/ab27f138-a18f-4722-b855-3cba407cbe26" />
<img width="550" height="280" alt="image" src="https://github.com/user-attachments/assets/3091f54b-c9e2-431e-8d73-03615af97b10" />
