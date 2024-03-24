# Запуск

## 1. В папку 'wrapper_docker' склонировать backend

```
git clone git@github.com:Space-HR/hr-space-backend.git -b development_backend hr-space-backend 
```
или
```
git clone https://github.com/Space-HR/hr-space-backend.git -b develop hr-space-frontend
```

## 2. В папку 'wrapper_docker' склонировать frontend

```
git clone git@github.com:Space-HR/hr-space-frontend.git -b develop hr-space-frontend
```
или
```
git clone https://github.com/Space-HR/hr-space-frontend.git -b development_backend hr-space-backend 
```

## 3.  Скопируйте все из файла .env.example в файл .env и актуализируйте данные по необходимости

## 4. В папку 'wrapper_docker' запустить docker-compose.yml:

```
docker-compose up -d
```

## 5. Остановить:

```
docker-compose down
```
