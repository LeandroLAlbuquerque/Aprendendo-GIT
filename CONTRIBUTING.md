# Aprendendo GIT

## Introdução

Aqui vai um pouco do que estou aprendendo sobre o **Git**  

---

## Sobre o Terminal Git Bash

O **Git Bash** é um terminal que simula um ambiente Linux (Bash) no Windows.  
Por isso, ele aceita comandos como `ls`, `rm`, `mv` e `touch`, que não existem no CMD tradicional do Windows.

Aqui foi a ordem na qual aprendi, e peguei do book disponibilizado para pelo próprio [site oficial do git](https://git-scm.com/book/pt-br/v2)

Abaixo estão alguns comandos básicos utilizados no Git Bash e no Git.

---

## Comandos básicos no Git Bash

Antes de começar a utilizar os comandos de git, é necessário um entendimento bre sobre terminal bash

### Criar um arquivo `.txt`

```bash
touch teste.txt
```

### Remover um arquivo

```bash
rm teste.txt
```

### Renomear um arquivo

```bash
rm teste.txt ofical.txt
```

### Navegar entre diretórios

```bash
cd /c/Users/SeuUsuario/Documents
```

### Leitura do conteúdo

```bash
cat teste.txt
```

>Irá "abrir" o arquivo dentro de um terminal git

### Abrir o comando com Vscode, ou editor de texto que você utiliza

```bash
code teste.txt
```

>Abrirá o arquivo dentro do Vscode, e não no seu editor de texto

### Abrir a pasta do repositório Git direto no explorador

```bash
explore .
```

>Certifique que esteja no diretorio certo caso contrário abra pelo caminho  
> Ex.: explore /c/Users/SeuUsuario/Documentos

---

## Comandos GIT

### Inicializar um repositório GIT

```bash
git init
```

>Inicializa um repositório Git na pasta, criando assim uma pasta .git

### Adicionar os arquivos à área de stage

```bash
git add teste.txt
```

### Criar um commit

```bash
git commit -m "Aqui onde você nomeia a versão"
```

>Cria um snapshot do estado atual dos arquivos versionados.

### Clonar um repositório

```bash
git clone URL_DO_REPOSITORIO
```

>Clona um repositório local ou remoto (por exemplo, do GitHub) para sua máquina.

### Ver o estado do repositório

```bash
git status
```

> #### Mostra
>
> - arquivos modificados
>
> - arquivos novos
>
> - arquivos removidos

### Versão resumida do Status

```bash
git status -s
```

>Legenda do git status -s
>
> - A → Added (adicionado ao stage)
>
> - M → Modified (modificado)
>
> - D → Deleted (removido)
>
> - ?? → Arquivo novo (untracked)

### Para você ver o que mudou no stage

```bash
git diff --staged || git diff --cached
```

### Podemos misturar agora alguns conhecimentos

```bash
git rm --cached teste.txt
```

>Aqui ele retira o arquivo dentro da pasta .git, ela ainda fica visível na pasta principal

### Agora se quisermos excluir dos dois ambientes

```bash
git rm -f teste.txt
```

>Aqui ele retira o arquivo dentro da pasta .git, ela ainda fica visível na pasta principal

### Ver histórico de commits

```bash
git log
```

> Mostra o histórico completo dos commits (hash, autor, data e mensagem).

### Versão resumida do log

```bash
git log --oneline
```

> Adiciona todos os arquivos modificados ou novos à área de preparação (stage)

### Tabela usada para ver as modificações

```bash
git log --stat
```

> Adiciona todos os arquivos modificados ou novos à área de preparação (stage)

### Você pode especificar o próprio formato dos registros

```bash
git log --pretty=format:"%h - %an, %ar : %s"
```

> Aqui existe alguns detalhes a mais onde você deve ficar atento para facilitar sua vida:

| Valor da entrada | Valor da saída            |
| :--------------: | :-----------------------: |
| %h               | Hash do commit abreviado  |
| %an              | nome do autor             |
| %h               | Hash do commit abreviado  |
| %ae              | Email do autor            |
| %s               | Ver os comentários        |
| %cd              | data do commiter          |

>Existem mais opções, porém fica a sua curiosidade procurar, mas como estou aqui para ajudar
>[Aqui você pode verificar os restos dos valores](https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Vendo-o-hist%c3%b3rico-de-Commits#rpretty_format)

### Errou o nome do commit, você consegue modificar a partir do --amend

```bash
git commit -m "Fist commit"
git commit --amend -m "First commit"
```
<!-- Lembre-se de colocar essa tabela por último-->
### Envie para o git hub

```bash
git push -u origin main
```

> Adiciona todos os arquivos modificados ou novos à área de preparação (stage)

---

> #### Oberservação
>
>Quis deixar algumas nomenclaturas em inglês para fomentar mais meu aprendizado. Nada muito elaborado, apenas anotações práticas do dia a dia. [EOF]
