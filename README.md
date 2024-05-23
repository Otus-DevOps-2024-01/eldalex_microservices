# eldalex_microservices
установили докер
Создали контейнер
запустили приложение внутри контейнера.
docker 3
раскидали один контейнер на несколько сервисов.
подняли их в пределах одной сети.
заставили работать и клепать посты.


Смена базового имени.
1 вариант:
docker-compose -p myproject up -d
2 вариант:
export COMPOSE_PROJECT_NAME=myproject
или прописать в .env проекта
после этого запускать как обычно.


initial root password gitlab
sudo docker exec -it <container_name> grep 'Password:' /etc/gitlab/initial_root_password
