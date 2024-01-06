# Estruturas de Controle

## Estruturas Condicionais: IF e ELSE

As estruturas condicionais são usadas para controlar o fluxo de execução de um programa. Elas permitem que o programador execute um bloco de código somente quando uma determinada condição for verdadeira.

A estrutura condicional mais básica é o **IF**, que tem a seguinte sintaxe:

```js
if (condicao) {
// bloco de código a ser executado quando a condição for verdadeira
}

// Por exemplo, o seguinte código irá imprimir "O número é par" se o número for par:

int numero = 2;

if (numero % 2 == 0) {
printf("O número é par");
}
```

A estrutura condicional **ELSE** pode ser usada para acrescentar um bloco de código que será executado quando a condição for falsa. A sintaxe é a seguinte:

```js
if (condicao) {
// bloco de código a ser executado quando a condição for verdadeira
} else {
// bloco de código a ser executado quando a condição for falsa
}

// Por exemplo, o seguinte código irá imprimir "O número é ímpar" se o número for ímpar:

int numero = 3;

if (numero % 2 == 0) {
printf("O número é par");
} else {
printf("O número é ímpar");
}
```

A estrutura condicional **ELSE IF** pode ser usada para acrescentar mais de uma condição. A sintaxe é a seguinte:

```js
if (condicao1) {
// bloco de código a ser executado quando a condição1 for verdadeira
} else if (condicao2) {
// bloco de código a ser executado quando a condição2 for verdadeira
} else {
// bloco de código a ser executado quando nenhuma das condições for verdadeira
}

// Por exemplo, o seguinte código irá imprimir "O número é par", "O número é ímpar" ou "O número é zero", dependendo do valor do número:

int numero = 0;

if (numero == 0) {
printf("O número é zero");
} else if (numero % 2 == 0) {
printf("O número é par");
} else {
printf("O número é ímpar");
}
```

### Operador Ternário

O operador ternário é uma forma abreviada e autoavaliada do **IF ELSE**. A sintaxe é a seguinte:

```js
const resultado = condicao ? resultado_verdadeiro : resultado_falso;

// Por exemplo:

int numero = 0;

const resultado = numero == 0 ? "O número é zero" : "O número é par ou ímpar";
```

### Estruturas Condicionais: SWITCH

A estrutura condicional **SWITCH** é uma **forma mais compacta de escrever condições múltiplas**. Ela permite que o programador execute um bloco de código diferente de acordo com o valor de uma variável ou expressão.

A sintaxe da estrutura SWITCH é a seguinte:

```js
switch (expressao) {
case valor1:
// bloco de código a ser executado quando o valor da expressão for igual a valor1
break;
case valor2:
// bloco de código a ser executado quando o valor da expressão for igual a valor2
break;
...
default:
// bloco de código a ser executado quando o valor da expressão não for igual a nenhum dos valores especificados
}
```

O bloco de código a ser executado é especificado pelo **case**. O valor do case deve ser igual ao valor da expressão. Se o valor da expressão for igual a algum dos valores especificados, o bloco de código correspondente será executado. Se o valor da expressão não for igual a nenhum dos valores especificados, o bloco de código do default será executado.

O **break é uma palavra-chave que indica que o SWITCH deve ser encerrado**. Se o break não for usado, o SWITCH continuará executando os blocos de código dos case subsequentes, até encontrar um break ou o fim do SWITCH.
