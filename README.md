# Desafio: Scripts Python — Fundamentos

Este repositório reúne **scripts Python simples** criados para exercitar conceitos fundamentais de programação: manipulação de strings, repetição, entrada de dados e operações aritméticas básicas. O objetivo é consolidar habilidades essenciais para qualquer desenvolvedor e demonstrar como ferramentas assistivas — como o **GitHub Copilot** — podem acelerar e melhorar o fluxo de desenvolvimento.

---

# Como o GitHub Copilot ajudou

* **Geração rápida de snippets**: sugestões automáticas de trechos repetitivos (leitura de `input`, conversão de tipos, tratamento de erros).
* **Melhores práticas**: lembra de adicionar checagens comuns (ex.: `if num2 != 0`) ou conversões (`str()`), reduzindo bugs triviais.
* **Iteração acelerada**: ao experimentar variações (formatar saída, linhas por repetição), o Copilot ofereceu alternativas que serviram de base para ajustes rápidos.

---

# Objetivos e soluções implementadas

## 1 - Concatenando Dados

**Descrição:** Criar um script que recebe dois dados diferentes e concatena-os em uma única string.

**Skills trabalhadas:**

* Manipulação de strings
* Concatenação
* Entrada de dados

**Status:** ✅ Concluído

**Exemplo de implementação (arquivo: `concatenacao.py`):**

```python
# concatenacao.py
# Recebe dois dados do usuário e concatena como string

dado1 = input("Digite o primeiro dado: ")
dado2 = input("Digite o segundo dado: ")

# Garantir que ambos sejam strings e concatenar com espaço
resultado = f"{dado1} {dado2}"

print(resultado)
```

---

## 2 - Repetindo textos

**Descrição:** Solicitar uma string e um número inteiro e retornar a string repetida o número de vezes informado.

**Skills trabalhadas:**

* Manipulação de strings
* Números inteiros
* Repetição/múltiplas repetições
* Entrada de dados

**Status:** ✅ Concluído

**Exemplo de implementação (arquivo: `repeticao.py`):**

```python
# repeticao.py
# Recebe uma string e um número inteiro e repete a string

texto = input("Digite uma string: ")
try:
    vezes = int(input("Digite um número inteiro (>= 0): "))
except ValueError:
    print("Entrada inválida: informe um número inteiro.")
    raise

if vezes < 0:
    print("Número negativo informado. Usando 0 repetições.")
    vezes = 0

resultado = texto * vezes
print(resultado)
```

> Observação: se `vezes` for `0` ou negativo, o comportamento é controlado (retorna string vazia ou normaliza para 0).

---

## 3 - Operações Matemáticas Simples

**Descrição:** Receber dois números e mostrar o resultado das operações matemáticas básicas.

**Skills trabalhadas:**

* Operações matemáticas com dados
* Entrada de dados

**Status:** ✅ Concluído

**Exemplo de implementação (arquivo: `operacoes.py`):**

```python
# operacoes.py
# Lê dois números e exibe soma, subtração, multiplicação e divisão

try:
    num1 = float(input("Digite o primeiro número: "))
    num2 = float(input("Digite o segundo número: "))
except ValueError:
    print("Entrada inválida: informe números válidos.")
    raise

soma = num1 + num2
subtracao = num1 - num2
multiplicacao = num1 * num2
if num2 != 0:
    divisao = num1 / num2
else:
    divisao = "Erro: divisão por zero"

print(f"Soma: {soma}")
print(f"Subtração: {subtracao}")
print(f"Multiplicação: {multiplicacao}")
print(f"Divisão: {divisao}")
```

---
