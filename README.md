## Otel Operator Setup
- [Cert Manager](https://cert-manager.io/docs/installation/kubectl/)
- [Otel Operator](https://github.com/open-telemetry/opentelemetry-operator/blob/main/README.md)

## Usage (Minikube)
- Add your Datadog API key in `otelcol.yaml`.
- `k apply -f deployment.yaml`
- `k expose deploy node`
- `minikube service node --url`
- Update `request.sh` to use the port returned by minikube.
- `k apply -f otelcol.yaml`
- `./request.sh` to produce traces.
