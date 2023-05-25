# Dockerize Nginx

Repositori ini berisikan, Dockerfile yang akan digunakan untuk membuild nginx sebagai web server dari ubuntu 18 di dalam image docker.

Jika ingin menjalankan atau melihat hasil buildnya silahkan kunjungi repositori dockerhub disini - https://hub.docker.com/repository/docker/druzxh/nginx/general

## How to build

```bash
# Build
docker build -t nginx:1.0 .

# Jika Docker filenya ada di folder lain gunakan path
docker build -t nginx /path/to/folder

# List image yang telah dibuild
docker images

# Test / jalankan dockernya
docker run -d -p 9090:80 --name webserver nginx:1.0

# -d adalah untuk menjalankan container dalam mode terpisah
# -p untuk nomor port, formatnya adalah local-port:container-port
# --name untuk nama container

# List container yang berjalan
docker ps

# Update tag sesuaikan dockerhub
docker tag nginx:1.0 druzxh/nginx:1.0

# Push ke dockerhub
docker push nginx:1.0
```

### Thank you
