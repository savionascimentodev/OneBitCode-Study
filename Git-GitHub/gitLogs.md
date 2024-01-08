# Visualizando Logs no Git

## Introdução

O Git é um sistema de controle de versão distribuído que permite aos desenvolvedores registrar alterações em seus códigos-fonte ao longo do tempo. À medida que um projeto cresce, especialmente se muitas pessoas estão contribuindo com ele, visualizar o histórico desses commits (confirmações de alterações) se torna essencial.

Felizmente, o Git possui comandos poderosos para exibir logs - um registro de toda atividade de commit que ocorreu em um repositório. Esses logs não apenas mostram quais alterações foram feitas, mas também quem as fez e quando.

Neste ebook, vamos explorar em profundidade os comandos de log do Git, incluindo:

- git log - Exibe logs de commit
- git log -p - Mostra diferenças introduzidas em cada commit
- git log --stat - Exibe estatísticas de alteração de arquivo por commit
- git log --pretty=oneline - Formata a saída do log em uma linha por commit
- git log --graph --all --decorate - Exibe um gráfico de histórico de branch

Ao final deste guia, você estará apto a navegar pelo histórico de commit de qualquer repositório Git e entender o que aconteceu e quando. Isso lhe dará maior controle e contexto à medida que você e sua equipe colaborarem em projetos.

## Por que visualizar logs no Git

Antes de mergulharmos nos comandos específicos, vamos discutir por que visualizar logs do Git é tão importante.

Aqui estão alguns dos principais motivos pelos quais você desejará visualizar logs do Git regularmente:

### Entender o que mudou

Os logs do Git mostram exatamente quais arquivos foram alterados, por quem e quando. Isso fornece contexto inestimável sobre como o código evoluiu ao longo do tempo e por que certas decisões foram tomadas.

### Encontrar bugs introduzidos

Se um bug for introduzido em algum ponto, você pode percorrer o log para identificar quando foi introduzido e por quem. Isso torna muito mais fácil desfazer, consertar e aprender com o erro.

### Ver contribuições de membros da equipe

Se você estiver trabalhando em uma equipe, visualizar logs ajudará você a ver quem fez o quê. Isso torna mais fácil atribuir crédito e também coordenar para que vários desenvolvedores não sobrescrevam o trabalho uns dos outros.

### Entender o propósito por trás das alterações

As mensagens de commit que acompanham cada confirmação de alteração geralmente explicam por que uma mudança foi feita. Os logs tornam fácil ver o histórico dessas mensagens.

### Encontrar pontos na história para voltar

Se você precisar reverter o código para um estado anterior, os logs do Git permitirão encontrar commits anteriores aos quais você pode redefinir.

Como você pode ver, há uma infinidade de razões pelas quais a visualização dos logs do Git deve se tornar uma parte regular do seu fluxo de trabalho. Agora vamos ver exatamente como fazer isso.

## O comando git log básico

O comando mais básico para visualizar o histórico de commit de um repositório é simplesmente `git log`:

    git log

Isso imprimirá cada commit feito no branch atual, começando pelo mais recente.

A saída de `git log` parece algo como isto:

    commit abc123def456fgh789Author: John Doe <john@example.com>Date:   Thu Jul 16 11:04:13 2020 -0700    Fix typo in index pagecommit def456abc123fgh789  Author: Jane Doe <jane@example.com>Date:   Wed Jul 15 17:23:41 2020 -0700    Improve styling for footer

Cada commit é listado com um hash SHA exclusivo como ID, junto com informações sobre quem fez o commit e quando, e a mensagem de commit explicando suas alterações.

Por padrão, a saída do `git log` pagina para que você possa rolar pelo histórico. Pressione `Enter` para avançar e `q` para sair quando terminar.

### Limitando a saída do log

Para repositórios muito ativos, a saída do `git log` pode se estender indefinidamente. Você pode limitar o número de commits exibidos adicionando o argumento `-n`:

    git log -n 5

Isso mostrará apenas os 5 commits mais recentes.

## Visualizando mudanças com git log -p

Para ver o que realmente mudou em cada commit, use a opção `-p`:

    git log -p

Isso produzirá uma saída semelhante a esta:

    commit abc123def456fgh789Author: John Doe <john@example.com>Date:   Thu Jul 16 11:04:13 2020 -0700    Fix typo in index pagediff --git a/index.html b/index.html index 3fcb123..d34d456 100644--- a/index.html+++ b/index.html@@ -16,7 +16,7 @@        <h1>Welcome Page</h1>        <p>This is the home page for our website. Check out the            <a href="/about">About</a> and -          <a href="/blog">Blog<a> pages to learn more!+          <a href="/blog">Blog</a> pages to learn more!        </p>     </div> </body>commit def456abc123fgh789Author: Jane Doe <jane@example.com> Date:   Wed Jul 15 17:23:41 2020 -0700    Improve styling for footer

Isso mostra a diferença exata em cada arquivo alterado por um commit, o que é incrivelmente útil para entender exatamente o que mudou.

## Exibindo estatísticas de alteração com git log --stat

Às vezes, você não precisa ver as alterações linha por linha, mas ainda deseja uma visão geral do impacto de um commit. É aí que entra `--stat`:

    git log --stat

Agora a saída se parecerá com:

    commit abc123def456fgh789Author: John Doe    Fix typo in index pageindex.html | 2 +-1 file changed, 1 insertion(+), 1 deletion(-)commit def456abc123fgh789Author: Jane Doe    Improve styling for footerstyles.css | 23 +++++++++++++----------1 file changed, 14 insertions(+), 9 deletions(-)

Isso mostra resumidamente quantas linhas foram alteradas em cada arquivo por um commit, ajudando a dar uma noção do tamanho da alteração.

## Formatando a saída em uma linha por commit

Para obter uma visão ainda mais concisa do histórico, use `--pretty=oneline`:

    git log --pretty=oneline

Agora cada commit ocupará apenas uma linha:

    abc123 Fix typo in index pagedef456 Improve styling for footerghi789 Add new blog post template

Isso torna muito mais fácil percorrer rapidamente o histórico e ter uma noção de alto nível do que mudou.

## Exibindo um gráfico visual de histórico de branch

Para a visualização mais abrangente possível do histórico do seu repositório Git, use:

    git log --all --graph --decorate

Isso mostrará um gráfico do histórico de branch com pontos de merge rotulados:

    *   commit abc123 (HEAD -> master)|\  | * commit def456 (footer-styling)* | commit ghi789|/  * commit jkl101 (tag: v1.0)

Permitindo que você visualize facilmente como os branches divergiram e convergiram ao longo do tempo.

## Conclusão

Neste guia, cobrimos os principais comandos que você usará para visualizar logs no Git:

- `git log` exibe o histórico de commit
- `git log -p` mostra as alterações em cada commit
- `git log --stat` exibe um resumo das estatísticas de alteração
- `git log --pretty=oneline` formata a saída como uma linha por commit
- `git log --all --graph --decorate` mostra um gráfico do histórico do branch

Domine esses comandos e você será capaz de desvendar o que aconteceu em qualquer repositório Git, entender por que e por quem. Isso dará a você e sua equipe muito mais controle e contexto à medida que colaborarem em projetos.

Boa sorte na exploração dos logs do seu repositório!
