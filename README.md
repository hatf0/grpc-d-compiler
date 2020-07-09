# gRPC-D-Compiler
## Info
This program is intended to compile .proto files to a format which [gRPC-D](https://github.com/hatf0/grpc-d) expects.

It is maintained as a fork of [dcarp/protobuf-d](https://github.com/dcarp/protobuf-d)'s compiler (and as such, all arguments that are recognized by it are recognized by this).

**IMPORTANT**: this COMPILER must be used instead of the protobuf-d compiler if you are attempting to use gRPC-D. 
## Usage
This program is intended to be passed to the protoc compiler (as a plugin argument).

**IMPORTANT**: You must **ALWAYS** pass `--d_opt=message-as-struct` (subject to change)

Example usage:
`protoc --plugin=/usr/bin/protoc-gen-grpcd hello_world.proto --d_opt=message-as-struct --d_out=./`
