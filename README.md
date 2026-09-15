# DevOps Journey: From Zero to Cloud

This repository documents my practical evolution through the Cloud and DevOps roadmap. The goal is to record hands-on labs, scripts, and automations in a real-world environment.

## Phase 1: Operational Foundation (Completed)
In this first stage, I consolidated the core skills required to manage remote servers without a graphical interface (Headless OS).

**Hands-on Skills Mastered:**
* **Linux & Terminal:** Directory navigation (`cd`, `ls`), file manipulation (`touch`, `mkdir`, `mv`), and CLI editing (`nano`).
* **Security & Permissions:** File system access management using symbolic and octal modes (`chmod o-r`, `chmod u+rwx`).
* **Practical Networking:** Network diagnostics and HTTP communication using native tools (`ip a`, `ping`, `curl -I`).
* **Git & Version Control:** Identity configuration, HTTPS cloning, state management (`add`, `commit`), and remote synchronization (`push`).

**Lab Environment:** 
* Operating System: Ubuntu Server (ARM64)
* Virtualization: OrbStack (Apple Silicon)

### Phase 2: Containers & Docker (Completed)

In this phase, I advanced to modern containerization, establishing a lightweight, scalable foundation for application deployment.

**Hands-on Skills Mastered:**
- **Container Lifecycle Management:** Orchestrated container states using Docker CLI (`run`, `stop`, `rm`, `ps`, `images`).
- **Network & Port Binding:** Exposed containerized applications (Nginx) to host environments using port mapping (`-p`).
- **Foreground vs. Background Processing:** Managed daemonized services (`-d`) versus interactive terminal sessions (`-it`).
- **Infrastructure as Code (IaC) Introduction:** Authored `docker-compose.yml` configuration files to deploy and tear down multi-service environments deterministically using `docker compose up -d` and `down`.
- **System Administration:** Performed headless Docker Engine installations via shell scripts and managed Linux user group privileges (`usermod -aG`) to secure daemon access.
