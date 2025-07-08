
# 📘 Explicativo do Código C# – Estruturas de Repetição e Menu Interativo

Este código é um estudo prático sobre estruturas de repetição em C#, incluindo `for`, `while`, `do-while`, e o uso de `switch` com um menu interativo. Abaixo, explicamos cada parte do código, incluindo os trechos comentados.

---

## 🧠 1. Introdução

```csharp
// See https://aka.ms/new-console-template for more information
// Estudo de estruturas de repetição
```

- Comentário introdutório indicando que o código é baseado no template padrão do .NET.
- O objetivo do script é estudar estruturas de repetição.

---

## 🔁 2. Estrutura de Repetição `for`

```csharp
//int numero = 5;

//Console.WriteLine($"{numero} X 1 = {numero * 1}");
/*
for (int contador = 0; contador <= 10; contador++)
{
    Console.WriteLine($"{numero} X {contador} = {numero * contador}");
}
*/
```

- Define um número fixo (`numero = 5`) e imprime sua tabuada de 0 a 10.
- Utiliza a estrutura `for`, ideal quando se sabe o número de repetições.
- Comentado para fins de estudo.

---

## 🔄 3. Estrutura de Repetição `while`

```csharp
/*
int contador = 0;

while (contador <= 10)
{
    Console.WriteLine($"{numero} X {contador} = {numero * contador}");
    contador++;
}
*/
```

- Alternativa ao `for`, usando `while`.
- Executa enquanto a condição `contador <= 10` for verdadeira.
- Também comentado para fins de comparação.

---

## ⛔ 4. Interrupção com `break`

```csharp
/*
int contador = 1;

while (contador <= 10)
{
    Console.WriteLine($"{numero} X {contador} = {numero * contador}");
    contador++;
    if (contador == 6)
    {
        break;
    }
}
*/
```

- Demonstra o uso do `break` para interromper o loop antes do fim natural.
- O loop para quando `contador == 6`.

---

## 🔂 5. Estrutura `do-while` com entrada do usuário

```csharp
/*
int soma = 0, numero = 0;

do
{
    Console.WriteLine("Digite um número: (0 para parar) ");
    numero = Convert.ToInt32(Console.ReadLine());

    soma += numero;
    Console.WriteLine($"Total da soma dos números digitados é : {soma}");

} while (numero != 0);
*/
```

- Usa `do-while` para garantir que o bloco seja executado ao menos uma vez.
- Solicita números ao usuário até que ele digite `0`.
- Soma os valores digitados e exibe o total.

---

## 📋 6. Menu Interativo com `switch`

```csharp
string opcao;
bool exibirMenu = true;

while (exibirMenu)
{
    Console.Clear();
    Console.WriteLine("Digite a sua opção: ");
    Console.WriteLine("1 - Cadastrar cliente");
    Console.WriteLine("2 - Buscar cliente");
    Console.WriteLine("3 - Apagar cliente");
    Console.WriteLine("4 - Encerrar");

    opcao = Console.ReadLine();

    switch (opcao)
    {
        case "1":
            Console.WriteLine("Cadastro do cliente");
            break;
        case "2":
            Console.WriteLine("Busca do cliente");
            break;
        case "3":
            Console.WriteLine("Apagar cliente");
            break;
        case "4":
            Console.WriteLine("Encerrar");
            //Environment.Exit(0);
            exibirMenu = false;
            break;
        default:
            Console.WriteLine("Opção inválida");
            break;
    }
}
Console.WriteLine("O Programa se encerrou");
```

### 🔹 Explicação:

- Um menu simples é exibido em loop até que o usuário escolha a opção "4".
- `Console.Clear()` limpa a tela a cada iteração.
- O `switch` trata as opções digitadas:
  - `"1"`: Cadastrar cliente
  - `"2"`: Buscar cliente
  - `"3"`: Apagar cliente
  - `"4"`: Encerra o programa
  - Qualquer outro valor: mensagem de erro

---

## ✅ 7. Considerações Finais

- O código é um ótimo exemplo didático para entender estruturas de repetição e controle de fluxo.
- Os trechos comentados permitem testar diferentes abordagens sem interferir no funcionamento principal.
- O menu interativo é uma aplicação prática de `while` + `switch`.

---
