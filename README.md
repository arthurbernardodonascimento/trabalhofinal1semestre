# Sistema de Estoque de Supermercado em C - Estudo Individual 🛒

Este é um **projeto de estudo** que desenvolvi para praticar os conhecimentos adquiridos na **Universidade Positivo**. Ele simula o controle de estoque de um pequeno supermercado, usando estruturas de dados e funções em linguagem C.

## 📌 Sobre o Projeto
O programa resolve um problema prático: gerenciar os produtos de um mercado, permitindo consultar os dados, calcular o valor total do estoque e registrar vendas com baixa automática na quantidade disponível.

## 💻 Conceitos Praticados
* **Estruturas Homogêneas (`struct`):** Uso de `typedef struct` para representar um `Produto` (nome, preço, código e quantidade) e de um vetor de produtos.
* **Modularização:** Divisão do programa em funções e procedimentos (`impressao`, `estoque`, `retirada`, `ierro`).
* **Menu Interativo:** Laço `while` com `switch/case` para navegação entre as opções.
* **Manipulação de Vetores:** Percurso e atualização de dados do estoque com `for`.
* **Lógica Aplicada:** Validação de código de produto e de quantidade disponível antes de concluir uma venda.

## 🔍 Funcionalidades
O sistema possui um menu com as seguintes opções:

| Opção | Descrição |
|-------|-----------|
| **[1]** | Lista todos os produtos com preço, código e quantidade |
| **[2]** | Lista o valor em estoque de cada produto e o valor total |
| **[3]** | Cadastro de novo produto (ainda não disponível) |
| **[4]** | Realiza uma venda, descontando a quantidade do estoque |
| **[5]** | Encerra o programa |

### 📦 Produtos Pré-cadastrados
| Código | Produto | Preço (R$) | Quantidade |
|--------|---------|-----------|------------|
| 1 | Chocolate | 15,99 | 6 |
| 2 | Arroz | 23,95 | 22 |
| 3 | Feijao | 24,55 | 19 |
| 4 | Cereal | 12,79 | 15 |
| 5 | Leite | 7,99 | 4 |
| 6 | Pao | 8,95 | 32 |

## 🧮 A Lógica do Cálculo
O valor em estoque de cada produto e o valor total são calculados por:

$$\text{Valor em Estoque} = \sum_{i=1}^{n} \text{Preço}_i \times \text{Quantidade}_i$$

Na venda, o programa só efetua a baixa se a quantidade pedida for menor ou igual à disponível:

$$\text{Nova Quantidade} = \text{Quantidade Atual} - \text{Quantidade Vendida}$$

## ▶️ Como Executar
```bash
gcc AV1_5P_ArthurBernardo_V2.c -o estoque
./estoque
```

## 🔧 Pontos de Melhoria
* Utilizar `#define` para definir o número de produtos como constante (ex.: `#define PDS 6`), evitando o valor fixo no código.
* Inicializar a variável `v` da função `estoque` com `0` para evitar lixo de memória no total.
* Implementar o cadastro de novos produtos (opção 3).

---

> [!IMPORTANT]
> **Diferencial:** Este projeto demonstra a aplicação da programação para resolver problemas do mundo real, unindo lógica, estruturas de dados e tecnologia de forma prática.

---

> [!NOTE]
> **Registro Histórico:** Realizado em **24 de junho de 2024**.
>
> **Autor:** Arthur Bernardo do Nascimento
