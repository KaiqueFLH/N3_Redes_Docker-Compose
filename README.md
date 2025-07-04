# Avaliação N3 - Redes de Computadores

Este projeto contém uma configuração do Docker Compose para implantar um ambiente web com Nginx, WordPress, MySQL e phpMyAdmin, atendendo aos requisitos da Avaliação N3.

**Alunos:**
* Kaique Fernandes Lima Homem
* Vitor Augusto Rinkawetsky
* Davi Simplício

---

### Como Executar

1.  **Pré-requisito:** Ter [Docker](https://www.docker.com/products/docker-desktop/) e Docker Compose instalados.
2.  Clone este repositório: `git clone https://github.com/KaiqueFLH/N3_Redes_Docker-Compose.git`
3.  Navegue até a pasta do projeto: `cd DOCKER_N3`
4.  Execute o seguinte comando para iniciar todos os serviços em segundo plano:
    ```bash
    docker-compose up -d
    ```

---

### Como Acessar os Serviços

Após a execução, os serviços estarão disponíveis nos seguintes endereços:

* **WordPress (Site Principal):**
    * URL: **http://localhost/prova**
    * *Este é o endereço principal a ser avaliado.*

* **phpMyAdmin (Gerenciador de Banco de Dados):**
    * URL: **http://localhost:8080**
    * **Servidor:** `mysql`
    * **Usuário:** `root`
    * **Senha:** `Catolica@SC`

---

### Estrutura do Projeto

* **`docker-compose.yml`**: Arquivo principal que define e configura os 4 serviços (`nginx`, `wordpress`, `mysql`, `phpmyadmin`), a rede e os volumes de dados.
* **`nginx_config/proxy.conf`**: Arquivo de configuração do Nginx, responsável por criar o proxy reverso para o serviço do WordPress no endpoint `/prova`.