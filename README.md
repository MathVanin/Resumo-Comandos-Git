# Resumo sobre utilização básica do GIT
Vamos percorrer alguns comandos essenciais para utilização do GIT via terminal, separaremos por tópicos para faciliar a busca por informações especificas de determinado assunto.

> Por convenção todos os codigos que possuem parametros podem aparecer de duas formas \<NomeParametro> ou [NomeParametro], sendo:
    >- \<NomeParametro> Parametros origatórios
    >- [NomeParametro] Parametros opcionais

1. [Como configurar o GIT e vincular ao GitHub](#como-configurar-o-git-e-vincular-ao-github)

# Como configurar o GIT e vincular ao GitHub
Para configurar o GIT o primeiro passo é configurar as credenciais de acesso, para isso utilizaremos o comando [`git config`](#git-config) e alguns de seus parametros

1. Execute `git config --global user.name "<NomeDeUsuario>"`

2. Execute `git config --global user.email <EmailDoUsuario>`
3. Gerar um token na conta do GitHub
4. Ter ao menos um repositorio para ser clonado na sua conta GitHub
5. Execute `git config --global credential.helper store`
6. Execute `git clone <Link-do-repositorio>`
7. Digite seu usuario GitHub
8. Cole o token gerado no passo 3

Pronto, seu GIT está vinculado a sua conta GitHub


## Comando git config

Utilizado para configurar o GIT, pode receber diversos parametros

### Informações do usuario
- Configurar email do usuário
    >`git config [Local-Configuracao] user.name <Usuario>`
- Configurar nome do usuário
    >`git config [Local-Configuracao] user.name <Usuario>`
- Exibir o nome do usuário configurado
    >`git config user.name`
- Exibir o e-mail do usuário configurado
    >`git config user.email`
- Exibir a branch padrão, criada ao utilizar o comando `git init`
    >`git config init.defaultBranch`
- Alterar a branch padrão
    >`git config init.defaultBranch <NomeBranch>`
- Listar as configurações
    >`git config [Local-Configuracao] --list`
- Definir armazenamento de credenciais
    >`git config [Local-Configuracao] credential.helper <store|cache>`

### Local do arquivo de configuração
Parametro para definir o local da configuração de usuário

|Parametro|Ação|
|-|-|
|--global|Utiliza arquivo de configuração global|
|--system|Utiliza arquivo de configuração do sistema|
|--local|Utiliza arquivo de configuração do repositório|
|--worktree|Utiliza arquivo de configuração por árvore de trabalho|
|-f, --file \<File>|Utiliza arquivo de configuração passado como parâmetro|
|--blob \<blob-id>|Lê configurações de um objeto blob|