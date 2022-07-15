# Monitoring via docker-compose

Each docker-compose file placed at `/home/asible/docker-compose` directory

### Grafana with Prometheus
`./monitoring/monitoring.service.yaml`
 - prometheus
 - grafana
Suggested additional directories (`mkdir -p`):
 - /prometheus
 - /data
 - /grafana
 - /grafana/provisioning
```
docker-compose -f monitoring.service.yaml up -d
```

### Node
`./monitoring/monitoring.node.yaml`
 - node-exporter 
 - cadvisor
Suggested additional directories (`mkdir -p`):
 - None
```
docker-compose -f monitoring.node.yaml up -d
```

### Postgres
`./monitoring/monitoring.postgres.yaml`
 - postgres-exporter
 - pgadmin4 
Suggested additional directories (`mkdir -p`):
 - /pgadmin
```
docker-compose -f monitoring.postgres.yaml up -d 
```

