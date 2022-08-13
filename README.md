# Instructions

1. Build the nuget package for JsonTranscoding.Protos. From the project root:
```
dotnet pack JsonTranscoding.Protos\JsonTranscoding.Protos.csproj --output=publish
```
2. Add the above local publish folder from your filesystem to your NuGet package sources under Manage Nuget Package Sources so that VS can find it. This avoids having to publish it to a NuGet repository.
3. Then the restore for MyGrpcService should work on build.
4. Run the MyGrpcService project in VS. The console should output something like:

>  Now listening on: https://localhost:7119
5. Go to a browser and verify that e.g. the request https://localhost:7119/v1/greeter/richard works and returns `Hello Richard`.