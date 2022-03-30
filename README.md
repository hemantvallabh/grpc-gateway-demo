Demo of https://github.com/grpc-ecosystem/grpc-gateway


protoc -I protodef protodef/helloworld.proto --go_out=plugins=grpc:protofiles
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative protodef/helloworld.proto

###USE THIS
protoc -I . --grpc-gateway_out . --grpc-gateway_opt logtostderr=true --grpc-gateway_opt paths=source_relative --grpc-gateway_opt generate_unbound_methods=true protodef/helloworld.proto