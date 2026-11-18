# CitizenTech - MVP Deploy Blindado

## Ficha Técnica do MVP
- **Aplicação:** CitizenTech (Portal Web)
- **Containerização:** Docker (`nginx:alpine`)
- **Infraestrutura como Código (IaC):** Terraform (AWS EC2 `t2.micro` + Security Group)
- **Registro de Imagens:** Docker Hub
- **Pipeline DevSecOps:** GitHub Actions com Gitleaks (Secret Scanning) e Semgrep (SAST)
- **Observabilidade:** AWS CloudWatch Dashboard & CloudWatch Alarms + Amazon SNS

## Como Executar Localmente
```bash
docker build -t citizentech:v1 .
docker run -d -p 8080:80 --name web-citizen citizentech:v1