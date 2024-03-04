## Micronaut gRPC NoClassDefFound bug

See issue here https://github.com/micronaut-projects/micronaut-grpc/issues/855

To reproduce just run `./gradlew run` and observe the `NoClassDefFoundException` in the stacktrace

Happening since 4.0.0 since discovery dependency was removed, not happening in 3.x.x (discovery dependency was bundled together)

Workaround is to manually add discovery-core dependency, even tho it's not used.

