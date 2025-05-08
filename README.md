# Kubernetes YAML Format & Vulnerability Scan

This repository uses a GitHub Actions workflow to automatically format and scan Kubernetes YAML files for vulnerabilities and misconfigurations on every push or pull request.

## 🔍 What It Does

On every commit or PR that includes `.yaml` or `.yml` files, the following steps are triggered:

1. **Format YAML files** using [Prettier](https://prettier.io/)
2. **Vulnerability scan** using [Trivy](https://github.com/aquasecurity/trivy)
3. **Static analysis** using [kube-linter](https://github.com/stackrox/kube-linter)
4. **Policy-as-code scanning** with [Checkov](https://www.checkov.io/)

---

## ✅ Workflow Triggers

The workflow runs on:

- `push` and `pull_request` events
- When changes are made to any `.yaml` or `.yml` files

---

## 🛠️ Tools Used

| Tool         | Purpose                                     |
|--------------|---------------------------------------------|
| Prettier     | YAML formatting                             |
| Trivy        | Vulnerability and misconfiguration scanning |
| kube-linter  | Kubernetes YAML static analysis             |
| Checkov      | Kubernetes policy-as-code checks            |

---

## 🚀 Quick Start

To use this workflow:

1. Clone this repository.
2. Push or modify any `.yaml`/`.yml` files.
3. The GitHub Action will automatically run and report results in the Actions tab.

---

## ⚙️ Optional Customizations

- **Skip formatting**: Remove the Prettier step if unnecessary.
- **Tune scan rules**: Adjust Trivy, kube-linter, or Checkov configurations as needed.
- **Add custom policy files** if you want more specific checks.

---

## 📄 License

MIT
