Este é um problema clássico que utiliza as propriedades de **conjugados de irracionais** e sequências recorrentes. Para determinar o limite da parte fracionária, precisamos observar o comportamento de **$(2 + \sqrt{3})^n$** em relação ao seu "parceiro" conjugado.

O limite é  **1** .

### O Raciocínio Passo a Passo

Seja **$x = 2 + \sqrt{3}$** e seu conjugado **$y = 2 - \sqrt{3}$**. Note que:

* **$y \approx 2 - 1,732 = 0,268$**
* Portanto, **$0 < y < 1$**.

#### 1. A Soma das Potências

Considere a soma **$S_n = (2 + \sqrt{3})^n + (2 - \sqrt{3})^n$**.

Pelo Binômio de Newton, ao expandir ambos os termos, as partes que contêm **$\sqrt{3}$** com expoentes ímpares se cancelam, enquanto as partes com expoentes pares (que resultam em números inteiros) se somam. Isso garante que:

$$
S_n = (2 + \sqrt{3})^n + (2 - \sqrt{3})^n \in \mathbb{Z}
$$

Ou seja, a soma de **$x^n$** e **$y^n$** é sempre um **número inteiro** para qualquer **$n$** natural.

#### 2. Relação com a Parte Inteira

Sabemos que **$(2 + \sqrt{3})^n = S_n - (2 - \sqrt{3})^n$**.

Como **$S_n$** é inteiro e **$0 < (2 - \sqrt{3})^n < 1$** (já que **$y < 1$**), temos que:

* **$(2 + \sqrt{3})^n$** é um pouquinho menor que o inteiro **$S_n$**.
* Isso significa que a parte inteira **$\lfloor (2 + \sqrt{3})^n \rfloor$** é igual a **$S_n - 1$**.

#### 3. Cálculo da Parte Fracionária

A definição de parte fracionária é **$\{x\} = x - \lfloor x \rfloor$**. Aplicando ao nosso termo:

$$
\{(2 + \sqrt{3})^n\} = (2 + \sqrt{3})^n - (S_n - 1)
$$

Substituindo **$S_n$** pela sua definição:

$$
\{(2 + \sqrt{3})^n\} = (2 + \sqrt{3})^n - ((2 + \sqrt{3})^n + (2 - \sqrt{3})^n - 1)
$$

$$
\{(2 + \sqrt{3})^n\} = 1 - (2 - \sqrt{3})^n
$$

### Conclusão do Limite

Agora, aplicamos o limite quando **$n \to \infty$**:

Como **$0 < 2 - \sqrt{3} < 1$**, o termo **$(2 - \sqrt{3})^n$** converge para **0** conforme **$n$** cresce.

$$
\lim_{n \to \infty} \{(2 + \sqrt{3})^n\} = \lim_{n \to \infty} (1 - (2 - \sqrt{3})^n) = 1 - 0 = 1
$$

---

**Curiosidade:** Números como **$2 + \sqrt{3}$** são chamados de **Números de Pisot-Vijayaraghavan** (ou simplesmente números de Pisot). Eles têm a propriedade fascinante de que suas potências ficam "arbitrariamente próximas" de números inteiros.

Gostaria de ver como isso se aplica a outros números, como o Número de Ouro (**$\phi$**), ou prefere que eu explique a expansão binomial que garante que **$S_n$** é inteiro?
