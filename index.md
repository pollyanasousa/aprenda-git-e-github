# 🧭 Aprenda Git e GitHub  
### 🚀 Guia Completo: Subindo um Projeto no GitHub com Git e SSH  

Bem-vindo(a)! 👋  
Este guia foi criado com o objetivo de ajudar iniciantes a **configurar o Git, conectar ao GitHub via SSH e publicar seus projetos** com segurança.  
Perfeito para quem quer dominar o básico e dar os primeiros passos com confiança! 💪  

---

## 🎯 Objetivo  

Este guia tem como propósito:  
- 🧩 Instalar e configurar o **Git** corretamente  
- 🔐 Criar e adicionar uma **chave SSH** ao GitHub  
- 📦 Criar um **repositório local e remoto**  
- 🚀 Fazer o **push** do seu projeto para o GitHub  
- 🌎 Ativar o **GitHub Pages** e publicar o projeto online  

---

## 🧠 O que você vai aprender  

Durante este passo a passo, você aprenderá a:  
- Configurar nome e e-mail no Git  
- Criar e usar chaves SSH  
- Versionar arquivos (`git add`, `git commit`, `git push`)  
- Conectar um repositório local ao remoto  
- Publicar seu site com GitHub Pages  

---

## ⚙️ Passo a Passo

### 1️⃣ Instale o Git

- **Windows:** baixe em [git-scm.com/download/win](https://git-scm.com/download/win)  
- **macOS:**  
  ```bash
  brew install git
  ```
- **Linux (Ubuntu/Debian):**  
  ```bash
  sudo apt update && sudo apt install git
  ```

---

### 2️⃣ Configure o Git com seu nome e e-mail

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
git config --list
```

---

### 3️⃣ Crie sua conta no GitHub

Acesse [github.com](https://github.com), clique em **Sign up**, crie seu usuário e confirme o e-mail.

---

### 4️⃣ Gere sua chave SSH

```bash
ssh-keygen -t ed25519 -C "seuemail@example.com"
```

> 💡 Dica: esse comando cria uma chave segura para autenticação no GitHub sem precisar digitar senha.

---

### 5️⃣ Ative o agente SSH (Linux/macOS)

```bash
eval "$(ssh-agent -s)"
```

No **Windows**, esse passo normalmente é automático.

---

### 6️⃣ Adicione e copie a chave SSH

```bash
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

No GitHub → **Settings → SSH and GPG keys → New SSH key** → cole a chave → **Add SSH key** ✅

---

### 7️⃣ Crie um repositório remoto no GitHub

Clique em **New repository**, dê um nome, escolha público ou privado e clique em **Create repository**.

---

### 8️⃣ Crie uma pasta local

```bash
C:\Users\PC\OneDrive\Área de Trabalho\git-github-guia-iniciantes
```

Adicione o arquivo `git_para_iniciantes.md` dentro dela.

---

### 9️⃣ Inicialize o repositório local

```bash
cd "C:\Users\PC\OneDrive\Área de Trabalho\git-github-guia-iniciantes"
git init
git add .
git commit -m "Adiciona guia de Git para iniciantes"
```

---

### 🔗 10️⃣ Conecte ao GitHub via SSH

```bash
git remote add origin git@github.com:seu-usuario/git-para-iniciantes.git
```

---

### 🚀 11️⃣ Envie os arquivos

```bash
git push -u origin main
```

> Se o branch principal for `master`, troque `main` por `master`.

---

### 🌎 12️⃣ Ative o GitHub Pages

No repositório → **Settings → Pages → Source → branch main → / (root)** → **Save**  
✅ Pronto! Seu site será publicado em:  
`https://seu-usuario.github.io/git-para-iniciantes/`

---

## 🏆 Badges

![Git](https://img.shields.io/badge/GIT-black?style=for-the-badge&logo=git)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown)
![Praticando](https://img.shields.io/badge/Praticando-blue?style=for-the-badge)

---

## 🔗 Link do Projeto

Acesse o repositório remoto via SSH:  
👉 `git@github.com:pollyanasousa/aprenda-git-e-github.git`  
🔗 [Abrir no GitHub](https://github.com/pollyanasousa/aprenda-git-e-github)

---

## ✍️ Autor

Feito com 💙 por **Pollyana Sousa**  
📚 Inspirado na vontade de aprender e compartilhar conhecimento!  