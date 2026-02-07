# 🛡️ SecurityCompany - Infraestrutura Ágil com Docker

Este projeto demonstra a implementação de uma arquitetura de microserviços utilizando **Containers Docker**. A stack foi desenhada para ser resiliente, escalável e oferecer visibilidade total sobre a saúde dos serviços através de ferramentas de monitoramento modernas.



---

## 🏗️ Arquitetura da Solução

A solução é composta por 5 serviços principais que se comunicam através de uma rede virtual isolada no Docker:

* **Frontend (Nginx):** Servidor web otimizado (Alpine) entregando a interface da SecurityCompany.
* **Database (MariaDB):** Camada de persistência de dados SQL.
* **Management (Adminer):** Ferramenta web para administração de banco de dados.
* **Observability (Netdata):** Dashboard de monitoramento de performance em tempo real.
* **Agent (Zabbix):** Coleta de telemetria e métricas do sistema.

---

## 🛠️ Conhecimentos Aplicados (Hard Skills)

Este projeto foi um excelente exercício de **Troubleshooting** e **IaC**, onde apliquei:
1.  **Infrastructure as Code (IaC):** Definição de toda a stack através de um único arquivo `docker-compose.yml`.
2.  **Dockerização de Aplicações:** Criação de `Dockerfiles` customizados, com gestão de camadas e otimização de imagens.
3.  **Persistência de Dados:** Implementação de **Docker Volumes** para garantir que as informações do banco de dados sobrevivam a reinicializações.
4.  **Networking:** Configuração de redes internas para que os serviços se comuniquem por `service_name` em vez de IPs fixos.
5.  **Observabilidade:** Configuração de ferramentas de monitoramento de baixo overhead para análise de métricas em tempo real.

---

## 🚀 Como Executar

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/Raelzxda/SecurityCompany.git](https://github.com/Raelzxda/SecurityCompany.git)
    cd SecurityCompany
    ```

2.  **Suba a infraestrutura:**
    ```bash
    docker compose up -d --build
    ```

---

## 🔐 Acesso aos Serviços e Credenciais

Abaixo, os dados para validação de cada camada da aplicação:

| Serviço | Porta | Descrição | Credenciais |
| :--- | :--- | :--- | :--- |
| **Site Web** | `8080` | Interface Principal | Acesso Público |
| **Adminer** | `8081` | Gestão do Banco | **Servidor:** `db` <br> **Usuário:** `root` <br> **Senha:** `root_310504` |
| **Netdata** | `19999` | Monitoramento | Dashboards em Tempo Real |
| **Zabbix** | `10050` | Agente de Métricas | Coleta Interna |

> **Nota de Segurança:** Para fins de teste em ambiente de estágio, as credenciais estão em variáveis de ambiente simplificadas. Em produção, recomenda-se o uso de **Docker Secrets**.

---

## 🔧 Resolução de Problemas (Troubleshooting)

Durante o deploy, realizei as seguintes correções críticas:
* **Ajuste de Contexto:** Correção de caminhos no `Dockerfile` para garantir a cópia correta dos arquivos estáticos.
* **Dependências de Rede:** Configuração de ordens de inicialização para garantir que o banco de dados estivesse pronto para conexões externas.
* **Depuração de Build:** Resolução de erros de "File Not Found" através do ajuste de caminhos relativos no contexto do Docker.

---

## 👨‍💻 Desenvolvedor

Confira este e outros projetos no meu perfil:
🔗 **[GitHub do Gabriel (Raelzxda)](https://github.com/Raelzxda)**
**Desenvolvido por Gabriel Gomes**
*Conecte-se comigo no [LinkedIn](https://www.linkedin.com/in/gabriel-gms011/)*
