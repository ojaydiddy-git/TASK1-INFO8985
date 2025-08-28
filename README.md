# signoz
signoz demo with docker-compose 

```bash
ansible-playbook up.yml
```

This does docker compose up on an "empty" signoz in a codespace. Use this as a starting point for instrumenting your app.

```bash
ansible-playbook down.yml
```

This does docker compose down on the clickhouse-setup/docker-compose-minimal.yaml (the same docker-compose file from up.yml)


# Hypothesis 2: Instances to be logged were filtered.

Remove filtering from instances to be monitored

This has already been resolved by Professor Richard Hildred

Modify the otel-collector-config.yaml file to correct the OTLP exporter settings:

Refrences: https://faun.pub/monitoring-docker-container-metrics-with-signoz-cloud-a-comprehensive-guide-469548fc8b43