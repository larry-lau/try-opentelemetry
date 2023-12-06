# OpenTelemetry Example Application

This set of projects is an example application that use open telemetry collector to distribute trace, metrics and log to popular monitoring software.

The application demonstrates a number of OpenTelemetry concepts:
* OpenTelemetry APIs for distributed context propagation.
* Basic conventions of how messaging systems are handled in OpenTelemetry.

## Running the example
To run the example using `docker-compose`, run the following from this
directory:

```shell
docker-compose up --build
```

With everything running:

* View the demo web app at [http://localhost:16686](http://localhost:8080/)
* View traces with Zipkin at endpoint
  [http://localhost:9411/zipkin](http://localhost:9411/zipkin).
* View traces with Jaeger at endpoint
  [http://localhost:16686](http://localhost:16686/).
* View metrics with prometheus at endpoint
  [http://localhost:9090](http://localhost:9090/).
* View dashboard with grafana at endpoint
  [http://localhost:3000](http://localhost:3000/).

## References

* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [OpenTelemetry Project](https://opentelemetry.io/)
* [Prometheus](https://prometheus.io/)
* [Grafana](https://grafana.com/)
* [Jaeger](https://www.jaegertracing.io/)
* [Zipkin](https://zipkin.io)