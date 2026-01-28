## 🚀 Deploy em Produção

- **Front-end (Vercel):**  
  https://bingo-frontend-p7k6cfumy-tainaras-projects-5dbdb007.vercel.app/

- **Imagem Docker (Docker Hub):**  
  https://hub.docker.com/r/tainara97/bingo-driven-frontend

---

## 🛠️ Tecnologias Utilizadas

- React
- Vite
- TypeScript
- Docker
- Nginx
- GitHub Actions (CI/CD)
- Vercel

---

## 🔄 CI/CD

O projeto possui uma pipeline de **Continuous Deployment (CD)** utilizando **GitHub Actions**, com o seguinte fluxo:

- Build da imagem Docker do front-end
- Publicação automática da imagem no Docker Hub
- Deploy automático na Vercel a partir da branch `main`

---

## 🐳 Como rodar o projeto com Docker

### Pré-requisitos
- Docker instalado

### Passos

```bash
docker build -t bingo-driven-frontend .
docker run -p 80:80 bingo-driven-frontend