
<div align="center">
  <img src="assests/Ansible-img.webp" alt="Ansible" width="500" height="350" />

  # Ansible Monitoring Hub
  Simple, dynamic deployment of monitoring stacks using Ansible
</div>

## 🚀 Quick Deploy

```bash
# Deploy full stack
ansible-playbook playbook.yml -e '{
  "deploy_components": {
    "grafana": true,
    "loki": true,
    "node_exporter": true,
    "process_exporter": true,
    "prometheus": true
  }
}'


# Deploy specific components
ansible-playbook playbook.yml -e '{
  "deploy_components": {
    "grafana": true,
    "prometheus": true
  }
}'
```

## 📊 Components & Ports

- Grafana ``:3000``
- Prometheus ``:9090``
- Node Exporter ``:9100``
- Process Exporter ``:9256``

## 🔧 Requirements

- Ansible 2.9+
- Ubuntu 20.04+
- SSH access
- Sudo privileges

## 🔍 Service Status

```bash
# Check service status
sudo systemctl status [service-name]

# Available services:
# - grafana-server
# - prometheus
# - node_exporter
# - process-exporter
```

## 📝 License

This project is licensed under the terms of the LICENSE file included.
