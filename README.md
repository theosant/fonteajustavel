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

### Diagrama da fonte no Falstad

![Fonte](https://github.com/theosant/fonteajustavel/blob/main/Imagens/Falstad3.png)
[Link do projeto no Falstad](https://tinyurl.com/yj6r99p3)

### Projeto do esquemático da PCB no EAGLE

![Esquematico](https://github.com/theosant/fonteajustavel/blob/main/Imagens/Esquematico3.png)<br />
![Conexoes](https://github.com/theosant/fonteajustavel/blob/main/Imagens/Conexoes3.png)<br />

### Descrição dos componentes
#### 1ª Etapa - Transformação
**• Transformador:** <br />Altera a tensão do circuito através da indução de duas bobinas, que mudam a tensão conforme a razão entre as voltas do fio. Inicialmente a tensão que se tem para os cálculos é a de 180V de corrente eficaz proveniente da corrente alternada, portanto, é necessário que se dimensione essa voltagem para um valor mais aproximado de 12V como na especificação. Assim, considerando possível redução de tensão devido às resistências dos componentes do circuito, foi estimado o valor 18V para a tensão de saída. <br />

#### 2ª Etapa - Retificação
**• Diodos (Ponte retificadora):** <br />São semicondutores que permitem a passagem da corrente por apenas um sentido. Ao colocar os diodos em uma certa configuração, é possível alterar a corrente alternada para uma corrente que irá apenas para um sentido. <br />

#### 3ª Etapa - Filtragem

**• Capacitor:** <br />Para fazer a tensão ficar realmente contínua na saída é necessário utilizar um capacitor que se carregará de energia toda a vez que a tensão subir e quando a ela descer, o capacitor é quem alimentará o circuito, fazendo com que a tensão na saída seja praticamente contínua. A variação entra a continuidade perfeita e a real é dada pelo Ripple.<br />


#### 4ª Etapa - Regulagem

**• Resistores:** <br />- R1: Limita a corrente que passa pelo Diodo Zener para que ele se mantenha abaixo do máximo definido pelas especificações.<br /> - R2: Limita a tensão mínima na saída, para que ela fique aproximadamente 3V, assim como nas especificações.<br />

**• Potenciômetro:** <br />É um dispositivo com a resistência ajustável, que será responsável pelas alterações de tensão entre 12V e 3V, conforme o necessário.<br />

**• Diodo Zener:** <br />É parecido com um diodo comum, porém possui uma tensão de ruptura que permite o fluxo de elétrons no sentido inverso. Ele limita a tensão máxima de acordo com suas especificações que, no caso são de 13V. Foi escolhido 13 Volts para não ficar abaixo de 12V, uma vez que o Transistor consome 0,7V para o início da passagem da corrente de C a E.<br />

**• Transistor:** <br />Funciona como um interruptor, quando recebe corrente pela base permite o fluxo de elétrons, além disso também possui a função de amplificar a corrente. Nesse projeto, ele adquire o segundo papel, uma vez que ele faz com que a corrente que passa de C a E, seja proporcional à corrente que vem do potenciômetro, baseado em uma proporção Beta de 100 (B*100 = C). Assim, é possível regular de maneira inversamente proporcional tanto a corrente da saída, quanto sua tensão (já que a Resistencia é inversamente proporcional à Corrente).<br />

#### Extra:
**+ LED:** Apenas uma maneira de se visualizar que há corrente passando pelo sistema. <br />
**+ Resistor LED:** Limita a corrente que passará pelo LED para que ele não queime. De acordo com as especificações, seu valor de resistência deve ser entre 680R e 1K1 para que a corrente que passa por ele seja abaixo de 20mA que é seu máximo. Dessa forma, escolhemos o resistor de 1k que dá uma boa margem para que não haja problemas. 


### Escolha dos componentes
Quantidade | Componente | Especificações | Valor Unitário |
:--------: | :--------: | :------------: | :------------: |
1x | [Transformador](https://www.soldafria.com.br/transformador-18v-500ma-entrada-110-220vac?gclid=CjwKCAjwgISIBhBfEiwALE19SYi9AQrBZl5fFIyoIGijSuOdKULBggC66sKIhYPmz87XsCafkuF5EBoCyG0QAvD_BwE) | 18V | R$27,99 
4x | [Diodo](https://www.baudaeletronica.com.br/diodo-1n4007.html?gclid=CjwKCAjwgISIBhBfEiwALE19SafDhS3zcKlc-pYkbX4yrKnC0vrDEIC7dmgl-M4LfWpkxQgSgWPXVBoCGGAQAvD_BwE)| 1N4007 | R$0,10 
1x | [Capacitor](https://produto.mercadolivre.com.br/MLB-1915915264-560uf-25v-10-unidades-capacitor-eletrolitico-560uf-25v-_JM?matt_tool=87716990&matt_word=&matt_source=google&matt_campaign_id=12413740998&matt_ad_group_id=119070072438&matt_match_type=&matt_network=g&matt_device=c&matt_creative=500702333978&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=295274570&matt_product_id=MLB1915915264&matt_product_partition_id=337120033364&matt_target_id=aud-879604627128:pla-337120033364&gclid=CjwKCAjwgISIBhBfEiwALE19SSJuvn_YJIBoWkNwUp9WwY33Nta2HSl5PS2rgAiBzvIXnVDysL0c2BoCJPgQAvD_BwE) | 560 μF 25V | R$1,90 | R$1,90
1x | [Resistência](https://www.baudaeletronica.com.br/resistor-2k2-5-1-4w.html?gclid=CjwKCAjwgISIBhBfEiwALE19SS1oi92NCxtcSPmxnNBpX_zIe8WpckMf3SExsrUsOE_ks7Yn8ie1-xoC-GQQAvD_BwE) | 2k2Ω 1/4W | R$0,05 
1x | [Resiência](https://www.baudaeletronica.com.br/resistor-1k-5-1-4w.html) | Resistor 1K 1/4W | R$0,05
1x | [Resistência](https://www.baudaeletronica.com.br/resistor-560r-5-1-4w.html?gclid=CjwKCAjwgISIBhBfEiwALE19Sf6vY3taqhZoEn3L4qgsixLtqOAoYjv3Ge9f_c2XX-5geIaFSLrnPxoCAkkQAvD_BwE) | 560Ω 1/4W | R$0,05 
1x | [Led](https://www.baudaeletronica.com.br/led-difuso-5mm-vermelho.html?gclid=CjwKCAjwgISIBhBfEiwALE19SeEbv2XmTl9l-goiKp9pguh6RLQcJC7GVRghqHqdLSCI5sf0waV4eBoChY0QAvD_BwE) | Difuso 5mm | R$0,23 
1x | [Zener](https://www.baudaeletronica.com.br/diodo-zener-bzx55c-13v-0-5w.html?gclid=CjwKCAjwgISIBhBfEiwALE19SWIFKwNCWbOrWzfxyZ2e321rHF8viCXOqk8JYHUQMETebNwSlPXylhoCtX8QAvD_BwE) | 13V 0,5W | R$0,09 
1x | [Potenciometro](https://www.baudaeletronica.com.br/potenciometro-linear-de-5k-5000.html?gclid=CjwKCAjwgISIBhBfEiwALE19SfD9mpnf_luAb2enr7G8WmFqdA7xBAykY8erseIPlrFKdb14Mw_V4xoCB-gQAvD_BwE) | 5kΩ | R$1,99
1x | [Transistor](https://www.filipeflop.com/produto/transistor-s8050-npn-x10-unidades/?utm_source=google&utm_medium=organic&utm_campaign=shopping&utm_content=surfaces_across_google) | S8050NPN | R$0,59 

Total | R$33,04
:---: | :---:

### Cálculos
![Contas](https://github.com/theosant/fonteajustavel/blob/main/Imagens/contas.jpg)
### Vídeos
[Video 1](<>)<br />
[Video 2](<>)<br />

### Considerações finais
Como proposto, a fonte projetada atinge os objetivos estabelecidos: possibilita a obtenção de tensão ajustável entre 3V e 12V com capacidade de 100mA, funcionando a partir de uma tomada de 127V de corrente alternada e frequência de 60Hz. Todos os componentes escolhidos foram importantes para atingir o resultado final e o comportamento do circuito na simulação reflete o esperado pelos nossos cálculos.

### Agradecimentos
Agracemos especialmente ao professor Eduardo Simões pelo incentivo ao aprendizado, aulas divertidas e compreensão no contexto de pandemia.
