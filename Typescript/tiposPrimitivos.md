# Tipos primitivos no TypeScript

- Assim como no Js os tipos primitivos são aqueles mais básicos e utilizados;
- São aqueles que aparecem utilizando o **typeof** no Js;

### Principais tipos primitivos

#### Boolean

- Valores **true** ou **false**;

```ts
// Exemplo
let exemplo: boolean = true
```

#### Number

- Números **inteiros** e de **ponto flutuante**;

```ts
// Exemplo
let exemplo: number = 10
```

#### String

- Valores de **texto**;

```ts
// Exemplo
let exemplo: string = "hello world"
```

#### Array

- São **listas de dados**;
  - A sintaxe básica para especificar um **array** é utilizando o **tipo** dos seus **elementos**:
    ```ts
    // Exemplo
    let exemplo: number[] = [1, 2, 3, 4]
    // Ou
    let exemplo2: Array<number> = [1, 2, 3, 4]
    ```
  - Idealmente usamos **arrays** sendo uma lista onde todos os elementos tem o mesmo **tipo**, mas esse comportamento também pode ser evitado
