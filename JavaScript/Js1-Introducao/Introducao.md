# Fundamentos

## O que é uma Linguagem de Programação

- Conjunto de códigos que contém instruções para o computador;
- Diferente de linguagem de marcação (como HTML, XML, YAML, etc) e de linguagem de estilização (como CSS);
- Podem ser **compiladas** ou **interpretadas**;
- Podem ser de **alto nível** ou de **baixo nível**

## O que é Javascript

- Criada em 1995 por Brendan Eich para ser usada pelo Netscape;
- Não confundir com **Java**;
- Seu nome oficial é **ECMAScript**
- De **alto nível**,**interpretada** e **multiparadigma**;
- Principal linguagem de programação usada pelos navegadores web;
- Junto com HTML e CSS forma as três principais tecnologias da web;
- Também pode ser usada fora dos navegadores através de runtimes como o Node.js;

### Tipos de Dados

No javascript (e em outras linguagens de programação) dados podem ser representados em diferentes formas.

- **string**;
- **number**;
- **boolean**;
- **null e undefined**;
- **objetos e funções**;

#### Criando variáveis

Váriaveis servem para armazenar os dados para podermos usá-los no nosso código.

- **var**;
- **let**;
- **const**;

### Operadores e Expressões

- **Aritméticos: +, -, \*, / e %**;
- **Agrupamento: ( )**;
- **Atribuição: =, +=, -=, \*=, /= e %=**;
- **Encadeamento: .**;
- **Incrementar: ++** e **Decrementar: --**;
- **Concatenação de strings: +**;

### Comentários

Linhas do código que serão ignoradas pelo interpretador, exemplos:

- **Uma linha: //**;
- **Várias linhas: /\* \*/**;

Servem para deixar **anotações**, ajudar a **entender/documnentar** o código.

### Recursos Nativos do Navegador

Objeto que representa o terminal interativo do navegador

- **console**
- **window**
- **document**

##### O objeto `console` **representa o terminal interativo do navegador**. Ele pode ser usado para imprimir mensagens, depurar código e executar comandos.

Algumas funções úteis do `console` incluem:

- **log()**: Imprime uma mensagem no console.
- **info()**: Imprime uma mensagem de informação no console.
- **warn()**: Imprime uma mensagem de aviso no console.
- **error()**: Imprime uma mensagem de erro no console.

##### O objeto **window** representa a aba atual do navegador. Ele pode ser usado para interagir com o DOM, acessar informações sobre a aba e exibir mensagens ao usuário.

Algumas funções úteis do `window` incluem:

- **alert()**: Exibe uma mensagem de alerta ao usuário.
- **confirm()**: Exibe uma mensagem de confirmação ao usuário e retorna um valor booleano.
- **prompt()**: Exibe uma mensagem de prompt ao usuário e retorna uma string.

##### O objeto **document** representa a página HTML atual. Ele pode ser usado para acessar elementos do DOM, alterar o conteúdo da página e executar JavaScript.

Algumas funções úteis do `document` incluem:

- **getElementById()**: Recupera um elemento do DOM pelo seu ID.
- **getElementsByTagName()**: Recupera todos os elementos do DOM com um determinado nome de tag.
- **getElementsByClassName()**: Recupera todos os elementos do DOM com uma determinada classe.

### Comparação de dados

Os operadores de comparação são usados para comparar dois valores e retornar um valor booleano (true ou false). Os operadores de comparação mais comuns são:

- **Igualdade (==)**: Retorna true se os dois valores forem iguais.
- **Estritamente Igual (===)**: Retorna true se os valores dos operandos são iguais e se os tipos dos operandos também são iguais. Este operador verifica tanto o valor quanto o tipo, garantindo uma correspondência precisa.
- **Diferente (!=)**: Retorna true se os dois valores forem diferentes.
- **Maior que (>=)**: Retorna true se o primeiro valor for maior que o segundo.
- **Maior ou igual que (>=)**: Retorna true se o primeiro valor for maior ou igual que o segundo.
- **Menor que (<)**: Retorna true se o primeiro valor for menor que o segundo.
- **Menor ou igual que (<=)**: Retorna true se o primeiro valor for menor ou igual que o segundo.

### Operadores lógicos

Os operadores lógicos são usados para combinar duas ou mais expressões lógicas e retornar um valor booleano. Os operadores lógicos mais comuns são:

- **E (&&)**: Retorna true se ambas as expressões forem verdadeiras.
- **Ou (||)**: Retorna true se pelo menos uma das expressões for verdadeira.
- **Não (!)**: Inverte o valor booleano de uma expressão.
