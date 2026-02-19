# 🏗️ Homelab Platform SRE

Este repositório documenta a construção e operação de um ambiente **Kubernetes Bare-metal**, focado em práticas reais de engenharia de confiabilidade (SRE), troubleshooting e cultura de automação.

> **Diferencial:** O foco deste projeto não é apenas "subir um cluster", mas demonstrar a capacidade técnica de operar, suportar e documentar workloads de forma profissional.

---

## 🎯 Objetivo
Construir experiência prática comprovável (*hands-on*) em:
* **Provisionamento:** Instalação e configuração via Kubeadm + Containerd.
* **Operação:** Criação de runbooks acionáveis e análise de post-mortems.
* **Troubleshooting:** Diagnóstico de falhas em componentes do cluster e camadas de rede/storage.

---

## 💻 Infraestrutura & Ambiente

O cluster é executado sobre um hipervisor **Proxmox**, simulando um cenário de infraestrutura on-premises.

### Inventário do Cluster
| Role | OS | CPU | RAM | Stack |
| :--- | :--- | :--- | :--- | :--- |
| **Control Plane** | Ubuntu 22.04 | 2 vCPU | 4 GB | Kubeadm / Containerd |
| **Worker 01** | Ubuntu 22.04 | 2 vCPU | 3 GB | Kubeadm / Containerd |
| **Worker 02** | Ubuntu 22.04 | 2 vCPU | 3 GB | Kubeadm / Containerd |
| **Admin Host** | Windows + WSL2 | - | - | Kubectl / Helm |

---

## 📂 Organização do Repositório

A estrutura foi desenhada para refletir a organização de um time de plataforma:

* [**`notes/`**](notes/)  
  *Diário de bordo: registros do progresso diário, comandos úteis e lições aprendidas.*
* [**`runbooks/`**](runbooks/)  
  *Guias acionáveis: procedimentos passo-a-passo para diagnóstico e correção de incidentes.*
* [**`scripts/`**](scripts/)  
  *Automação: scripts de bootstrap, validação de ambiente e utilitários de gestão.*
* [**`docs/`**](docs/)  
  *Arquitetura: registros de decisões (ADRs), diagramas e referências técnicas.*

---

## 🛠️ Tecnologias Principais
- **Runtime:** Containerd
- **Orquestração:** Kubernetes (v1.x+)
- **Virtualização:** Proxmox VE
- **Terminal:** WSL2 (Ubuntu)

