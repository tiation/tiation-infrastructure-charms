---
layout: default
title: Tiation Infrastructure Charms
---

# Tiation Infrastructure Charms

**Kubeflow + MLflow on Juju with Microk8s - Enterprise Infrastructure Solutions**

![screenshot](demo.png "Screenshot showing kubeflow notebook publishing to mlflow")

Deploy and manage enterprise-grade machine learning infrastructure with Kubeflow and MLflow on Kubernetes using Juju charms.

---

## 🚀 Key Features

- **🧪 Complete ML Stack**: Kubeflow + MLflow integration for end-to-end ML workflows
- **🔧 Easy Deployment**: One-command setup with Juju and Microk8s
- **📊 Experiment Tracking**: Built-in MLflow tracking and model registry
- **🛡️ Enterprise Ready**: Scalable, secure, and production-ready infrastructure
- **🔗 Seamless Integration**: Pre-configured environments for ML notebooks

---

## 🛠️ Quick Start

### Prerequisites
- Ubuntu system with 14GB+ RAM and 50GB+ disk space
- Docker Hub Pro account (to avoid rate limits)

### Installation

```bash
# Set up user permissions (first time only)
getent group microk8s || sudo groupadd microk8s
sudo usermod -a -G microk8s $USER
sudo chown -f -R $USER ~/.kube
sudo su - $USER

# Deploy the infrastructure
export DOCKER_USERNAME=<docker-hub-username>
export DOCKER_ACCESS_TOKEN=<docker-hub-password>
bash integration_test_microk8s
```

### Access the Environment

1. **Kubeflow Dashboard**: [http://10.64.140.43.nip.io/](http://10.64.140.43.nip.io/)
2. **MLflow UI**: Run `microk8s kubectl get services -A|grep mlflow` and access the ClusterIP with `:5000`

---

## 📖 Documentation

For detailed setup instructions, troubleshooting, and advanced configuration, see the [full documentation](README.md).

---

## 🎯 Use Cases

- **ML Experimentation**: Track experiments, parameters, and metrics
- **Model Development**: Collaborative notebook environment
- **Model Registry**: Centralized model storage and versioning
- **Production Deployment**: Scalable inference infrastructure

---

## 🗺️ Roadmap

- [ ] Write intro explaining why you'd want to do this
- [ ] Publish to charm store
- [ ] Expose MLflow GUI on MetalLB
- [ ] Make it work for namespaces other than admin
- [ ] Spell out the tutorial explicitly
- [ ] Reference various juju/kubeflow bugs
- [x] Record demo video
- [ ] Move to Canonical repo

---

## 🔗 Links

- **[GitHub Repository](https://github.com/tiation/tiation-infrastructure-charms)** - Full source code
- **[Issues](https://github.com/tiation/tiation-infrastructure-charms/issues)** - Report bugs or request features
- **[Discussions](https://github.com/tiation/tiation-infrastructure-charms/discussions)** - Community discussions

---

## 📞 Contact & Support

For questions, enterprise support, or custom Kubeflow/MLflow deployments:

- **Email**: [tiatheone@protonmail.com](mailto:tiatheone@protonmail.com)
- **Enterprise Support**: Available for custom infrastructure deployments

---

<div style="text-align: center; margin-top: 2rem; padding: 1rem; background-color: #f8f9fa; border-radius: 8px;">
  <strong>Part of the <a href="https://github.com/tiation">Tiation</a> ecosystem - Enterprise-grade infrastructure solutions</strong>
</div>
