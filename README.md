# Etap 1


1. 
Aby zbudować obraz oraz przesłać go do repozytorium DockerHub należy wykorzystać polecenie ```docker buildx build -t docker.io/nikesz/lab5:etap1v1 --push .```.

Aby sprawdzić na jakie platformy dostępny jest ```docker manifest inspect -v docker.io/nikesz/lab5:etap1v1```.

2. 
Aby utworzyć i wybrać builder ze sterownikiem docker-container należy wykorzystać polecenia ```docker buildx create --name testbuilder``` i ```docker buildx use testbuilder```.

Aby zbudować obraz dla trzech wybranych architektur sprzętowych i przesłać go do repozytorium DockerHub należy wykorzystać polecenie ```docker buildx build -t docker.io/nikesz/lab5:etap1v2 --platform linux/amd64,linux/arm64,linux/s390x --push .```.

3. 
Aby sprawdzić czy zbudowany obraz wspiera wybrane architektury sprzętowe należy wykorzystać polecenie ```docker manifest inspect -v docker.io/nikesz/lab5:etap1v2```.

# Etap 2

3. 
Aby uruchomić aplikację należy wykorzystać polecenie ```docker compose up -d```.

Rezultat

# Etap 3

1. 
Aby zbudować obraz na wybrane architektury sprzętowe należy wykorzystać polecenie ```docker buildx bake -f docker-compose.yml --set *.platform=linux/amd64,linux/arm64 --set=*.output=type=image,name=docker.io/nikesz/lab5:etap3,push=true```.

Aby sprawdzić czy zbudowany obraz wspiera wybrane architektury sprzętowe należy wykorzystać polecenie ```docker manifest inspect -v docker.io/nikesz/lab5:etap3```.