# Projeto de uma Fonte de Tensão Ajustável
#### Resumo
Projeto de uma fonte de tensão ajustável entre 3V a 12V com capacidade de 100mA, realizado para a disciplina SSC0180 - Eletrônica para a Computação do 1º semestre do Bacharelado em Ciências de Computação no Instituto de Ciências Matemáticas e de Computação da Universidade de São Paulo (ICMC-USP). O trabalho foi supervisionado pelo Prof. Dr. Eduardo do Valle Simões.

#### Alunos
[Ana Lívia Ruegger Saldanha](https://github.com/liviaruegger) (Número USP: 8586691)<br />
[Guilherme Sousa Panza](https://github.com/guisp03) (Número USP: 12543519)<br />
[Rebeca Vieira Carvalho](https://github.com/RebecaVC) (Número USP: 12543530)<br />
[Théo da Mota dos Santos](https://github.com/theosant) (Número USP: 10691331)<br />

### Instruções
Projetar uma fonte de tensão ajustável entre 3V e 12V com capacidade de 100mA, que funcione a partir de uma tomada de 127V de corrente alternada e frequência de 60Hz.

### Introdução
O objetivo do projeto é utilizar os conhecimentos adquiridos em eletrônica durante o semestre para elaborar um circuito que correspondesse às especificações estabelecidas. Dessa forma, os componentes e suas funções foram estudados e organizados para obter os resultados desejados. 

### Descrição dos componentes
**• Transformador:** <br />Altera a tensão do circuito através da indução de duas bobinas, que mudam a tensão conforme a razão entre as voltas do fio. Inicialmente a tensão que se tem para os cálculos é a de 180V de corrente eficaz proveniente da corrente alternada, portanto, é necessário que se dimensione essa voltagem para um valor mais aproximado de 12V como na especificação. Assim, considerando possível redução de tensão devido às resistências dos componentes do circuito, foi estimado o valor 18V para a tensão de saída. <br />

#### 1° Etapa - Retificação

**• Diodos (Ponte retificadora):** <br />São semicondutores que permitem a passagem da corrente por apenas um sentido. Ao colocar os diodos em uma certa configuração, é possível alterar a corrente alternada para uma corrente que irá apenas para um sentido. <br />

#### 2° Etapa - Filtragem

**• Capacitor:** <br />Para fazer a tensão ficar realmente contínua na saída é necessário utilizar um capacitor que se carregará de energia toda a vez que a tensão subir e quando a ela descer, o capacitor é quem alimentará o circuito, fazendo com que a tensão na saída seja praticamente contínua. A variação entra a continuidade perfeita e a real é dada pelo Ripple.<br />

#### 4° Etapa - Regulagem

**• Resistores:** <br />— R1: Limita a corrente que passa pelo Diodo Zener para que ele se mantenha abaixo do máximo definido pelas especificações.<br /> — R2: Limita a tensão mínima na saída, para que ela fique aproximadamente 3V, assim como nas especificações.<br />

**• Potenciômetro:** <br />É um dispositivo com a resistência ajustável, que será responsável pelas alterações de tensão entre 12V e 3V, conforme o necessário.<br />

**• Diodo Zener:** <br />É parecido com um diodo comum, porém possui uma tensão de ruptura que permite o fluxo de elétrons no sentido inverso. Ele limita a tensão máxima de acordo com suas especificações que, no caso são de 13V. Foi escolhido 13 Volts para não ficar abaixo de 12V, uma vez que o Transistor consome 0,7V para o início da passagem da corrente de C a E.<br />

**• Transistor:** <br />Funciona como um interruptor, quando recebe corrente pela base permite o fluxo de elétrons, além disso também possui a função de amplificar a corrente. Nesse projeto, ele adquire o segundo papel, uma vez que ele faz com que a corrente que passa de C a E, seja proporcional à corrente que vem do potenciômetro, baseado em uma proporção Beta de 100 (B*100 = C). Assim, é possível regular de maneira inversamente proporcional tanto a corrente da saída, quanto sua tensão (já que a Resistencia é inversamente proporcional à Corrente).<br />

### Escolha dos componentes
Quantidade | Componente | Especificações | Valor Unitário | Subtotal
:--------: | :--------: | :------------: | :------------: | :------:
1x | [Transformador](https://www.soldafria.com.br/transformador-18v-500ma-entrada-110-220vac?gclid=CjwKCAjwgISIBhBfEiwALE19SYi9AQrBZl5fFIyoIGijSuOdKULBggC66sKIhYPmz87XsCafkuF5EBoCyG0QAvD_BwE) | 18V | R$27,99 | R$27,99
Total |||| R$ ??

### Diagrama da fonte no Falstad

![Fonte](https://github.com/theosant/fonteajustavel/blob/main/CircuitoFalstad2.png)
[Link do projeto no Falstad](https://tinyurl.com/ye2f5hnm)

### Cálculos
Não é obrigatório, mas seria legal incluir.

### Projeto do esquemático da PCB no EAGLE

![Esquematico](https://github.com/theosant/fonteajustavel/blob/main/Esquematico3.png)
![Conexoes](https://github.com/theosant/fonteajustavel/blob/main/Conexoes3.png)

### Vídeos
Pede-se: incluir vídeo(s) mostrando o Projeto funcionando e/ou simulando, e explicando porque escolheu os valores dos componentes.<br />
[Video 1](<>)<br />
[Video 2](<>)<br />

### Considerações finais
...

### Agradecimentos
...
