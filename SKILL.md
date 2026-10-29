---
name: varredura-heuristica
description: Roda um fluxo contra as dez heurísticas de Nielsen e devolve as fricções com severidade, lugar exato e a correção proposta. Use antes de levar um desenho para o time, antes de receber um fluxo herdado, e sempre que a pergunta for "onde este fluxo trava".
---

# Varredura heurística

Uma avaliação heurística feita à mão toma o dia e não cabe na semana. Então ela não é feita, e o fluxo vai para o time com fricção que ninguém olhou.

Esta skill faz a varredura em minutos. **O julgamento continua sendo de quem desenha.**

🔴 **O que ela entrega é uma lista de suspeitas ordenada por severidade, não um veredito.** Cada item sai com o lugar exato e a heurística que ele fere, para ser confirmado ou descartado em segundos.

---

## A base, com crédito

As dez heurísticas são de **Jakob Nielsen**, publicadas em 1994 e mantidas pelo Nielsen Norman Group: [10 Usability Heuristics for User Interface Design](https://www.nngroup.com/articles/ten-usability-heuristics/).

A escala de severidade também é dele: [Severity Ratings for Usability Problems](https://www.nngroup.com/articles/how-to-rate-the-severity-of-usability-problems/).

🔴 **Nunca apresentar isto como método próprio.** O método é público e tem autor. O que é próprio é a disciplina de rodar sempre, e o critério de corte.

---

## Como rodar

### 1 · Receber o fluxo inteiro, não a tela

Varredura em tela solta não vale: metade dos problemas de usabilidade mora **entre** as telas, no que o sistema não diz depois que a pessoa agiu.

Peça, nesta ordem: o fluxo completo, quem é a pessoa que entra nele, e o que ela veio fazer. Sem os três, diga que não dá para varrer e pare.

### 2 · Passar as dez, uma por uma

| # | heurística | a pergunta que eu faço |
|:--|:--|:--|
| 1 | Visibilidade do estado do sistema | depois de cada ação, a pessoa sabe o que aconteceu? |
| 2 | Correspondência com o mundo real | a palavra na tela é a palavra dela, ou a do banco de dados? |
| 3 | Controle e liberdade | dá para voltar, desfazer e sair sem perder o que já foi feito? |
| 4 | Consistência e padrões | a mesma coisa se chama igual e fica no mesmo lugar em todas as telas? |
| 5 | Prevenção de erro | o erro é impedido antes, ou só avisado depois? |
| 6 | Reconhecer em vez de lembrar | a informação necessária está na tela, ou foi deixada três telas atrás? |
| 7 | Flexibilidade e eficiência | quem já conhece tem atalho, sem atrapalhar quem é novo? |
| 8 | Estética e design minimalista | o que está competindo com o que importa nesta tela? |
| 9 | Ajudar a reconhecer e resolver erro | a mensagem diz o que houve, por quê, e como sair? |
| 10 | Ajuda e documentação | quando é preciso, a ajuda está no lugar do problema? |

🔴 **Uma heurística sem evidência na tela não vira item.** Se não dá para apontar o lugar, não entra na lista.

### 3 · Classificar a severidade, na escala de Nielsen

| nota | o que significa | o que fazer |
|:--|:--|:--|
| **4 · catastrófico** | impede a tarefa, ou faz perder trabalho | corrigir antes de ir ao ar |
| **3 · grave** | atrasa muito, e muita gente passa por ele | entra no próximo ciclo |
| **2 · menor** | incomoda, mas tem contorno | entra na fila |
| **1 · cosmético** | só se corrige se sobrar tempo | pode esperar |
| **0** | não é problema | sai da lista |

A severidade combina **frequência**, **impacto** e **persistência**. Um problema raro mas que trava a tarefa vale mais que um frequente e contornável.

### 4 · A saída

Uma linha por achado, nesta forma:

```
[severidade] tela ou passo · heurística ferida
o que a pessoa vê · por que isso trava · a correção proposta
```

Ordenada por severidade, nunca por ordem de tela.

E no fim, **as três que mudam mais**, destacadas. Uma lista de trinta itens sem prioridade é uma lista que ninguém usa.

---

## 🔴 Os limites, que vão escritos na entrega

1. **Isto não substitui teste com usuário.** Heurística encontra o que fere princípio conhecido. Ela não descobre o que a pessoa realmente quer, nem por que ela desistiu. O próprio Nielsen Norman Group escreve, em [How to Conduct a Heuristic Evaluation](https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/) (Kate Moran e Kelley Gordon, 2023): *"heuristic evaluations cannot replace user research"*.

2. **Um avaliador só não dá conta.** A recomendação do NN/g, no mesmo artigo, é de **três a cinco pessoas avaliando de forma independente**, porque cada uma deixa passar uma parte dos problemas. Esta skill é um desses avaliadores, não os cinco.

3. **Toda nota de severidade é opinião informada**, não medida. Ela se discute.

4. **Falso positivo existe e é comum.** Uma quebra deliberada de padrão pode ser decisão de produto, e a varredura não sabe disso. Por isso ela devolve suspeitas, e quem desenha valida.

🔴 **Nunca mandar a lista crua para o time.** Ela passa pelo meu olho primeiro, e o que não se sustenta sai antes de a reunião começar.

---

## O que nunca fazer

- **Não varrer protótipo sem estado.** Sem erro, sem vazio e sem carregamento, metade das heurísticas não tem o que avaliar. Diga isso em vez de entregar meia varredura.
- **Não transformar achado em redesign.** A varredura aponta a fricção e propõe a correção mínima. Redesenhar é outro trabalho, com outro briefing.
- **Não contar item para impressionar.** Trinta achados cosméticos valem menos que três graves.
