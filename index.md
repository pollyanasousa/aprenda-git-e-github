# Guia Completo: Subindo um Projeto no GitHub com Git e SSH 

Instale o Git no computador. No Windows, acesse https://git-scm.com/download/win, baixe e instale com as opções padrão. No macOS, use o comando `brew install git`. No Linux (Debian/Ubuntu), use `sudo apt update` seguido de `sudo apt install git`.

Configure o Git com seu nome e e-mail:  
`git config --global user.name "Seu Nome"`  
`git config --global user.email "seuemail@example.com"`  
Verifique com `git config --list`.

Crie uma conta no GitHub acessando https://github.com e clicando em "Sign up". Escolha um nome de usuário, e-mail e senha. Confirme seu e-mail para ativar a conta.

Configure a chave SSH para autenticação segura. Gere a chave com:  
`ssh-keygen -t ed25519 -C "seuemail@example.com"`

**Sobre o comando `eval "$(ssh-agent -s)"`:**  
Esse comando é usado para iniciar o agente SSH em sistemas como Linux ou macOS.  
No Windows, especialmente usando Git Bash ou PowerShell, esse passo geralmente não é necessário.  
Você não usou esse comando, Pollyana, e está tudo certo — o sistema já gerenciou isso automaticamente.

Adicione a chave (se necessário):  
`ssh-add ~/.ssh/id_ed25519`  
Copie a chave pública com:  
`cat ~/.ssh/id_ed25519.pub`  
No GitHub, vá em Settings > SSH and GPG keys > New SSH key, cole a chave e salve.

Crie um novo repositório remoto no GitHub clicando em "New repository". Dê um nome, escolha público ou privado e clique em "Create repository".

Crie manualmente uma pasta local no seu computador, por exemplo:  
`C:\Users\PC\OneDrive\Área de Trabalho\git-github-guia-iniciantes`  
Coloque dentro dela o arquivo `git_para_iniciantes.md` com o conteúdo desejado.

Abra o terminal e navegue até essa pasta:  
`cd "C:\Users\PC\OneDrive\Área de Trabalho\git-github-guia-iniciantes"`

Inicialize o repositório Git local com:  
`git init`

Adicione o arquivo ao controle de versão:  
`git add .`  
`git commit -m "Adiciona guia de Git para iniciantes"`

Copie o link SSH do repositório remoto (ex: `git@github.com:seu-usuario/git-para-iniciantes.git`) e conecte com:  
`git remote add origin git@github.com:seu-usuario/git-para-iniciantes.git`

Envie os arquivos para o GitHub com:  
`git push -u origin main`  
(Substitua `main` por `master` se necessário.)

Ative o GitHub Pages:  
Acesse o repositório no GitHub, vá em Settings > Pages. Em "Source", selecione o branch `main` e a pasta `/root`. Clique em "Save".

A página será publicada em:  
`https://seu-usuario.github.io/git-para-iniciantes/`

Pronto! Seu projeto está versionado com Git, publicado no GitHub e disponível como página web via GitHub Pages.