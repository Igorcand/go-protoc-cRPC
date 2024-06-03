# gRPC project with go module protoc gen

## Sobre o Projeto ##

O servidor foi desenvolvido utilizando a linguagem Go e a extensão protoc, que permite a criação de APIs eficientes e escaláveis. A comunicação entre o cliente e o servidor é gerenciada pelo protocolo gRPC, que facilita a troca de mensagens estruturadas e de alta performance.

## Tecnologias usadas ##
- Go
- Protoc
- Evans
- SQLite

## Como rodar ##

```bash

# Instalações
sudo apt-get protoc-protocol

go mod init

export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin

go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28

go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2

go install github.com/ktr0731/evans@latest

go mod tidy 

#Gerar/atualizar arquivo principaç
protoc --go_out=. --go-grpc_out=. proto/course_category.proto

#Rodar servidor
go run cmd/grpcServer/main.go

#Rodar evans
evans -r repl
package pb
service CategoryService

call CreateCategory
call CreateCategoryStream
call CreateCategoryStreamBidirectional
call ListCategories
call GetCategory


```

## Autor ##

Igor Cândido Rodrigues

https://www.linkedin.com/in/igorc%C3%A2ndido/