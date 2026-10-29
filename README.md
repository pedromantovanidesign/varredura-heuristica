# varredura heurística

Roda um fluxo contra as dez heurísticas de Nielsen e devolve as fricções com severidade, lugar exato e correção proposta.

Uma skill para o [Claude Code](https://claude.com/claude-code). Não é um script: é **critério de trabalho escrito por extenso**, para que a decisão seja a mesma na segunda-feira e na sexta.

## Por que ela existe

Uma avaliação heurística feita à mão toma o dia e não cabe na semana. Então ela não é feita, e o fluxo vai para o time com fricção que ninguém olhou.

Esta skill faz a varredura em minutos. O julgamento continua sendo de quem desenha.

## O método, com crédito

As dez heurísticas são de **Jakob Nielsen**, 1994, mantidas pelo [Nielsen Norman Group](https://www.nngroup.com/articles/ten-usability-heuristics/). A escala de severidade também é dele.

🔴 **O método é público e tem autor. O que é próprio é a disciplina de rodar sempre, e o critério de corte.**

## O que ela devolve

Uma linha por achado, com severidade de 0 a 4, a tela, a heurística ferida, o que a pessoa vê, por que trava e a correção proposta. Ordenada por severidade, com as três que mudam mais destacadas.

## O que ela NÃO faz

Não substitui teste com usuário: o próprio NN/g escreve que *"heuristic evaluations cannot replace user research"*. A recomendação deles é de três a cinco avaliadores independentes, e esta skill é um deles, não os cinco. Toda severidade é opinião informada, não medida. Falso positivo existe: ela devolve suspeitas, e quem desenha valida.

## O que tem aqui

```
SKILL.md    a skill inteira, que é o que o Claude lê
README.md   este arquivo
LICENSE     MIT
```

## Instalar

```bash
git clone https://github.com/SEU-USUARIO/varredura-heuristica.git ~/.claude/skills/varredura-heuristica
```

O Claude Code carrega a skill sozinho quando o assunto aparece, ou com `/varredura-heuristica`.

---

Escrito e mantido por [Pedro Mantovani](https://pedromantovani.com) · Product & Brand Designer
