# File Uploader Conf for NGINX

## Build source
Change to the directory of source code and execute:
```shell
go build main.go
```
## Build Docker images of file server
```shell
docker build -t uploadserver:1.0 .
```

## Run the file uploadserver
```shell
docker run  -d --name uploadserver -p 9092:8083 uploadserver:1.0
```

## Validate to upload file without NGINX
Open the index.html via browser, make sure the IP address and port is right

## Add nginx config
Refer to upload.conf.
