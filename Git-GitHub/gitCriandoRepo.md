# Criando um Novo Repositório Git

## Criando um Repositório Local

A primeira etapa é criar uma pasta para o nosso projeto. Podemos fazer isso diretamente no terminal:

    mkdir meu-projetocd meu-projeto

Isso vai criar e acessar uma pasta chamada "meu-projeto". Agora dentro dessa pasta, vamos inicializar o repositório Git com o comando `git init`:

    git init

Esse comando cria uma série de arquivos ocultos que vão registrar todas as alterações que fizermos nos arquivos dessa pasta. O Git mantém um histórico com "snapshots" de cada versão dos arquivos, permitindo voltar para qualquer ponto anterior se necessário.

Se listarmos os arquivos com `ls`, não vamos ver nenhum arquivo porque eles estão ocultos. Mas se entrarmos na pasta `.git` com `cd .git`, vamos encontrar toda a estrutura interna que o Git criou:

    cd .gitls

Dentro da pasta `.git` temos subpastas como `branches`, `hooks`, `objects` etc. Não precisamos mexer nesses arquivos manualmente, o Git gerencia tudo automaticamente.

## Adicionando Arquivos

Agora que temos um repositório Git inicializado, podemos começar a adicionar arquivos ao projeto.

Vamos criar um arquivo README.md com informações gerais sobre o projeto:

    echo "Bem-vindo ao meu projeto Git" > README.md

Para visualizar as alterações no repositório, usamos o comando `git status`:

    git status

Ele vai mostrar que existe um arquivo não rastreado chamado README.md. Isso significa que o Git ainda não está monitorando esse arquivo.

Para começar a monitorar, precisamos adicioná-lo à área de staging com `git add`:

    git add README.md

Agora o Git sabe que esse arquivo faz parte do projeto, mas ainda não registramos as alterações, apenas adicionamos à área de staging. Para efetivamente registrar no histórico de versões, usamos o comando `git commit`:

    git commit -m "Adicionado README inicial"

O parâmetro `-m` permite adicionar uma mensagem descritiva ao commit. É uma boa prática sempre escrever mensagens claras e objetivas.

## Ver Histórico de Commits

A cada commit, o Git salva um "snapshot" do projeto naquele momento. Para visualizar o histórico de commits, utilizamos o comando `git log`:

    git log

Ele retorna informações como o hash (identificador único), o autor, data e a mensagem de cada commit realizado.

À medida que formos adicionando novos arquivos e fazendo commits, todo o histórico será registrado pelo Git. Isso permite comparar versões, desfazer alterações, ver quem modificou o quê, entre outros recursos muito úteis.

## Branches no Git

Um conceito importante no Git são as branches (ramificações). Elas permitem criar fluxos de trabalho isolados para desenvolver novas features ou testar ideias sem impactar a branch principal (normalmente chamada de main ou master).

Por padrão, todo repositório Git tem uma branch principal. Para visualizar em qual branch estamos atualmente, utilizamos o comando `git branch`:

    git branch

Isso vai mostrar a branch atual com um asterisco ao lado do nome.

Para criar uma nova branch, basta fornecer um nome após o comando `git branch`:

    git branch nova-feature

Agora temos duas branches: main e nova-feature. Para mudar entre elas, usamos `git checkout`:

    git checkout nova-feature

Todas as alterações que fizermos agora serão isoladas na branch nova-feature. Podemos alternar livremente entre elas com `git checkout`.

As branches permitem separar o desenvolvimento por contexto: correções de bugs, novas features, experimentos, etc. Depois podemos mesclar uma branch na principal quando o trabalho estiver pronto para ser integrado.

## Resumo

Neste ebook você aprendeu os principais comandos para iniciar um repositório Git e começar a versionar arquivos. Viu na prática como criar branches para separar o trabalho e como registrar commits com histórico de alterações.

O Git é uma ferramenta poderosa para gerenciar projetos de desenvolvimento e trabalhar em equipe. Valendo dominar bem seus recursos desde o início para aproveitar todo seu potencial.

Espero que este material sirva de guia para seus primeiros passos com Git. Leia também nossos outros ebooks com dicas e melhores práticas para se tornar mais produtivo com essa excelente ferramenta.
