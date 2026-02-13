20 sapatos, provenientes de 10 pares de sapatos, são enfileirados aleatoriamente. Qual é a probabilidade de que na fila haja um conjunto de 10 sapatos consecutivos com 5 sapatos esquerdos e 5 sapados direitos?

---

Este é um problema clássico de combinatória que envolve uma simetria elegante. À primeira vista, parece exigir cálculos exaustivos de todas as combinações de 10 sapatos, mas a solução reside na aplicação do **Princípio da Casa dos Pombos** (ou apenas uma análise de variação contínua).

A probabilidade é **1** (ou seja,  **100%** ). Isso sempre acontecerá, independentemente da ordem dos sapatos.

### A Explicação Lógica

Vamos definir uma função para analisar qualquer sequência de 10 sapatos consecutivos:

1. Imagine os 20 sapatos em fila. Seja **$E$** um sapato esquerdo e **$D$** um sapato direito. No total, temos 10 **$E$** e 10 **$D$**.
2. Considere uma "janela" que cobre os primeiros 10 sapatos (da posição 1 à 10). Seja **$f(1)$** a diferença entre o número de sapatos esquerdos e direitos nessa janela (**$f = N_E - N_D$**).
3. Agora, deslize essa janela uma posição por vez até o final (posição 11 à 20).

### O Comportamento da Janela

* **Na primeira posição (1 a 10):** Suponha que temos **$k$** sapatos esquerdos. Então temos **$10-k$** sapatos direitos. A diferença é **$f(1) = k - (10-k) = 2k - 10$**.
* **Na última posição (11 a 20):** Como o total de sapatos esquerdos no conjunto inteiro de 20 é exatamente 10, se a primeira metade tinha **$k$** esquerdos, a segunda metade **obrigatoriamente** terá **$10-k$** esquerdos.
* A diferença na última janela será **$f(11) = (10-k) - k = 10 - 2k$**.

Observe que **$f(11) = -f(1)$**. Ou seja, se a primeira janela tem mais sapatos esquerdos, a última terá mais direitos (ou vice-versa), ou ambas serão zero.

---

### Por que a soma 5+5 é inevitável?

Ao deslizar a janela uma posição por vez, a diferença **$f(i)$** só pode mudar de três formas:

* **Permanece igual:** Se o sapato que sai da janela é igual ao que entra (sai **$E$**, entra **$E$** ou sai **$D$**, entra **$D$**).
* **Muda por 2:** Se sai um **$E$** e entra um **$D$** (a diferença cai 2), ou se sai um **$D$** e entra um **$E$** (a diferença sobe 2).

Como a função **$f(i)$** começa em um valor **$X$** e termina em **$-X$**, e ela só muda em passos de 2 ou 0 (ela nunca "pula" um número ímpar se começou par), ela **obrigatoriamente terá que passar pelo zero** para chegar ao lado oposto do espectro.

> Quando **$f(i) = 0$**, significa que o número de sapatos esquerdos é igual ao de direitos. Como a janela tem 10 sapatos, isso implica em  **5 esquerdos e 5 direitos** .

---

Como esse resultado é puramente matemático e baseado na paridade, ele funciona para qualquer par de elementos opostos em uma sequência equilibrada.

Gostaria que eu aplicasse esse mesmo raciocínio para um problema com um número diferente de sapatos ou talvez para outra variação de probabilidade?
