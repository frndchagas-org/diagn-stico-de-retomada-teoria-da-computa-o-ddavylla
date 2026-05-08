[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/zHqjFsRx)
# Diagnóstico de retomada - Teoria da Computação

Esta atividade serve para mapear o que você já domina sobre linguagens formais, autômatos, gramáticas e computabilidade.

Responda individualmente. Use suas palavras. Se usar IA depois da primeira tentativa, registre o uso na seção 7.

## 1. Mapa do que eu lembro

Marque cada tópico como: lembro bem, lembro parcialmente, não lembro, nunca vi ou não tenho certeza.

- alfabeto: lembro bem
- cadeia: lembro bem
- linguagem:lembro bem
- gramática:lembro bem
- autômato finito: lembro parcialmente
- linguagem regular: lembro parcialmente
- linguagem livre de contexto: lembro parcialmente
- linguagem sensível ao contexto: lembro parcialmente
- linguagem irrestrita:lembro parcialmente
- hierarquia de Chomsky: não lembro
- computabilidade: não lembro
- máquina de Turing:lembro parcialmente

## 2. Definições com exemplo

Explique, com suas palavras e com um exemplo simples, usando o alfabeto `Sigma = {a, b}`.

1. O que é um alfabeto? É um conjunto de símbolos ou caracteres, a unidade fundamental para a construção de estruturas maiores.
2. O que é uma cadeia? É uma sequência de símbolos escolhidos a partir de um alfabeto específico.
3. O que é uma linguagem? É um agrupamento de cadeias que compartilham uma propriedade em comum.
4. O que é uma gramática? É o conjunto de regras estruturais de uma linguagem. Ela estabelece como os símbolos podem ser combinados, como um molde.

## 3. Linguagens

Considere as linguagens:

```text
L1 = { w em {0,1}* | w termina com 01 }
L2 = { a^n b^n | n >= 0 }
L3 = { a^n b^n c^n | n >= 0 }
```

Para cada linguagem:

1. escreva três palavras que pertencem à linguagem;
   L1: 01; 101; 1101; terminam com 01
   L2: ab; aabb; aaabbb. mesma quantidade de a e b.
   L3: abc; aabbcc; aaabbbccc. mesma quantidade de a, b e c.
3. escreva duas palavras que não pertencem;
   L1: 10 e 111. não terminam em 01.
   L2: abb; aabbb. quantidades diferentes de a e b.
   L3: aabc; abbc; quantidades diferentes de a, b e c.
5. diga, se souber, em qual classe ela provavelmente se encaixa;
   L1: Regular pois é uma linguagem simples, com apenas 1 padrão.
   L2: livre de contexto pois usa uma memória simples.
   L3: acho que sensível ao contexto pois precisa de um pouco mais de memória que L2.
8. explique o motivo em linguagem simples.

Não há problema em dizer "não sei". Nesse caso, escreva o que te deixou em dúvida.

## 4. Autômato finito

Considere o autômato abaixo, sobre o alfabeto `{0,1}`:

```text
Estados: q0, q1, q2
Estado inicial: q0
Estado final: q2

Transições:
q0 --0--> q1
q0 --1--> q0
q1 --0--> q1
q1 --1--> q2
q2 --0--> q1
q2 --1--> q0
```

Responda:

1. Qual linguagem esse autômato parece reconhecer? cadeias que terminam em 01
2. Execute manualmente as cadeias abaixo e diga se aceita ou rejeita:
   - `01` - aceita
   - `101` - aceita
   - `100` - rejeita
   - `1101` - aceita
   - `111` - rejeita
3. Monte uma tabela curta mostrando o caminho dos estados para pelo menos duas cadeias.
   
   CADEIA 01
| Símbolo | Estado |
| ------- | -------|
| início  | q0     |
| 0       | q1     |
| 1       | q2     |

  CADEIA 100
| Símbolo | Estado |
| ------- | -------|
| início  | q0     |
| 1       | q0     |
| 0       | q1     |
| 0       | q1     |


## 5. Gramática

Considere a gramática:

```text
S -> aS
S -> b
```

Responda:

1. Gere cinco cadeias produzidas por essa gramática.
   b; ab; aab; aaab e aaaab.
3. Descreva a linguagem em palavras.
   Forma cadeias com 0 ou mais "a" e um unico "b" no final.
5. Essa gramática parece regular, livre de contexto ou outra classe? Justifique de forma simples.
   Regular, é uma regra simples sem complexidade, e sem contas.

## 6. Ponto de dificuldade

Escolha um tópico da lista inicial e escreva:

1. o que você entende dele; A Máquina de Turing é tipo um modelo teórico de computador que serve para representar um algoritmo.
2. onde você se confunde; 
3. que tipo de explicação ajudaria: desenho, exemplo, exercício guiado, analogia, prova passo a passo ou lista curta. Um passo a passo de um exemplo prático

## 7. Uso de IA, se houver

Se você usou IA depois da primeira tentativa, registre:

```text
Pergunta feita: perguntei sobre o caminho dos estados para fazer a tabela e sobre as classes de linguagens.
Resumo da resposta: me deu as tabelas da questão 4 e sobre as classes respondeu:
Resumo simples (escadinha)

Regular → Livre de contexto → Sensível ao contexto → Recursivamente enumerável
(simples → mais complexa)
Como eu verifiquei:
O que eu alterei na minha resposta: apenas simplifiquei as tabelas
O que ainda não entendi:
```

## Submissão no Moodle

Depois de finalizar, copie no Moodle:

```text
Repositório:
Commit final:
Autoavaliação: nível atual, maior dificuldade e tópico que precisa ser retomado.
```
