# Lab 01: DevOps Lifecycle & Value Stream Mapping

**Author:** Lasha Chipashvili  
**Course:** DevOps

---

## 1. Individual DevOps Lifecycle Breakdown

* **Plan:** Define feature scope (e.g., adding user profile page) in GitHub Issues/Projects.
* **Code:** Write application code and unit tests locally in VS Code using Git branches.
* **Build:** Build Docker images for the application locally or via GitHub Actions.
* **Test:** Run automated test suites (Pytest/Playwright) to verify code stability.
* **Release:** Tag releases (`v1.0.0`) and generate release notes in GitHub.
* **Deploy:** Deploy application container using Docker Compose.
* **Operate:** Manage running containers and environment settings.
* **Monitor:** Track application logs and runtime health via basic metrics/logs.

---

## 2. Value Stream Map (VSM)

| Stage | Type | Process Time | Wait Time | Bottleneck / Friction |
| :--- | :--- | :--- | :--- | :--- |
| **Plan** | Manual | 1 hour | 2 hours | Ambiguous feature requirements |
| **Code** | Manual | 4 hours | 1 hour | Context switching / debugging |
| **Build** | Automated | 3 minutes | 0 mins | None |
| **Test** | Semi-Automated | 30 minutes | 1 hour | Fixing broken test setups |
| **Release** | Manual | 15 minutes | 30 mins | Manual tagging and checks |
| **Deploy** | Automated | 5 minutes | 0 mins | None |
| **Operate** | Automated | N/A | 0 mins | None |
| **Monitor** | Automated | Real-time | 0 mins | None |

---

## 3. VSM Analysis & Improvements

The primary delay occurs during the **Code** and **Test** phases, where manual debugging and resolving broken test environments consume significant waiting and operational time. To streamline this workflow, I would implement automated linting and unit test execution on every Git commit using local Git hooks or automated CI pipelines. Additionally, fully automating the release process upon passing tests will eliminate unnecessary manual approval delays.
