# gRPC Python with Bazel Example

A minimal example of a gRPC service defined in a proto implemented in python with bazel.

To see an example without bazel see [https://github.com/theneekz/grpc-py-example](https://github.com/theneekz/grpc-py-example)

## Usage

To build from root directory:

```bash
bazel build server
```

To run after building from root directory:

```bash
bazel run server
```

To regenerate pyi file, change something within the proto before rebuilding. Or
clean before rebuilding:

```bash
bazel clean
```

To send requests to the server with postman:

- Create a new gRPC request
- Enter the URL `localhost:50051`
- Import the `lobby_service.proto` proto service definition
- Select the method `ListLobbies`
- Invoke
