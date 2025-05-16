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

#Hypothesis 1: Missing dockerstats Receiver in OpenTelemetry Collector Configuration
Problem: The OpenTelemetry Collector (OTel Collector) configuration lacks the dockerstats receiver, which is essential for collecting Docker container metrics.

Implementation: Create a new branch and update the OTell Collector Configuration.