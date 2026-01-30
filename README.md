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

As credenciais e tokens sensíveis são armazenados de forma segura utilizando **GitHub Secrets**.

---

## 🐳 Como rodar o projeto com Docker

⚠️ **Importante:** o front-end **depende do back-end em execução** para funcionar corretamente.  
O back-end deve estar acessível na porta **5000**.

---

### ▶️ Rodando **sem Docker Compose**

Este modo assume que o **back-end já está rodando**, seja:
- localmente (`npm run dev` / `npm start`), ou
- via Docker / Docker Compose no repositório do back-end.

#### Pré-requisitos
- Docker instalado

#### Passos

```bash
docker build -t bingo-driven-frontend .
docker run -p 80:80 bingo-driven-frontend

A aplicação ficará disponível em:
http://localhost

