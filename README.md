# DevOps Journey: From Zero to Cloud

This repository documents my practical evolution through the Cloud and DevOps roadmap. The goal is to record hands-on labs, automation scripts, and architectural configurations as I progress toward cloud engineering mastery.

## Phase 1: Operational Foundation
In this first stage, I consolidated the core skills required to manage remote servers without a graphical interface (Headless OS).

**Hands-on Skills Mastered:**
* **Linux & Terminal:** Directory navigation (`cd`, `ls`), file manipulation (`touch`, `mkdir`, `mv`), and CLI editing (`nano`).
* **Security & Permissions:** File system access management using symbolic and octal modes (`chmod o-r`, `chmod u+rwx`).
* **Practical Networking:** Network diagnostics and HTTP communication using native tools (`ip a`, `ping`, `curl -I`).
* **Git & Version Control:** Identity configuration, HTTPS cloning, state management (`add`, `commit`), and remote synchronization (`push`, `pull`).

**Lab Environment:**
* Operating System: Ubuntu Server (ARM64)
* Virtualization: OrbStack (Apple Silicon)

## Phase 2: Containers & Docker
In this phase, I advanced to modern containerization, establishing a lightweight, scalable foundation for application deployment.

**Hands-on Skills Mastered:**
* **Container Lifecycle Management:** Orchestrated container states using Docker CLI (`run`, `stop`, `rm`, `ps`, `images`).
* **Network & Port Binding:** Exposed containerized applications (Nginx) to host environments using port mapping (`-p`).
* **Processing States:** Managed daemonized services (`-d`) versus interactive terminal sessions (`-it`).
* **Infrastructure as Code (IaC):** Authored `docker-compose.yml` configuration files to deploy and tear down multi-service environments.
* **System Administration:** Performed headless Docker Engine installations via shell scripts and managed Linux user group privileges (`usermod -aG`).

### Git Version Control & Merge Conflict Resolution
In addition to basic version control, I have hands-on experience managing collaborative challenges, specifically resolving merge conflicts:
* Configuring global Git reconciliation strategies (`git config --global pull.rebase false`).
* Manually identifying and resolving code merge markers (HEAD vs. Incoming changes) using terminal-based text editors.
* Ensuring repository integrity before executing the final resolution commits to the remote branch.

## Phase 3: Real-World Troubleshooting & Bash Automation
In this module, I simulated a production incident and utilized advanced Linux debugging techniques to restore the environment, culminating in fully automated recovery processes.

* **Diagnostic Tooling:** Used `find` to locate buried application logs and `grep` to filter fatal errors out of unstructured text.
* **Configuration Auditing:** Applied `diff` to compare configuration files and trace developer misconfigurations across environments.
* **Automated Disaster Recovery:** Engineered a robust Bash script to execute systematic backups of production logs. Integrated dynamic variable assignment and command substitution (`$()`) to automatically stamp archives with precise temporal metadata.
* **Unattended Execution Lifecycle:** Transitioned the backup script from a manual operation to an autonomous lifecycle by configuring the Linux `cron` daemon, ensuring continuous execution without human intervention.
* **Execution Pathing:** Enforced strict absolute pathing paradigms within automation scripts to prevent execution failures associated with background environments.

## Phase 4: Secure Networking & Remote Administration
In this module, I secured server access protocols and established encrypted communication channels using industry best practices.

* **Asymmetric Cryptography Authentication:** Deprecated vulnerable password-based logins in favor of enterprise-grade asymmetric cryptography by generating and deploying RSA-4096 SSH key pairs.
* **Zero Trust & Network Isolation:** Established secure, encrypted remote administrative access to the primary server over a private mesh VPN topology (Tailscale), adhering to Zero Trust architecture principles.
* **OpenSSH Hardening:** Manually audited and locked down `.ssh` directory and `authorized_keys` file access using strict octal permission modes (`chmod 700` and `chmod 600`) to comply with OpenSSH daemon security standards.
* **MITM Mitigation:** Managed TOFU (Trust On First Use) host fingerprinting to validate server identity and prevent Man-in-the-Middle network interception.

## Phase 5: Advanced Git Troubleshooting & Build Tools
- **Conflict Resolution**: Mastered manual resolution of Git merge conflicts by isolating and editing `HEAD` and incoming branch markers.
- **State Recovery**: Utilized `git reset --soft` to perform non-destructive commit rollbacks, ensuring clean repository histories.
- **Build Ecosystems**: Analyzed the dependency management lifecycle using Node.js and NPM, establishing clear operational boundaries between application development and infrastructure deployment.

## Phase 6: Containerization Architecture (Docker)
- **Infrastructure as Code**: Engineered custom Docker images using `Dockerfile` to containerize a Node.js web application from raw source code.
- **Container Lifecycle**: Executed the complete build-to-run pipeline (`docker build`, `docker run -d -p`), configuring port mapping between isolated containers and the host network.
- **CI/CD Paradigms**: Mapped the enterprise software delivery lifecycle, contrasting the roles of Source Control (GitHub), Build Factories (CI Pipelines), Container Registries (Docker Hub/AWS ECR), and Production runtime environments.
- **Layer Optimization**: Evaluated Docker Layer Caching mechanisms and architectural distribution efficiency over traditional file transfers.

### Phase 7: Container Registries and Cloud Distribution
- **Objective:** Master image distribution architecture using external container registries.
- **Concepts Covered:**
  - Container Registries vs Local Image Caching.
  - Authentication and Session Management (`docker login`).
  - Image Namespace Tagging (`docker tag`).
  - Cloud Push/Pull Lifecycle (`docker push`, `docker pull`).
  - Forcing clean state deployments by pruning local images (`docker rmi`).
- **Practical Lab:** Built a V2 Node.js container image, tagged it with a standard Docker Hub namespace, pushed it to the public registry, purged the local environment to simulate a fresh production server, and successfully ran the container by pulling it directly from the cloud.
