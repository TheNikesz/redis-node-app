# Etap 1

1.

Aby zbudować obraz oraz przesłać go do repozytorium DockerHub należy wykorzystać polecenie ```docker buildx build -t docker.io/nikesz/lab5:etap1v1 --push .```.

![Etap1_01.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap1_01.png)

Aby sprawdzić na jakie platformy dostępny jest ```docker manifest inspect -v docker.io/nikesz/lab5:etap1v1```.

![Etap1_02.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap1_02.png)

2.

Aby utworzyć i wybrać builder ze sterownikiem docker-container należy wykorzystać polecenia ```docker buildx create --name testbuilder``` i ```docker buildx use testbuilder```.

Aby zbudować obraz dla trzech wybranych architektur sprzętowych i przesłać go do repozytorium DockerHub należy wykorzystać polecenie ```docker buildx build -t docker.io/nikesz/lab5:etap1v2 --platform linux/amd64,linux/arm64,linux/s390x --push .```.

![Etap1_03.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap1_03.png)
![Etap1_04.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap1_04.png)

3.

Aby sprawdzić czy zbudowany obraz wspiera wybrane architektury sprzętowe należy wykorzystać polecenie ```docker manifest inspect -v docker.io/nikesz/lab5:etap1v2```.

![Etap1_05.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap1_05.png)
![Etap1_06.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap1_06.png)
![Etap1_07.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap1_07.png)

# Etap 2

3.

Aby uruchomić aplikację należy wykorzystać polecenie ```docker compose up -d```.

![Etap2_01.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap2_01.png)

Rezultat

![Etap2_02.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap2_02.png)

# Etap 3

1.

Aby zbudować obraz na wybrane architektury sprzętowe należy wykorzystać polecenie ```docker buildx bake -f docker-compose.yml --set *.platform=linux/amd64,linux/arm64 --set=*.output=type=image,name=docker.io/nikesz/lab5:etap3,push=true```.

![Etap3_01.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap3_01.png)

Aby sprawdzić czy zbudowany obraz wspiera wybrane architektury sprzętowe należy wykorzystać polecenie ```docker manifest inspect -v docker.io/nikesz/lab5:etap3```.

![Etap3_02.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap3_02.png)
![Etap3_03.png](https://github.com/TheNikesz/redis-node-app/blob/main/Screens/Etap3_03.png)
