# Charger

![](https://github.com/ICMC/charger/blob/master/power.png)

## Diodo retificador:

Retifica sinais senoidais da corrente eletrica, permitindo que a corrende flua somente em um sentido, ou seja, ele     transforma a corrente alternada(eletrons fluem nos dois sentidos), em uma corrente continua, fluxo em apenas uma direção.Diodo emissor de luz(LED);

## Capacitores:
sua funcao é separar corrente alternada da continua, quando apresentam se simultaneamente,ele se comporta como circuito aberto em corrente continua e resistor em corrente alternada,o capacitor em paralelo na fonte serve para diminuir os “ruidos”!

## Regulador de Tensão :
### Aplicação do CI LM317:
O circuito usando o CI LM317 é mostrado abaixo.  O resistor R2 é o resistor de ajuste da tensão de saída e o resistor Rf é fixo no valor de 220 Ohm sendo este um valor recomendado pelo fabricante (na verdade o fabricante recomenda uma resistor de 240 Ohm)!
A idéia básica do circuito é ter um CI com saída fixa entre os pinos Vout e o pino de ajuste. A tensão de saída no CI LM317 é de 1,2 V e é chamada de tensão de referência Rref. Esta tensão fixa sobre o resistor Rf gera uma corrente constante em direção ao resistor R2 ajustável. O segredo do circuito é que a corrente sobre R2 é devido principalmente a corrente gerada sobre Rf desde que a corrente interna do CI que flui pelo pino  de ajuste é muito baixa. O fabricante constrói o CI de forma a ter 
uma corrente no pino de ajuste muito menor do que a corrente sobre o resistor Rf, de forma que, esta corrente possa ser desprezada no cálculo da tensão de saída!Para calcular a tensão de saída Vout você deve trabalhar na malha de saída e o resultado é mostrado abaixo:

_**Vout=Vref.(1+(Rf/R2))=1,2V(1+(Rf/R2))**_

Observe que também são empregados capacitores para estabilizar o circuito, estes capacitores devem ser de tântalo, se for usado capacitor comum de alumínio o valor dos capacitores deve ser aumentado de 10 vezes!O circuito é mostrado abaixo : 



![](https://github.com/ICMC/charger/blob/master/circuit.png)


## 3.7. CIRCUITOS RETIFICADORES
![](https://github.com/ICMC/charger/blob/master/circuitosRetificadores.png)

 * Circuitos retificadores a diodo são usados em fontes de alimentação cc para alimentar  um equipamento eletrônico.
 * A fonte é alimentada por uma rede elétrica ca de 60Hz com 120V (eficaz ou rms).
 * O retificador entrega uma tensão cc VO para um circuito eletrônico, representado pelo bloco “carga”.
 * O transformador de potência consiste em duas bobinas enroladas separadamente em um núcleo de ferro que acopla magneticamente os dois enrolamentos.
 * O enrolamento primário, com número de espiras N1, é conectado à fonte de alimentação.
 * O enrolamento secundário, com número de espiras N2, é conectado ao circuito da fonte de



alimentação cc.
* Pela escolha adequada da razão N1/N2 o projetista promove um abaixamento da tensão dalinha até um valor conveniente para produzir uma determinada tensão cc pela fonte.
* O transformador de linha também promove um  isolamento elétrico entre o equipamentoeletrônico e o circuito de potência da linha.
* Os diodos retificadores convertem a senóide de entrada vS em uma saída unipolar.
* A saída dos diodos retificadores possui valor médio diferente de zero e corresponde a uma forma de onda pulsante. 
* As variações na saída do retificador são reduzidas pelo bloco “filtro”.  
* A saída do filtro ainda contém ondulação. 
* Para reduzir a ondulação e estabilizar a tensão de  saída  cc da fonte contra variações causadas pela variação da corrente na carga, emprega-se um regulador de tensão(LM317T).”

