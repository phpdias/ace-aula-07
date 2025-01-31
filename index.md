<style>
  section {
    background: #fff url(./img/background.png) no-repeat center center;
    background-size: cover;
  }

  section.center img {
    display: block;
    margin: auto;
  }

  img[alt=small-img] {
    display: block;
    margin: auto;
    width: 30%;
  }

  .transparent {
    background-color: transparent!important;
  }

  section.transparent img {
    background-color: transparent!important;
  }

  section.ttable table {
    margin: auto;
  }

  .cabecalho {
    position: absolute;
    top: 10%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 48px;
    font-weight: bold;
  }

  .conteudo {
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }

  .conteudo-absoluto {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }
  
  .large {
    font-size: 36px;
  }

  .normal {
    font-size: 22px;
  }
  .regular {
    font-size: 18px;
  }
  .small {
    font-size: 16px;
  }
  .footnotesize {
    font-size: 14px;
  }
  .scriptsize {
    font-size: 12px;
  }
  .tiny {
    font-size: 10px;
  }
  .bold {
    font-weight: bold;
  }
  .center {
    text-align: center;
  }
  section.lead p {
    text-align: justify;
  }
  section.lead h1 {
    text-align: center;
  }
  section.lead h2 {
    text-align: center;
  }
  section.lead h3 {
    text-align: center;
  }
  
  .grid-50-50 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    text-align: justify;
  }

  .grid-25-25-25-25 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    text-align: justify;
  }

  .grid-33-33-33 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    text-align: justify;
  }


  .grid-66-33 {
    display: grid;
    grid-template-columns: 2fr 1fr;
    text-align: justify;
  }

  .grid-33-66 {
    display: grid;
    grid-template-columns: 1fr 2fr;
    text-align: justify;
  }

  .grid-element {
    margin-left: 5%;
    margin-right: 5%;
  }
  img[alt=grid-img] {
    width: 100%;
  }

</style>

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>


# Análise de Circuitos Elétricos
## Aula 07 - Respostas natural e a um degrau em circuitos de segunda ordem (RLC)
 
Prof. M.Sc. Diego Ascânio Santos (ascanio@cefetmg.br)

Aula baseada sobre o material do professor Dr. Emerson Gonçalves de Melo (emerdemelo@usp.br - DEMAR EEL USP), da professora Drª. Thabatta Moreira Alves de Araújo (thabatta@cefetmg.br - DIGDDV) e da Khan Academy.

CEFET-MG DIGDDV - Divinópolis, 2023.


---

## Roteiro

1. Introdução à resposta natural de um circuito RLC em paralelo.
2. Formas de resposta natural de um circuito RLC em paralelo.
3. Resposta a um degrau de um circuito RLC em paralelo.
4. Respostas natural e a um degrau de um circuito RLC em série.


---

## Objetivos

1. Saber determinar a resposta natural e a resposta a um degrau de circuitos RLC em paralelo.
2. Saber determinar a resposta natural e a resposta a um degrau de circuitos RLC em série.


---

## Introdução - Circuitos de Segunda Ordem

Circuitos de segunda ordem são denominados dessa forma devido à presença de dois elementos que armazenam energia (em diversas configurações), cujas tensões e correntes são regidas por equações diferenciais de segunda ordem.

Em outras palavras, a dinâmica de circuitos de segunda ordem é descrita por equações diferenciais que envolvem a segunda derivada temporal de grandezas como tensão e corrente, refletindo como a energia é trocada entre campos elétricos e magnéticos nos capacitores e indutores presentes no circuito.

Estamos interessados em encontrar as EDOs de ordem 2 que descrevem a resposta destes circuitos ao estímulo natural e ao estímulo degrau, considerando sempre as configurações mistas dos elementos armazenadores de energia — circuitos RLC — compostos por resistores, capacitores e indutores.


---

## Introdução

<div class="regular">

- Nesta aula, a discussão da resposta natural e ao degrau está limitada a duas configurações: o circuito RLC em paralelo e o circuito RLC em série.

<div class="grid-25-25-25-25">

<div class="grid-element scriptsize">

A resposta natural de um circuito RLC em paralelo consiste em determinar a tensão criada nos ramos em paralelo pelo fornecimento de energia armazenada no indutor ou no capacitor ou em ambos, como na figura 1.

</div>
<div class="grid-element">
<figure>

<!-- _class: transparent -->
![grid-img](./img/circuito-rlc-paralelo-natural.png)

<figcaption class="center tiny">

Figura 1: Circuito que ilustra a resposta natural de um circuito \\(RLC\\) paralelo.

</figcaption>

</figure>
</div>

<div class="grid-element scriptsize">

Ao aplicar repentinamente uma fonte de corrente contínua (estímulo degrau) em um circuito \\(RLC\\) em paralelo, busca-se entender a tensão nos ramos paralelos, considerando a energia inicial no circuito em \\(t_{0}\\). A representação desse processo é mostrada na figura 2.

</div>

<div class="grid-emelent">
<figure>

<!-- _class: transparent -->
![grid-img](./img/circuito-rlc-paralelo-degrau.png)

<figcaption class="center tiny">

Figura 2: Circuito que ilustra a resposta ao degrau de um circuito \\(RLC\\) paralelo.

</figcaption>

</figure>
</div>

</div>

<div class="grid-25-25-25-25">

<div class="grid-element scriptsize">

A resposta natural de um circuito RLC em série consiste em determinar a corrente gerada nos elementos em série pela descarga (fornecimento) da energia armazenada no indutor, no capacitor ou em ambos, como na figura 3.

</div>
<div class="grid-element">
<figure>

<!-- _class: transparent -->
![grid-img](./img/circuito-rlc-serie-natural.png)

<figcaption class="center tiny">

Figura 3: Circuito que ilustra a resposta natural de um circuito \\(RLC\\) série.

</figcaption>

</figure>
</div>

<div class="grid-element scriptsize">

Ao aplicar repentinamente uma fonte de tensão contínua (estímulo degrau) em um circuito \\(RLC\\) em série, busca-se entender o comportamento da corrente do sistema — em todos os elementos do circuito, que estão em série — considerando a energia inicial do circuito em \\(t_{0}\\). A representação desse processo é mostrada na figura 4.

</div>

<div class="grid-emelent">
<figure>

<!-- _class: transparent -->
![grid-img](./img/circuito-rlc-serie-degrau.png)

<figcaption class="center tiny">

Figura 4: Circuito que ilustra a resposta ao degrau de um circuito \\(RLC\\) paralelo.

</figcaption>

</figure>
</div>

</div>

</div>


---

## Resposta Natural do Circuito RLC Paralelo

<div class="grid-66-33 regular">

<div class="grid-element">

- Na resposta natural, estamos interessados na tensão \\(v(t)\\) do circuito. Como todos os elementos estão em paralelo \\(C, L \text{ e } R\\) sabemos que eles possuem a mesma tensão, portanto, \\(v(t)\\) nossa grandeza de interesse é partilhada por eles.

<div class="grid-50-50">

<div class="grid-element footnotesize">

- Entretanto, \\(v(t)\\) ainda é desconhecida e por sabermos que o circuito \\(RLC\\) é um circuito de segunda ordem, devemos de alguma forma encontrar expressões que possuam derivadas de \\(v(t)\\) até a segunda ordem.

</div>

<div class="grid-element footnotesize">

- Pela lei de Ohm, bem como, pelas equações de capacitância e indutância (vistas na [aula cinco](https://diegoascanio.github.io/ace-aula-05)), podemos escrever as correntes de cada um destes elementos em função de \\(v(t)\\), nossa grandeza de interesse e até então, desconhecida.

</div>

</div>

</div>

<div class="grid-element">

<!-- _class: transparent -->
![grid-img](./img/circuito-rlc-paralelo-natural.png)

</div>

</div>

<div class="grid-25-25-25-25 small">

<div class="grid-element">

Em função de \\(v(t)\\):

\\[
\begin{align}
    I_{C}(t) &= C \frac{dv(t)}{dt} \\\\
    I_{R}(t) &= \frac{v(t)}{R} \\\\
    I_{L}(t) &= \frac{1}{L} \int v(t) dt + I_{L}(0)
\end{align}
\\]

</div>

<div class="grid-element scriptsize">

Pela Lei de Kirchoff das correntes nos nós:

\\[
\begin{align}
    &I_{C}(t) + I_{R}(t) + I_{L}(t) = 0 \therefore \\\\
    &C \frac{dv(t)}{dt} + \frac{v(t)}{R} + \frac{1}{L} \int v(t) dt + I_{L}(0) = 0
\end{align}
\\]


</div>

<div class="grid-element tiny">

Podemos derivar os dois lados da equação à esquerda em relação ao tempo \\(t\\):

\\[
\begin{align}
    \frac{d}{dt} &\left( C \frac{dv(t)}{dt} + \frac{v(t)}{R} \right. \\\\ 
    &\left. + \frac{1}{L} \int v(t) dt + I_{L}(0) \right) = 0 \therefore \\\\
    &C \frac{d^{2}v(t)}{dt^{2}} + \frac{1}{R} \frac{dv(t)}{dt} + \frac{1}{L} v(t) = 0
\end{align}
\\]

\\(I_{L}(0)\\) é constante, portanto, \\(\frac{d}{dt} I_{L}(0) = 0\\).

</div>

<div class="grid-element footnotesize">

Já encontramos a derivada de segunda ordem de \\(v(t)\\), como esperávamos, agora, multiplicamos a equação por \\(1 \over C\\) e obtemos:

\\[
\begin{align}
    &\frac{d^{2}v(t)}{dt^{2}} + \frac{1}{RC} \frac{dv(t)}{dt} + \frac{1}{LC} v(t) = 0
\end{align}
\\]

Sendo necessário agora encontrar uma função \\(v(t)\\) que satisfaça a equação diferencial acima.

</div>

</div>


---

## Resposta Natural do Circuito RLC Paralelo - Solução Geral da Equação Diferencial de Segunda Ordem

<div class="grid-50-50 regular">

<div class="grid-element">

Recapitulando nossa EDO de ordem 2, temos:

\\[
\begin{align}
    &\frac{d^{2}v(t)}{dt^{2}} + \frac{1}{RC} \frac{dv(t)}{dt} + \frac{1}{LC} v(t) = 0 \tag{1} \label{eq:edo_{2}}\\
\end{align}
\\]

Pela nossa EDO ser de segunda ordem, não podemos solucioná-la pelo método da separação de variáveis para EDOs homogêneas de ordem 1. Mas, sabemos que toda EDO tem por solução uma função exponencial em função de \\(t\\). Consideremos \\(v(t)\\) como

\\[
    v(t) = A e^{st}
\\]

É \\(A e^{st}\\) uma função candidata para solucionar nossa EDO representada pela equação 1? Para descobrirmos, vamos substituir \\(v(t)\\) na equação 1 por \\(A e^{st}\\):


</div>

<div class="grid-element footnotesize">

<!-- _class: center -->
### Substituindo \\(v(t)\\) por \\(A e^{st}\\) na equação 1

\\[
\begin{align}
    &\frac{d^{2}(A e^{st})}{dt^{2}} + \frac{1}{RC} \frac{d(A e^{st})}{dt} + \frac{1}{LC} (A e^{st}) = 0 \therefore \\\\
    &A s^{2} e^{st} + \frac{1}{RC} A s e^{st} + \frac{1}{LC} A e^{st} = 0 \therefore \\\\
    &A e^{st} \left( s^{2} + \frac{s}{RC} + \frac{1}{LC} \right) = 0 \tag{2} \label{edo:caract} \\
\end{align}
\\]

Estudando a equação 2, 

\\[A e^{st} \left( s^{2} + \frac{s}{RC} + \frac{1}{LC} \right) = 0 \leftrightarrow A = 0 \text{ ou } {s^2 + \frac{s}{RC} + \frac{1}{LC} = 0} \\]

Pois, \\(e^{st} \neq 0 \text{ } \forall t\\). Se \\(A\\) for nulo, isso implica que \\(v(t) = 0 \text{ } \forall t\\) o que é fisicamente impossível na ocasião em que exista energia armazenada nos elementos do circuito em seu estado inicial, implicando assim que \\(A\\) seja não nulo para generalizar! Logo, \\(A e^{st}\\) é solução candidata para a solução da EDO de ordem 2 quando \\(s^2 + \frac{s}{RC} + \frac{1}{LC} = 0\\). 

O termo \\(s^2 + \frac{s}{RC} + \frac{1}{LC}\\) é chamado de **equação característica** da EDO de ordem 2 e suas raízes \\(s_{1}\\) e \\(s_{2}\\), chamadas de **raízes características** da EDO de ordem 2, fazem com que seja possível encontrar soluções da forma \\(v(t) = A e^{s_{1}t}\\) e \\(v(t) = B e^{s_{2}t}\\) para a EDO de ordem 2.

</div>

</div>


---

## Resposta Natural do Circuito RLC Paralelo - Solução Geral da Equação Diferencial de Segunda Ordem

<div class="grid-50-50 regular">

<div class="grid-element">

A equação \\(s^2 + \frac{s}{RC} + \frac{1}{LC} = 0\\) é chamada de **equação característica** da EDO de ordem 2 porquê suas raízes \\(s_{1}\\) e \\(s_{2}\\) determinam o caráter matemático de \\(v(t)\\).

Para encontrar suas raízes, apenas resolvemos esta equação de segundo grau pela fórmula de Bhaskara:

\\[s_{1,2} = \frac{-\frac{1}{RC} \pm \sqrt{\left(\frac{1}{RC}\right)^2 - 4\frac{1}{LC}}}{2}\\]

Aplicando as manipulações algébricas adequdas temos que:

\\[
\begin{align}
    s_{1} &= -\frac{1}{2RC} + \sqrt{\left(\frac{1}{2RC}\right)^2 - \frac{1}{LC}} \\\\
    s_{2} &= -\frac{1}{2RC} - \sqrt{\left(\frac{1}{2RC}\right)^2 - \frac{1}{LC}}
\end{align}
\\]

</div>

<div class="grid-element">

Se substituirmos \\(s\\) por \\(s_{1}\\) ou \\(s_{2}\\) na equação \\(v(t) = Ae^{st}\\), a solução satisfaz a EDO descrita pela equação [1](#7), pois, para qualquer valor de \\(A\\), \\(s^{2} + \frac{s}{RC} + \frac{1}{LC} = 0\\) quando \\(s = s_{1}\\) ou \\(s = s_{2}\\), já que \\(s_{1}, s_{2}\\) são raízes da equação característica.

Considere agora \\(v_{1}(t) = A_{1}e^{s_{1}t}\\) e \\(v_{2}(t) = A_{2}e^{s_{2}t}\\) como soluções da EDO [1](#7). A soma \\(v(t) = v_{1}(t) + v_{2}(t)\\) também é solução da EDO (demonstração presente no livro do Riedel 8ª edição).

Destarte, a solução geral da resposta natural do circuito \\(RLC\\) quando \\(s_{1} \neq s_{2} \\) é dada por:

<div style="box-sizing: border-box; border: 3px dotted #7851A9;">

\\[
    V(t) = A_{1}e^{s_{1}t} + A_{2}e^{s_{2}t}
\\]

</div>



</div>

</div>


---

## Resposta Natural do Circuito RLC Paralelo - Solução Geral da Equação Diferencial de Segunda Ordem

<div class="grid-50-50 regular">

<div class="grid-element">

É conveniente escrever \\(s_{1} e s_{2}\\) em função dos parâmetros \\(\alpha \text{ e } \omega_{0}\\) para interpretar o comportamento do circuito em relação a seus parâmetros \\(RLC\\) e de suas características — superamortecimento, subamortecimento e amortecimento crítico — que serão estudadas adiante. 

Considerando \\(\alpha = \frac{1}{2RC}\\) e \\(\omega_{0} = \frac{1}{\sqrt{LC}}\\), temos:

\\[
\begin{align}
    s_{1} &= -\alpha + \sqrt{\alpha^{2} - \omega_{0}^{2}} \\\\
    s_{2} &= -\alpha - \sqrt{\alpha^{2} - \omega_{0}^{2}} 
\end{align}
\\]

Os parâmetros \\(\alpha \text{ e } \omega_{0}\\) são conhecidos respectivamente por frequência de néper (ou fator de amortecimento) e frequência angular de ressonância (ou fator de oscilação) e eles que ditarão as características do circuito (superamortecimento, subamortecimento e amortecimento crítico).

</div>

<div class="grid-element">

A tabela abaixo apresenta um resumo destes parâmetros para facilitar o entendimento:

<div class="scriptsize" style="width: 80%; margin: auto; text-align: center;">

<!-- _class: ttable -->
|      Parâmetro     |              Terminologia             |                      Valor (na resposta natural)                    |      Unidade      |
|:------------------:|:-------------------------------------:|:-------------------------------------------------------------------:|:-----------------:|
| \\(s_{1}, s_{2}\\) |    Raízes da equação característica   | \\(s_{1}, s_{2} = -\alpha \pm \sqrt{\alpha^{2} - \omega_{0}^{2}}\\) |\\(\frac{rad}{s}\\)|
|  \\(\alpha\\)      |          Frequência de néper          |                \\( \alpha = \frac{1}{2RC} \\)                       |\\(\frac{rad}{s}\\)|
| \\(\omega_{0}\\)   |   Frequência angular de ressonância   |           \\( \omega_{0} = \frac{1}{\sqrt{LC}} \\)                  |\\(\frac{rad}{s}\\)|

</div>

Porque as unidades de todos os parâmetros estão em \\(\frac{rad}{s}\\)? Porque as raízes \\(s_{1}\\) e \\(s_{2}\\) (e por consequência, os parâmetros \\(\alpha \text{ e } \omega_{0}\\) que as determinam) são coeficientes do tempo \\(t\\) na exponencial \\(e^{st}\\). Como o expoente de \\(e\\) deve ser adimensional, logo, \\(s\\) deve ter a dimensão do recíproco (neste caso, inverso) do tempo — a frequência — para manter o expoente de \\(e^{st}\\) adimensional.

</div>

</div>


---

## Resposta Natural do Circuito RLC Paralelo - Solução Geral da Equação Diferencial de Segunda Ordem

<div class="normal">

Como visto no slide anterior, \\(\alpha\\) (frequência de néper) e \\(\omega_{0}\\) (frequência natural) ditam a natureza das raízes \\(s_{1}\\) e \\(s_{2}\\) e, por consequência, o comportamento do circuito na resposta ao estímulo natural.

Quando \\({\omega_{0}}^{2} < {\alpha}^{2}\\), as raízes \\(s_{1}, s_{2}\\) são reais e distintas, e a resposta natural é do tipo **superamortecida**.

Quando \\({\omega_{0}}^{2} = {\alpha}^{2}\\), as raízes são reais e iguais, e a resposta natural é do tipo **criticamente amortecida**. 

Quando \\({\omega_{0}}^{2} > {\alpha}^{2}\\), as raízes são complexas conjugadas, e a resposta natural é do tipo **subamortecida**.

Veremos mais adiante as características de cada uma destas respostas. Por hora, vamos aprender como determinar as raízes da equação característica de um circuito \\(RLC\\) paralelo através do exemplo 8.1 (pág. 296) do livro do NILSSON, RIEDEL - 10ª edição.

</div>


---

## Determinação das raízes da equação característica de um circuito RLC paralelo

<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=exemplo_8.1.ipynb" width=100% height=100%></iframe> 


---

## Características das Respostas Naturais dos Sistemas de Segunda Ordem

Já vimos que existem três tipos de respostas naturais para sistemas de segunda ordem, que são: superamortecida, criticamente amortecida e subamortecida, mas, não aprendemos ainda a distinguí-las. Nos próximos slides, começando da ordem reversa, vamos aprender como se comportam a partir de uma aplicação que pode ser modelada por um sistema de segunda ordem: portas mecânicas de fechamento automático (sistema massa-mola-amortecedor).


---

## Características das Respostas Naturais dos Sistemas de Segunda Ordem

<div class="regular">

**Resposta subamortecida (oscila em torno do ponto de equilíbrio)**

<!-- _class: center -->
![](./img/subamortecido.gif)

- O sistema não tem amortecimento suficiente para prevenir oscilações, mas, tem algum amortecimento que faz com que as oscilações decaiam ao longo do tempo.
- As raízes \\(s_{1}, s_{2}\\) do polinômio característico são distintas, imaginárias (complexas), mas, conjugadas.

</div>


---

## Características das Respostas Naturais dos Sistemas de Segunda Ordem

<div class="regular">

**Resposta criticamente amortecida (não oscila em torno do ponto de equilíbrio e alcança este ponto rapidamente)**

![small-img](./img/criticamente_amortecido.webp)


- O sistema tem amortecimento crítico — **AMORTECIMENTO MÍNIMO O SUFICIENTE** — para prevenir oscilações — por isso, dizemos que é criticamente amortecido — e por não ter amortecimento maior do que o necessário, o sistema atinge o ponto de equilíbrio (seu estado estacionário) o mais rápido possível.
- As raízes \\(s_{1}, s_{2}\\) do polinômio característico são iguais e reais.

</div>


---

## Características das Respostas Naturais dos Sistemas de Segunda Ordem

<div class="grid-50-50 regular">

<div class="grid-element">

**Resposta superamortecida (não oscila em torno do ponto de equilíbrio e alcança este ponto lentamente)**

- O sistema tem superamortecimento — **AMORTECIMENTO MAIOR DO QUE O SUFICIENTE PARA PREVENIR OSCILAÇÕES** — por isso, dizemos que é superamortecido — e por ter amortecimento maior do que o necessário, o sistema atinge o ponto de equilíbrio (seu estado estacionário) de forma lenta.
- As raízes \\(s_{1}, s_{2}\\) do polinômio característico são distintas e reais.

**Agora, a primeira ordem apresentada das respostas é retomada, sendo discutidas (a seguir) as respostas naturais — superamortecida, criticamente amortecida e subamortecida — do circuito RLC**

</div>

<div class="grid-element">

<video style="display: block; margin: auto;" width="240" controls src="./videos/superamortecido.mp4" type="video/mp4"></video>

</div>

</div>


---

## Formas de resposta natural de um circuito \\(RLC\\) paralelo

<div class="regular">

Pela superposição, sabemos que a tensão de um circuito \\(RLC\\) paralelo em resposta ao estímulo natural tem a forma:

\\[
    v = A_{1} e^{s_{1} t} + A_{2} e^{s_{2} t}
\\]

Para encontrar as soluções para a resposta natural (como também para o degrau ) é necessário encontrar os valores de \\(A_{1}\\) e \\(A_{2}\\).

Como estamos lidando com equações diferenciais ordinárias da segunda ordem, só conseguiremos obter os valores de \\(A_{1}, A_{2}\\) na resposta ao estímulo natural se conhecermos as condições iniciais do circuito (tensão e / ou corrente no instante \\(t = t_{0}\\)), bem como, as derivadas de primeira ordem da tensão e / ou corrente no mesmo instante.

Para a resposta de um circuito \\(RLC\\) ao estímulo degrau, como verificado adiante, são necessários os valores finais das grandezas de interesse \\((V_{f} \text{ e / ou } I_{f})\\).

Para cada tipo de resposta existente — **superamortecida, criticamente amortecida e subamortecida** — existe uma forma de determinar os valores de \\(A_{1}\\) e \\(A_{2}\\) e, consequentemente, determinar a função da resposta natural do circuito.

</div>


---

## Formas de resposta natural de um circuito \\(RLC\\) paralelo — Resposta Superamortecida

<div class="grid-50-50 regular">

<div class="grid-element">

- Recapitulando: ocorre quando as raízes da equação característica são reais e distintas.

- A solução para \\(v(t)\\) tem a forma

\\[
    v(t) = A_{1} e^{s_{1} t} + A_{2} e^{s_{2} t}
\\]

- Para determinar as constantes \\(A_{1}\\) e \\(A_{2}\\), precisamos das condições iniciais do circuito, dadas pelos valores de \\(v(0^{+})\\) e \\(\frac{dv(0^{+})}{dt}\\) que por sua vez, são determinados pela tensão inicial no capacitor, \\(V_{0}\\), e pela corrente inicial no indutor, \\(I_{0}\\).

</div>

<div class="grid-element">

Considerando \\(v(0^{+})\\), temos:

\\[
    v(0^{+}) = A_{1} e^{s_{1} \times 0} + A_{2} e^{s_{2} \times 0} = A_{1} + A_{2}
\\]

Ao fazermos a primeira derivada, temos:

\\[
    \frac{dv(t)}{dt} = A_{1} s_{1} e^{s_{1} t} + A_{2} s_{2} e^{s_{2} t}
\\]

Substituindo \\(t = 0^{+}\\), temos:

\\[
\begin{align}
    \frac{dv(0^{+})}{dt} &= A_{1} s_{1} e^{s_{1} \times 0} + A_{2} s_{2} e^{s_{2} \times 0} \therefore \\\\
    \frac{dv(0^{+})}{dt} &= s_{1} A_{1} + s_{2} A_{2}
\end{align}
\\]

Se conhecermos \\(s_{1}\\) e \\(s_{2}\\), encontrar \\(A_{1}\\) e \\(A_{2}\\) limita-se a:
1. Determinar \\(v(0^{+})\\) e \\(\frac{dv(0^{+})}{dt}\\);
2. Resolver o sistema linear resultante.

</div>

</div>


---

## Formas de resposta natural de um circuito \\(RLC\\) paralelo — Resposta Superamortecida

<div class="grid-50-50 regular">

<div class="grid-element">

Se conhecermos \\(s_{1}\\) e \\(s_{2}\\), encontrar \\(A_{1}\\) e \\(A_{2}\\) limita-se a:
1. Determinar \\(v(0^{+})\\) e \\(\frac{dv(0^{+})}{dt}\\);
2. Resolver o sistema linear resultante.

</div>

<div class="grid-element">

<!-- _class: transparent center -->
![](./img/circuito-rlc-paralelo-natural.png)

</div>

</div>

<div class="grid-33-33-33 footnotesize">

<div class="grid-element">

- O valor \\(v_{0^{+}}\\) é a tensão \\(V_{0}\\) no capacitor no instante \\(t=0^{+}\\);
- Pelas equações da capacitância:

\\[
\begin{align}
    i_{C}(0^{+}) &= C \frac{dv_{0^{+}}}{dt} \therefore \\\\
    \frac{dv_{0^{+}}}{dt} &= \frac{i_{C}(0^{+})}{C} \tag{3}
\end{align}
\\]

</div>

<div class="grid-element">

- Assim, temos que determinar qual a corrente \\(i_{C}(0^{+})\\) que circula no capacitor no instante \\(t=0^{+}\\);
- Pela Lei de Kirchoff das Correntes nos nós, temos que \\(0 = i_{C} + i_{L} + i_{R} \\);
- Pela Lei de Ohm, temos que \\(i_{R} = \frac{V_{0}}{R}\\);
- A corrente presente no indutor no instante de tempo \\(t=0^{+}\\) é \\(I_{0}\\);

</div>

<div class="grid-element">

- Reorganizando a equação obtida pela LKC nos nós obtém-se: \\(i_{C} = -i_{R} - i_{L}\\);
- Substituindo-se \\(I_{R}\\) por \\(\frac{V_{0}}{R}\\) e \\(I_{L}\\) por \\(I_{0}\\), temos que \\(i_{C} = -\frac{V_{0}}{R} - I_{0}\\);
- Assim, podemos determinar o valor numérico de \\(i_{C}(0^{+})\\) e substituir na equação (3) para determinar \\(\frac{dv_{0^{+}}}{dt}\\).
- Depois, substituimos \\(v_{0^{+}}\\) e \\(\frac{dv_{0^{+}}}{dt}\\) no sistema linear e o resolvemos, obtendo \\(A_{1}\\) e \\(A_{2}\\).

</div>

</div>


---

## Formas de resposta natural de um circuito \\(RLC\\) paralelo — Resposta Superamortecida

<div class="regular">

O processo para determinação da resposta superamortecida \\(v(t)\\) pode ser resumido da seguinte forma — ipsis líteris ao contido em NILSSON, RIEDEL 10ª Edição p. 298:

1. Determine as raízes da equação característica \\(s_{1}\\) e \\(s_{2}\\), usando os valores de \\(R, L \text{ e } C\\);
2. Determine \\(v(0^{+})\\) e \\(\frac{dv(0^{+})}{dt}\\) usando análise de circuitos;
3. Determine os valores de \\(A_{1}\\) e \\(A_{2}\\) usando as equações simultaneamente:
\\[
\begin{align}
v(0^{+}) &= A_{1} + A_{2} \\\\
\frac{dv(0^{+})}{dt} &= \frac{i_{C}(0^{+})}{C} = s_{1}A_{1} + s_{2}A_{2}
\end{align}
\\]
4. Substitua os valores de \\(s_{1}, s_{2}, A_{1} \text{ e } A_{2}\\) na equação da resposta natural \\(v(t) = A_{1}e^{s_{1}t} + A_{2}e^{s_{2}t}\\) para determinar \\(v(t), t \geq 0\\).

Resolveremos dois exemplos (8.2, 8.3) presentes no livro de NILSSON, RIEDEL 10ª Edição p. 298-300 para ilustrar o processo de determinação da resposta superamortecida.

</div>


---

## Resposta Natural Superamortecida RLC — Exemplo 8.2


<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=exemplo_8.2.ipynb" width=100% height=100%></iframe> 


---

## Cálculo das correntes de ramo na resposta natural de um circuito RLC em paralelo — Exemplo 8.3


<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=exemplo_8.3.ipynb" width=100% height=100%></iframe> 


---

## Resposta Natural Criticamente Amortecida do circuito RLC

<div class="regular grid-50-50">

<div class="grid-element">

Quando consideramos a resposta criticamente amortecida de um circuito RLC, admitimos que as raízes do polinômio característico que descreve o circuito são reais e iguais. Para que este caso aconteça, o discriminante \\(\Delta\\) da equação característica deve ser igual a zero.

Até o momento, admitimos como solução para uma EDO de segunda ordem a existência de uma função \\(v(t)\\) do tipo \\(A e^{st}\\) que pode ser escrita por uma superposição de outras duas funções do tipo \\(A_{1} e^{s_{1}t}\\) e \\(A_{2} e^{s_{2}t}\\) quando \\(s_{1} \neq s_{2}\\):

\\[
    v(t) = A_{1} e^{s_{1}t} + A_{2} e^{s_{2}t} \tag{4}
\\]

Entretanto, quando \\(s_{1} = s_{2}\\), conseguimos encontrar um sistema linear possível e determinado que encontre os valores das constantes \\(A_{1}\\) e \\(A_{2}\\)?

</div>
<div class="grid-element">

Se \\(s_{1} = s_{2}\\), então, podemos considerar \\(s_{1} = s_{2} = s\\). Substituindo \\(s_{1}\\) e \\(s_{2}\\) por \\(s\\) na equação (4), temos:

\\[
    v(t) = (A_{1} + A_{2}) e^{st} \\\\
    v^{'}(t) = s (A_{1} + A_{2}) e^{st}
\\]

Para encontrar os valores das constantes \\(A_{1}\\) e \\(A_{2}\\) temos que considerar as condições iniciais \\(v(0)\\) e \\(v^{'}(0)\\). Assim, temos que \\(v(0) = A_{1} + A_{2}\\) e \\(v^{'}(0) = s (A_{1} + A_{2})\\).

Reescrevendo este sistema na forma matricial, temos:

\\[
\begin{align}
    \begin{bmatrix}
        1 & 1 \\\\
        s & s
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
        A_{1} \\\\
        A_{2} 
    \end{bmatrix}
    =
    \begin{bmatrix}
        v(0) \\\\
        v^{'}(0)
    \end{bmatrix}
\end{align}
\\]

Verificamos de imediato que a matriz dos coeficientes é singular, pois \\(det(\begin{bmatrix} 1 & 1 \\\\ s & s \end{bmatrix}) = 0\\). Portanto, o sistema linear não é determinado. Destarte, precisamos de outra função candidata \\(v(t)\\) para encontrar um SL possível e determinado que permita encontrar os valores das constantes \\(A_{1}\\) e \\(A_{2}\\).

</div>

</div>


---

## Resposta Natural Criticamente Amortecida do circuito RLC

<div class="regular">

Considerando que \\(s_{1} = s_{2} = s = - \alpha = -\frac{1}{2RC} \\) precisamos encontrar função (funções) candidata(s) para \\(v(t)\\) que forme(m) um conjunto fundamental de soluções para a equação diferencial homogênea que sejam linearmente independentes, para que \\(D_{1} (A_{1}) \neq -D_{2} (A_{2})\\) e portanto, outra solução além da trivial — \\(v(t) = 0\\) \\(\forall t \geq 0 \\), físicamente inviável  — seja possível.

Considerar \\(v(t) = (D_{1}t + D_{2})e^{st}\\) forma este conjunto de soluções fundamentais? Vamos verificar.

</div>

<div class="small grid-50-50" style="border-style: solid; border-width: 2px; border-color: #6b3fa0;">

<div class="grid-element">

\\[
\begin{align}
    v(t) &= (D_{1}t + D_{2})e^{st} \\\\
    \frac{d v(t)}{dt} &= (st + 1) \cdot D_{1}e^{st} + s \cdot D_{2}e^{st} 
\end{align}
\\]

Para encontrarmos \\(D_{1}\\) e \\(D_{2}\\) temos de considerar \\(v(0)\\) e \\(\frac{dv(0)}{dt}\\). Assim:

\\[
\begin{align}
    v(0) &= (D_{1} \cdot 0 + D_{2})e^{s \cdot 0} = D_{2} \\\\
    \frac{dv(0)}{dt} &= (s \cdot 0 + 1) \cdot D_{1}e^{s \cdot 0} + s \cdot D_{2}e^{s \cdot 0} = D_{1} + s \cdot D_{2}
\end{align}
\\]

Reescrevendo este sistema em sua representação matricial, temos:

\\[
\begin{align}
\begin{bmatrix}
0 & 1 \\\\
1 & s
\end{bmatrix}
\cdot
\begin{bmatrix}
D_{1} \\\\
D_{2}
\end{bmatrix}
&=
\begin{bmatrix}
v(0) \\\\
\frac{dv(0)}{dt}
\end{bmatrix}
\end{align}
\\]

</div>

<div class="grid-element">

Agora, verificamos que \\(det(
\begin{bmatrix}
0 & 1 \\\\
1 & s
\end{bmatrix}) \neq 0
\\) em qualquer situação, o que portanto, garante um sistema linear possível e determinado para encontrar os valores de \\(D_{1}\\) e \\(D_{2}\\) que serão, respectivamente:

\\[
\begin{align}
D_{1} &= \frac{dv(0)}{dt} - s \cdot v(0) \\\\
D_{2} &= v(0)
\end{align}
\\].

Resta verificar agora se \\(\frac{d^{2}v(t)}{dt^{2}} + \frac{1}{RC} \frac{dv(t)}{dt} + \frac{1}{LC}v(t) = 0\\) quando \\(v(t) = (D_{1}t + D_{2})e^{st}\\).

Utilizaremos o exemplo 8.5 do livro de NILSSON, RIEDEL 10ªed. implementado em um jupyter notebook no próximo slide para fazer esta verificação.

</div>

</div>


---

## Cálculo da resposta natural de um circuito RLC em paralelo criticamente amortecido — Exemplo 8.5

<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=exemplo_8.5.ipynb" width=100% height=100%></iframe> 


---

## Resposta Natural Subamortecida do circuito RLC paralelo

<div class="grid-50-50 small">

<div class="grid-element">

Quando consideramos a resposta subamortecida de um circuito RLC, admitimos que as raízes do polinômio característico que descreve o circuito são complexas e conjugadas. Para que este caso aconteça, o discriminante da equação característica deve ser menor que zero — **ou seja, \\( \alpha^{2} - \omega_{0}^{2} < 0 \rightarrow \alpha^{2} < \omega_{0}^{2} \\)** — o que implica a existência de uma raiz quadrada de um número negativo, onde esse número pode ser escrito da forma:

\\[
j \omega_{d}
\\]

Consideremos \\(s_{1}, s_{2} = -\alpha \pm \sqrt{\alpha^{2} - \omega_{0}^{2}}\\).

É possível reescrever \\(s_{1}\\) (e \\(s_{2}\\)), por conveniência da expressão, como:

\\[
\begin{align}
    s_{1} &= -\alpha + \sqrt{-({\omega_{0}}^{2} - \alpha^{2})} \therefore \\\\
          &= -\alpha + \sqrt{(-1) \cdot ({\omega_{0}}^{2} - \alpha^{2})} \therefore \\\\
          &= -\alpha + j \sqrt{{\omega_{0}}^{2} - \alpha^{2}} \therefore \\\\
          &= -\alpha + j \omega_{d} \\\\
    s_{2} &= -\alpha - j \omega_{d}
\end{align}
\\]

</div>

<div class="grid-element">

Onde \\(\omega_{d}\\) é a frequência angular amortecida do circuito – termo explicado adiante – definida como:

<div class="normal" style="border: 2px solid #7851A9; padding: 5px; margin: 5px 0px;">

\\[
    \omega_{d} = \sqrt{{\omega_{0}}^{2} - \alpha^{2}}
\\]

</div>

Considerando que nossas raízes \\(s_{1}\\) e \\(s_{2}\\) são complexas e conjugadas, podemos escrever a resposta natural subamortecida do circuito RLC paralelo pela forma padrao da resposta natural como:

\\[
    v(t) = A_{1} e^{(-\alpha + j \omega_{d})t} + A_{2} e^{(-\alpha - j \omega_{d})t}
\\]

Da identidade de euler, temos que:

\\[
    e^{\pm j \theta} = \cos(\theta) \pm j \sin(\theta)
\\]

Assim, devemos aplicar manipulações algébricas necessárias para escrevermos a resposta subamortecida como uma soma de senos e cossenos que — SPOILERS INCLUSOS —oculta o termo \\(j\\) (complexo) da resposta final.

</div>

</div>

</div>


---

## Resposta Natural Subamortecida do circuito RLC paralelo

<div class="grid-50-50 small">

<div class="grid-element">

A partir de

\\[
\begin{align}
    v(t) &= A_{1} e^{(-\alpha + j \omega_{d})t} + A_{2} e^{(-\alpha - j \omega_{d})t} \\\\
    &\text{Temos: } \\\\
    &= A_{1} e^{-\alpha t} e^{j \omega_{d} t} + A_{2} e^{-\alpha t} e^{-j \omega_{d} t} \therefore \\\\
    &= e^{-\alpha t} \left( A_{1} e^{j \omega_{d} t} + A_{2} e^{-j \omega_{d} t} \right) \\\\
    &\text{Aplicando a identidade de Euler: } \\\\
    &= e^{-\alpha t} \left( A_{1} \cos(\omega_{d} t) + j A_{1} \sin(\omega_{d} t) + \right. \\\\ 
    &\left. A_{2} \cos(\omega_{d} t) - j A_{2} \sin(\omega_{d} t) \right) \\\\
    &= e^{-\alpha t} \left[ (A_{1} + A_{2}) \cdot \cos(\omega_{d} t) + \right. \\\\
    &\left. j (A_{1} - A_{2}) \cdot \sin(\omega_{d} t) \right] 
\end{align}
\\]

</div>

<div class="grid-element">

Agora, substitua as constantes arbitrárias \\( A_{1} + A_{2} \\) e \\( j (A_{1} - A_{2}) \\) por novas constantes reais arbitrárias denotadas \\( B_{1} \\) e \\( B_{2} \\), respectivamente, para obter:

\\[
\begin{align}
    v(t) &=  e^{-\alpha t} \left[ B_{1} \cdot \cos(\omega_{d} t) + B_{2} \cdot \sin(\omega_{d} t) \right] \therefore \\\\
\end{align}
\\]

<div style="border: 2px solid #7851A9; padding: 5px; margin: 5px 0px; text-align: center;">

\\[
\begin{align}
    v(t) &= B_{1} e^{-\alpha t} \cdot \cos(\omega_{d} t) + B_{2} e^{-\alpha t} \cdot \sin(\omega_{d} t)
\end{align}
\\]

**A forma padrão da resposta natural subamortecida.**

</div>

Observações:
- Não se deixe enganar pelo fato de que \\(B_{2} = j(A_{1} - A_{2})\\). Neste caso, \\(A_{1}\\) e \\(A_{2}\\) são conjugados complexos, de modo que \\(B_{1}, B_{2}\\) são reais, de acordo com Nilsson Riedel 10ª edição.
    - Quem provar matematicamente que \\(B_{1}, B_{2}\\) são reais ganha 3 pontos extras, quero a prova formatada em LaTeX.

</div>

</div>


---

## Resposta Natural Subamortecida do circuito RLC paralelo

<div class="grid-50-50 small">


<div class="grid-element">

Conhecendo a forma geral da resposta Subamortecida de um circuito \\(RLC\\) paralelo dada por:

\\[
    v(t) =  e^{-\alpha t} \left[ B_{1} \cdot \cos(\omega_{d} t) + B_{2} \cdot \sin(\omega_{d} t) \right]
\\]

Devemos agora determinar \\(B_{1}\\) e \\(B_{2}\\). Para a resposta subamortecida, as duas equações simultâneas que determinam \\(B_{1}\\) e \\(B_{2}\\) dependem das condições iniciais \\(v(0^{+})\\) e \\(\frac{dv(0^{+})}{dt}\\) do circuito, sendo:

\\[
\begin{align}
v(0^{+}) &= V_{0} = B_{1} \\\\
\frac{dv(0^{+})}{dt} = \frac{i_{C}(0^{+})}{C} = - \alpha B_{1} + \omega_{d} B_{2}
\end{align}
\\]


</div>

<div class="grid-element">

Verificaremos no exemplo 8.4 — NILSSON, RIEDEL 10ª Ed. — que a resposta subamortecida de um circuito é caracterizada por oscilações indicadas por funções trigonométricas, com a tensão alternando entre valores positivos e negativos. A frequência dessas oscilações é determinada por \\(\omega_{d}\\), enquanto a taxa de diminuição da amplitude é regida pelo fator de amortecimento \\(\alpha\\). A frequência \\(\omega_{d}\\) é conhecida como a frequência angular amortecida, que é menor do que a frequência natural \\(\omega_{0}\\) em presença de um elemento dissipativo \\(R\\) no circuito. Quando \\(\alpha \neq 0\\), a frequência de oscilação é considerada amortecida.

</div>

</div>


---

<!-- _class: lead -->
# Resolução do Exemplo 8.4 direta, no jupyter notebook em sala de aula


---

<iframe src="https://diegoascanio.github.io/jupyterlite" width=100% height=100%></iframe> 


---

<div class="regular">

# Seminários de estudos autônomos - valor base 6 pontos + 6 pontos bônus na prova

Vocês serão divididos em grupos de até quatro pessoas.

Vocês devem construir seus slides com base no meu modelo de slides para a aula 7, disponível em [https://github.com/diegoascanio/ace-aula-07](https://github.com/diegoascanio/ace-aula-07), no meu formato de slides.

Grupo 1 - Responsável por determinar as características da resposta subamortecida natural
Grupo 2 - Responsável por determinar a forma da resposta superamortecida a um degrau no circuito RLC paralelo
Grupo 3 - Responsável por determinar a forma da resposta criticamente amortecida a um degrau no circuito RLC paralelo
Grupo 4 - Responsável por determinar a forma da resposta subamortecida a um degrau no circuito RLC paralelo.
Grupo 5 - Responsável por determinar a forma da resposta superamortecida natural e degrau no circuito RLC série
Grupo 6 - Responsável por determinar a forma da resposta criticamente amortecida natural e degrau no circuito RLC série
Grupo 7 - Responsável por determinar a forma da resposta subamortecida natural e degrau no circuito RLC série
Grupo 8 - Responsável por abordar a perspectiva prática: a sincronização do relógio de um computador.

</div>


---

<div class="cabecalho large">
Referências Bibliográficas
</div>
<div class="conteudo normal">

- RIEDEL, SUSAN A.; NILSSON, James W. — Circuitos Elétricos 8ª ed. 2009.
- RIEDEL, SUSAN A.; NILSSON, James W. — Circuitos Elétricos 10ª ed. 2015.
- DE MELO, E. G. — Curso: LOM3202 - Circuitos Elétricos (2020). Accessed August 6, 2023. https://edisciplinas.usp.br/course/view.php?id=82680.
- DE ARAÚJO, THABATTA M. A. - SLIDES E NOTAS DE AULAS - Disponível junto à profª Thabatta.

</div>


---

# Determinar a Forma da Resposta Subamortecida a um Degrau no Circuito RLC Paralelo

<div class="grid-element">

## Introdução

Determinar a resposta a um degrau Subamortecido de um circuito RLC em paralelo significa determinar a tensão nos ramos paralelos ou a corrente nos ramos individuais em que ambas as raízes sejam complexas.

No nosso caso estudaremos quando ela se inicia em t = 0 e i = 0. Conforme t aumenta, nosso i também aumenta até se aproximar do i da fonte.

</div>


---

<div class="grid-25 small">

<div class="grid-element">

# Resposta ao Degrau de Circuito RLC

<p align="center">
<img src="./img/grupo4/cc2.png" width="500"/>
</p>

\\[ R = 625\Omega \\]

1. A frequência angular de amortecimento \\( \omega_0 \\) é dada por:

\\[ \omega_0^2 = \frac{1}{LC} = \frac{10^{12}}{25 \times 25} = 16 \times 10^8 \\]

2. O coeficiente de amortecimento \\( \alpha \\) é dado por:

\\[ \alpha = \frac{1}{2RC} = \frac{10^9}{2 \times 625 \times 25} = 3.2 \times 10^4 \text{ rad/s} \\]

<p align="center">
ou
</p>

\\[ \alpha^2 = 10.24 \times 10^8 \\]

- Como \\( \alpha^2 < \omega_0^2 \\), as raízes da equação característica são complexas, o que indica uma resposta subamortecida.

</div>


---

<div class="grid-25 small">

<div class="grid-element">

# Resposta ao Degrau Subamortecida

3. A frequência de oscilação amortecida \\( \omega_d \\) é calculada pela diferença entre a frequência natural não amortecida ao quadrado e o coeficiente de amortecimento ao quadrado:

\\[ \omega_d = \sqrt{\omega_0^2 - \alpha^2} = \sqrt{16 \times 10^8 - 10,24 \times 10^8} = 24.000 \\]

4. As raízes da equação característica são:

\\[ s_1 = -\alpha + j\omega_d = -3,2 \times 10^4 + j2,4 \times 10^4 \text{ rad/s} \\]
\\[ s_2 = -\alpha - j\omega_d = -3,2 \times 10^4 - j2,4 \times 10^4 \text{ rad/s} \\]

- A corrente no indutor \\( i_L \\) como resposta ao degrau é dada por:

  \\[ i_L = I_f + e^{-\alpha t} \left[ B'_1 \cos(\omega_d t) + B'_2 \sin(\omega_d t) \right] \\]

</div>


---

<div class="grid-25 small">

<div class="grid-element">

# Resposta ao Degrau Subamortecida

- As condições iniciais para a corrente \\( i_L \\) no indutor são dadas por:

  \\[ i_L(0) = I_f + B'_1 = 0 \\]

  \\[ \frac{d i_L}{d t}(0) = \omega_d B'_2 -\alpha B'_1 = 0 \\]

  Onde \\( B'\_1 \\) e \\( B'\_2 \\) são constantes a serem determinadas.

- Resolvendo as condições iniciais, encontramos os valores de \\( B'\_1 \\) e \\( B'\_2 \\):

  \\[ B'_1 = -24 \text{ mA} \\]

  \\[ B'_2 = -32 \text{ mA} \\]

- A expressão para a corrente \\( i_L(t) \\) com as constantes substituídas é:

  \\[ i_L(t) = 24 + (-24 \cos(24.000t) - 32 \sin(24.000t))e^{-32.000t} \text{ mA, t} \geq 0\\]

</div>


---

<div class="grid-25 small">

<div class="grid-element">

# Resposta ao Degrau Subamortecida

- A corrente no indutor \\( i_L(t) \\) como resposta ao degrau é dada pela expressão:

  \\[ i_L(t) = 24 + (-24 \cos(24.000t) - 32\sin(24.000t))e^{-32.000t} \text{ mA} \\]

- A seguir, um gráfico da corrente \\( i_L(t) \\) em função do tempo ilustrando a resposta ao degrau subamortecida.

<p align="center">
<img src="./img/grupo4/grupo4-img1.png" width="500"/> 
</p>

</div>


---

<div class="grid-25-25 small">

<div class="grid-element">

# Gráfico com os Três Tipos de Respostas: Superamortecido, Criticamente Amortecido e Subamortecido

- O gráfico a seguir ilustra as diferentes respostas de um circuito RLC para diferentes valores de resistência \\( R \\):

  - Superamortecido (\\( R = 400 \Omega \\))
  - Criticamente amortecido (\\( R = 500 \Omega \\))
  - Subamortecido (\\( R = 625 \Omega \\))

- Cada curva mostra como a corrente no indutor \\( i_L \\) se comporta com o tempo após a aplicação de um degrau de tensão.

<p align="center">
<img src="./img/grupo4/grupo4-img3.png" width="500"/> 
</p>

</div>
