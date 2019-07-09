# Adapters

Mixer adapters allow Istio to interface to a variety of infrastructure backends for such things as metrics and logs.

> To implement a new adapter for Mixer, please refer to the [Adapter Developer's Guide](https://github.com/istio/istio/wiki/Mixer-Compiled-In-Adapter-Dev-Guide).

## Templates

The table below shows the set of [templates](https://istio.io/docs/reference/config/policy-and-telemetry/templates) that are implemented by each supported adapter.

 Adapter                                                                                                      | Supported Templates
--------------------------------------------------------------------------------------------------------------|----------------------------------
 [Apache SkyWalking](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/apache-skywalking/) | Metric
 [Apigee](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/apigee/)                       | Analytics, Authorization
 [Circonus](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/circonus/)                   | Metric
 [CloudMonitor](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/cloudmonitor/)           |
 [CloudWatch](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/cloudwatch/)               | Metric
 [Datadog](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/datadog/)                     | Metric
 [Denier](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/denier/)                       | Check Nothing, List Entry, Quota
 [Fluentd](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/fluentd/)                     | Log Entry
 [Kubernetes Env](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/kubernetesenv/)        | Kubernetes
 [List](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/list/)                           | List Entry
 [Memory quota](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/memquota/)               | Quota
 [OPA](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/opa/)                             | Authorization
 [Prometheus](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/prometheus/)               | Metric
 [Redis Quota](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/redisquota/)              | Quota
 [SignalFx](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/signalfx/)                   | Metric, Trace Span
 [SolarWinds](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/solarwinds/)               | Log Entry, Metric
 [Stackdriver](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/stackdriver/)             | Log Entry, Metric, Trace Span
 [StatsD](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/statsd/)                       | Metric
 [Stdio](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/stdio/)                         | Log Entry, Metric
 [Wavefront by VMware](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/wavefront/)       | Metric
 [Zipkin](https://istio.io/docs/reference/config/policy-and-telemetry/adapters/zipkin/)                       | Trace Span

 
