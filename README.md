# helm-cd

This repo conatins the custom helm charts to deploy the following resources on EKS:-

1. hello-world application
2. Prometheus as mertrics collector
3. Grafana to create dashbaords around metrics
4. Sample playbook to automate the helm deployments
5. Jenkinsfile configured to run the ansible playbook (install ansible in same box where jenkins is installed)
