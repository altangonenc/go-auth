# go-auth

export GO111MODULE=on
go mod init altan.com/go-example

go get -u github.com/dgrijalva/jwt-go
go get -u github.com/gin-gonic/gin

go run main.go

curl -X POST http://localhost:8080/register -d '{"username":"exampleuser", "password":"secretpassword"}' -H "Content-Type: application/json"

curl -X POST http://localhost:8080/login -d '{"username":"exampleuser", "password":"secretpassword"}' -H "Content-Type: application/json"

curl -X GET http://localhost:8080/profile -H "Authorization: Bearer {TOKEN}"



