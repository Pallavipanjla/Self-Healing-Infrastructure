# Self-Healing-Infrastructure
Automatically detect service failures and recover them using alerts and automation

# Components Used:-

Prometheus – A Monitoring system to detect service status
Alertmanager – Handles alerts triggered by Prometheus
Flask Web Server – Acts as a webhook receiver for Alertmanager
Ansible – Automates restarting the NGINX service
NGINX – Target service being monitored

# Setup and Configuration:-

1. Prometheus Configuration (prometheus.yml)
2. Alertmanager Configuration (alertmanager.yml)
3. Flask Webhook Server (webhook_server.py)
4. Ansible Playbook (heal.yml)

# How It Works:-

- Prometheus scrapes NGINX metrics from the exporter.
- If NGINX is down, Prometheus triggers an alert.
- Alertmanager forwards the alert to the Flask webhook server.
- The Flask server receives the alert and triggers an Ansible playbook.
- Ansible restarts the NGINX service automatically.

----
