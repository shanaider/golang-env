# Install golang
```
brew install go
```

# Go init
```
go mod init {Project_name}  
```

# godotenv
ref. https://github.com/joho/godotenv
```
go install github.com/joho/godotenv/cmd/godotenv@latest
```

# go run (local)
```
go run main.go
```
# output
```
2024/11/21 22:49:39 S3_BUCKET: pig
2024/11/21 22:49:39 SECRET_KEY: duck
```

# docker build with multi-stage (--platform linux/amd64 --> mac M1)
ref.https://docs.docker.com/guides/golang/build-images/#multi-stage-builds
```
docker build --platform linux/amd64 -t pump-golang-env:v1.0.0 .
```

# docker run
```
docker run --platform linux/amd64 pump-golang-env:v1.0.0 
```

# output
```
2024/11/21 15:51:37 S3_BUCKET: pig
2024/11/21 15:51:37 SECRET_KEY: duck
```
