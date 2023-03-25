# filtered-opentelemetry-go
A Go OpenTelemetry SDK to flexibly filter out traces.


## Timeline


We selected Golang, together with opentelemetry-go as our implementation base, and there are changes to thie proposal after the in-class chat. We are first implementing attributes filtering directly inside the normal OT Exporter, testing its performance variation, then considering structure filtering feature.

- By Mar 31: Reading the opentelemetry exporter implementation, designing proper code modification locations. Designing system architecture (e.g. query parser, modified collector, etc.)
- By Apr 06: A basic extension to opentelemetry accepting static filtering policy, start designing benchmark set.
- By Apr 13: A further extension to opentelemetry allowing changing policy at runtime, benchmarking the static version for performance
- By Apr 23: Building other components, like distributing policy to instances, parsing query to policy / or providing graphical attribute selector. Implementing full benchmark set, including request generator and dynamic policy generators.
- By Apr 30: Sorting benchmark results, exploring structural filtering.
- Apr 30+: Tentative time for delay in previous tasks or structural filtering implementation.
- Final Presentation.
