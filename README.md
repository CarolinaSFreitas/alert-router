# Kubernetes Get Images

Este projeto contém scripts e arquivos de configuração para orquestrar e monitorar aplicações utilizando Docker Compose, FastAPI, Prometheus e cAdvisor.

> Este projeto é parte do curso "Python para DevOps" do instrutor Mateus Muller na Udemy.

## Estrutura do Projeto

- `docker-compose.yaml`: Orquestração dos containers para ambiente local.
- `Dockerfile`: Imagem customizada para o serviço principal.
- `alert-router.py`: Script principal da aplicação.
- `requirements.txt`: Dependências Python do projeto.
- `prometheus/prometheus.yml`: Configuração do Prometheus para monitoramento.

## Como usar

1. Clone o repositório e acesse a pasta do projeto.
2. Crie e ative um ambiente virtual Python:
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```
3. Instale as dependências:
   ```powershell
   pip install -r requirements.txt
   ```
4. Suba os containers:
   ```powershell
   docker compose up -d
   ```
5. Acesse os serviços:
   - Aplicação principal: http://localhost:8000
   - Prometheus: http://localhost:9090
   - cAdvisor: http://localhost:8080

## Observações
- Certifique-se de que o arquivo `prometheus.yml` está no caminho correto e mapeado no `docker-compose.yaml`.
- Para personalizar o monitoramento, edite o arquivo `prometheus/prometheus.yml`.

---

Projeto para fins de aprendizado.