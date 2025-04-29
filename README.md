# Material de Estudo: Git e GitHub

---

## 1. O que é Git?

Git é um **sistema de controle de versão distribuído** usado para rastrear alterações em arquivos durante o desenvolvimento de software. Ele permite:
- Trabalhar em equipe de forma organizada.
- Reverter para versões anteriores do código.
- Criar branches (ramificações) para testar novas funcionalidades sem afetar o código principal.

## Qual ferramenta de comando você deve utilizar ?
   
   ### Windows:
   Git bash. Para executar comandos git no Windows, baixe o GitBash:

   ### Linux:
   Terminal. O atalho Linux para abrir o terminal é: Ctrl+Alt+T. 

   ### MacOS:
   Terminal. No MacOS, abra o Spotlight clicando em Command + Espaço, (ou clique no ícone do Launchpadno Dock) digite Terminal no campo de busca e clique em Terminal.

---



## 2. O que é GitHub?

GitHub é uma plataforma de hospedagem de código que usa Git. Ele adiciona funcionalidades colaborativas, como:
- **Repositórios remotos** (para armazenar código na nuvem).
- **Pull Requests** (solicitações para integrar mudanças).
- **Issues** (gerenciamento de tarefas e bugs).

---

## 3. Comandos Básicos do Git

### Configuração Inicial
Configure seu nome e e-mail para o Git:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

### Iniciar um Repositório
Crie um repositório Git local:
```bash
git init
```

### Clonar um Repositório Remoto
Clone um repositório remoto para sua máquina local:
```bash
git clone https://github.com/usuario/repositorio.git
```

---

## 4. Comandos Essenciais

### Adicionar Arquivos ao Staging Area
Adicione arquivos para preparação antes do commit:
```bash
git add .          # Adiciona todos os arquivos modificados
git add arquivo.js # Adiciona um arquivo específico
```

### Fazer um Commit
Salve as alterações no histórico do Git:
```bash
git commit -m "Mensagem descritiva do commit"
```

### Enviar Alterações para o Repositório Remoto
Envie os commits locais para o repositório remoto:
```bash
git push origin main  # Envia para a branch main
```

### Atualizar o Repositório Local
Atualize o repositório local com as alterações do remoto:
```bash
git pull origin main
```

---

## 5. Trabalhando com Branches

### Listar Branches
Liste todas as branches do repositório:
```bash
git branch
```

### Renomear a Branch Atual
Renomeie a branch em que você está trabalhando:
```bash
git branch -m novo-nome
```

### Mudar para uma Branch Existente
Troque para uma branch já criada:
```bash
git checkout nome-da-branch
```

### Criar e Mudar para uma Nova Branch
Crie e mude para uma nova branch:
```bash
git switch -c feature/nova-funcionalidade
```

---

## 6. Salvando Alterações Temporárias

### Guardar Alterações Não Commitadas
Guarde alterações temporariamente para usar depois:
```bash
git stash          # Salva as alterações
git stash pop      # Recupera as alterações mais recentes
```

---

## Exercício Prático: JS + Git + GitHub

### Objetivo
Criar uma função em JavaScript que verifica se uma palavra é um palíndromo (lê-se igual de trás para frente). Use Git e GitHub para gerenciar o processo.

### Passo a Passo

1. **Crie um Repositório no GitHub**
   - Nome: `palindromo-checker`.
   - Adicione um arquivo `README.md`.

2. **Clone o Repositório Localmente**
   ```bash
   git clone https://github.com/l-furquim/material-estudo.git
   ```

3. **Crie uma Branch para Desenvolvimento**
   ```bash
   git switch -c feature/palindromo-function
   ```
4. **Instale o Node.js (caso ainda não tenha instalado)**  
   - Acesse o site oficial do Node.js: [https://nodejs.org/](https://nodejs.org/).
   - Clique no botão **LTS** (versão recomendada para a maioria dos usuários).
   - Baixe o instalador e execute-o.
   - Siga as instruções do instalador para concluir a instalação.
   - Após a instalação, verifique se o Node.js foi instalado corretamente:
     ```bash
     node -v
     ```
     Esse comando exibirá a versão do Node.js instalada.


5. **Escreva a Função em JavaScript**
   Altere o arquivo `palindromo.js` com o seguinte código:
   ```javascript
   function isPalindromo(palavra) {
     // seu codigo vem aqui
   }

   // Teste
   console.log(isPalindromo("Ana")); // true
   console.log(isPalindromo("JavaScript")); // false
   ```

6. **Teste a Função usando o node**
   Teste sua função com o seguinte comando:
   ```bash
   node palindromo.js   
   ```

7. **Adicione, Commit e Push**
   ```bash
   git add palindromo.js
   git commit -m "Adiciona função de verificação de palíndromo"
   git push origin feature/palindromo-function
   ```

8. **Crie uma Pull Request (PR) no GitHub**
   - Faça o merge da branch `feature/palindromo-function` na `main`.

9. **(Desafio Extra) Resolva um Conflito**
   - Altere o `README.md` no GitHub diretamente na branch `main`.
   - Tente fazer um `git pull` localmente e resolva o conflito.

---

## Dica de Ouro
Use `git stash` se precisar trocar de branch sem perder alterações não commitadas!

---

🔗 **Pronto!** Agora você tem um projeto versionado com Git, integrado ao GitHub e uma função útil em JavaScript. 🚀
