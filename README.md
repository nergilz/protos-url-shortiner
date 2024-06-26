# protos-url-shortiner

```bash
protoc -I proto proto/sso/sso.proto --go_out=./gen/go/ --go_opt=paths=source_relative --go-grpc_out=./gen/go
```
```
-I proto — опция -I или —proto_path указывает путь к корневой директории с файлами .proto. Это нужно, чтобы компилятор смог найти импорты, если они есть. В нашем случае это директория proto.

proto/sso/sso.proto — путь к конкретному .proto файлу, который мы компилируем.

—go_out=./gen/go/ — опция —go_out указывает, куда записывать сгенерированный код Go. 

—go_opt=paths=source_relative — дополнительная опция, которая указывает, как создавать имена пакетов. paths=source_relative означает, что выходные файлы будут иметь тот же пакет, что и исходные файлы .proto.

—go-grpc_out=./gen/go/ — указывает, куда записывать сгенерированный Go gRPC-код. Как и в предыдущем случае, выходные файлы будут помещены в директорию ./gen/go/.

—go-grpc_opt=paths=source_relative — это аналогичная опция для генерации Go gRPC-кода, которая указывает, как создавать имена пакетов для gRPC.
```