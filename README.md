# SecurityCompany
# 🛡️ SecurityCompany v2.0 - Dashboard de Auditoria e Segurança

O **ScurityCompany** é um projeto de monitoramento de infraestrutura focado em **DevSecOps** e **Observabilidade**. Ele automatiza a coleta de logs críticos do sistema Linux e exibe esses dados em um dashboard web em tempo real, permitindo a identificação rápida de falhas de acesso e status de serviços.

---

## 🚀 Tecnologias Utilizadas

* **Linux (Ubuntu/Debian):** Base do sistema e gerenciamento de permissões.
* **Nginx:** Servidor web de alta performance para hospedar o dashboard.
* **Bash Scripting:** Automação da coleta e filtragem de logs (`systemd`).
* **Journalctl:** Ferramenta de auditoria do Kernel e serviços.
* **Bootstrap 5:** Frontend responsivo com interface em Dark Mode.
* **Git/GitHub:** Controle de versão e CI/CD manual.

---

## 🛠️ Funcionalidades e Troubleshooting

Durante o desenvolvimento, foram aplicados conceitos fundamentais de administração de sistemas:

1.  **Auditoria com Journalctl:** Filtra erros críticos (Prioridade 3) ocorridos nas últimas 24 horas.
2.  **Automação:** Script Bash configurado via `Crontab` para atualização automática.
3.  **Resiliência (Rollback):** Implementação de fluxos de manutenção com backups temporários (`.bak`).
4.  **Permissões POSIX:** Gerenciamento de acessos via `chmod` e `chown` para garantir que o serviço Nginx consuma os dados de forma segura.

---

## 📂 Como rodar o projeto

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/](https://github.com/)[SEU-USUARIO]/SecurityCompany.git
    ```

2.  **Configure o Script de Auditoria:**
    Dê permissão de execução ao script:
    ```bash
    chmod +x audit_web.sh
    sudo ./audit_web.sh
    ```

3.  **Acesse o Dashboard:**
    Abra o navegador e digite o IP da sua máquina.

---

## 📈 Próximos Passos (SentinelStack)
Este projeto é a base para a implementação de tecnologias mais avançadas. O próximo estágio incluirá:
- [ ] Containerização com **Docker**.
- [ ] Orquestração com **Kubernetes**.
- [ ] Monitoramento avançado com **Zabbix**.

---
**Desenvolvido por Gabriel Gomes**
*Conecte-se comigo no [LinkedIn](https://www.linkedin.com/in/gabriel-gms011/)*
