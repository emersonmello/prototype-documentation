---
layout: derivative
title: emersonMello's set
category: derivative
folder: emersonMello
---

<div id="notes">
<b>This document is intended to Portuguese speaking audience.</b><br>
Please use this document side-by-side the original documentation of Primo for the building instructions.<br>
<br><b>pt_BR:</b> Por favor, considere primeiro em ler a documentação original da Primo para só depois ver os ajustes que proponho. A documentação original omite alguns pontos importantes com relação a alimentação e facilidade para abertura do Cubetto e da interface de controle.<BR>
<BR>
<br>Emerson Ribeiro de Mello<br><BR>
License: <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>
</div>




## Lista de materiais

Esse projeto seguiu fielmente a lista de materiais do projeto original e foram acrescentados os seguintes itens:

### Cubetto

- 04 imãs ø 4 h 3
- [04 parafusos com porca 10mm x 3mm](images/parafuso-porca-10mm-3mm.jpg)
- [04 cantoneiras de fixação com 2 furos](images/cantoneira.png)
- [01 módulo Conversor XL6009 DC/DC Step-up](images/xl6009-step-up.png)
- [01 módulo Carregador De Baterias De Lítio TP4056](images/tp4056.png)
- [01 suporte duplo para 4 baterias AA](images/suporte-4aa.gif)
- [01 socket para CI (driver do motor)](images/socket-ci.jpg)
- 04 baterias AA recarregáveis 1.2v e 2300mAh
- 01 bateria 18650 3.7v
- [01 placa de fenolite Ilhada 4 X 6 cm PCB](images/placa-pcb-universal-dupla-face.jpg)
- [01 conector mini USB fêmea](images/usb-femea-mini.png) 
- [01 mini chave liga/desliga de alavanca](images/mini-chave-liga.png)
- [03 conectores JST-XH de 3 vias (macho e fêmea)](images/conector-jst-xh-3p-macho)
- 01 conector JST-XH de 4 vias (macho e fêmea)



### Interface de controle

- [08 porcas autotravantes 3mm com nylon](images/porca-01.png)
- 04 parafusos sem cabeça 15mm x 3mm (pode comprar uma barra e cortar no tamanho desejado)
- [04 espaçadores de nylon para fixar a placa Arduino Mega](images/espacador-nylon.png)
- [01 módulo Conversor XL6009 DC/DC Step-up](images/xl6009-step-up.png)
- [01 módulo Carregador De Baterias De Lítio TP4056](images/tp4056.png)
- [01 conector USB B fêmea](images/usb-b-femea.png)
- 01 bateria 18650 3.7v
- [01 suporte para bateria 18650](images/suporte-18650.jpg)
- [01 botão gangorra de liga/desliga](images/chave-kcd1-101-preta.jpg) 
- 01 led difuso vermelho 3mm
- 01 led difuso verde 3mm





## Montagem da interface de controle

A montagem da interface seguiu fielmente as instruções originais, contudo foi acrescentado itens para permitir a abertura da interface de controle e para carregar a bateria 18650 sem a necessidade de abertura.



### Processo de montagem



![colando as placas](images/photos/board-01.jpg)

![colando as placas](images/photos/board-02.jpg)



Coloquei os ímãs e apliquei cola de madeira por cima e quando essa secou, apliquei cola quente. Quero garantir que seja muito difícil para uma criança ter acesso a ele. 

![colando as placas](images/photos/board-03.jpg)



![interface de controle](images/photos/board-04.jpg)



Use o papel que protege a fita de cobre como guia para passar pelos orifícios na placa de MDF.

![interface de controle](images/photos/board-05.jpg)



Faça o mesmo para passar a fita de cobre pelos orifícios dos blocos de comando.

![interface de controle](images/photos/board-06.jpg)



![interface de controle](images/photos/board-08.jpg)

![interface de controle](images/photos/board-10.jpg)



![interface de controle](images/photos/board-07.jpg)

![interface de controle](images/photos/board-09.jpg)

![interface de controle](images/photos/board-13.jpg)



A ideia era montar um circuito que fosse possível recarregar a bateria sem que houvesse a necessidade de ter que abrir a interface de controle. Assim, pensei em usar uma bateria de lítio 18650 e o [módulo TP4056](images/tp4056.png) para carregá-la. Contudo, a bateria 18650 oferece 3.7V e, de acordo com a especificação oficial do [Arduino Mega 2560](https://store.arduino.cc/usa/arduino-mega-2560-rev3), é recomendado que a alimentação seja de 7V a 12V. Dessa forma, foi feito do [módulo Conversor XL6009 DC/DC Step-up](images/xl6009-step-up.png) para subir a tensão de 3.7V para 9V.  A figura abaixo ilustra a conexão entre bateria, TP4056, XL6009 e Arduino. Na figura também está representado o [botão gangorra de liga/desliga](images/chave-kcd1-101-preta.jpg).



![interface de controle](images/photos/board-18.jpg)



No projeto original do Cubetto (interface-board-4mm.dxf) já tem um recorte do tamanho correto para uma porta USB B fêmea. Imagino que a ideia inicial era colocar o ali a porta do próprio Arduino MEGA, porém eu aproveitei esse recorte para colocar uma porta USB B fêmea que está conectada no TP4056. Dessa forma, essa porta é usada para fazer o carregamento da bateria.

![interface de controle](images/photos/board-14.jpg)

Ao lado do recorte que usei para o conector USB B fêmea existe um outro recorte, que imagino eu, era para colocar o conector JACK de alimentação do Arduino. Aproveite esse espaço para colocar 2 leds (vermelho e verde) que foram soldados sobre os leds do módulo TP4056. Assim, quando estiver carregando a bateria é possível ver facilmente se a bateria já esta carregada (led verde aceso) ou se ainda está carregando (led vermelho aceso).

![interface de controle](images/photos/board-15.jpg)

![interface de controle](images/photos/board-17.jpg)



No projeto original para recorte do MDF já tem também um espaço para o botão liga/desliga do tipo gangorra.

![interface de controle](images/photos/board-16.jpg)



### Permitindo que a interface seja aberta por um adulto, mas não por uma criança



Foi feito uso de porcas autotravantes para permitir que um adulto com uma chave consiga abrir, mas não uma criança.

![porcas autotravantes](images/photos/board-11.jpg)



Optei por um barra de parafuso de 3mm e a cortei em pedaços de forma a permitir colocar uma porca autotravante na parte superior e na parte inferior da interface de controle. Isso foi motivado pela facilidade de só fazer 4 furos de 3mm na base em MDF da interface de controle.

![porcas autotravantes](images/photos/board-12.jpg)





##  Montagem do Cubetto

Comprei o motor e rodas sugeridos pelo projeto original na Solarbotics. Ao montar notei que os eixos dos dois motores se encostavam. Tive que cortar um pouco um dos eixos, como mostrado na figura abaixo.

![cubetto](images/photos/cubetto-01.jpg)



Para a alimentação do Cubetto pensei em uma solução que fosse possível recarregar as baterias sem que houvesse a necessidade de abrí-lo. Assim, coloquei uma porta mini USB femêa em um recorte da base do cubetto que inicialmente estava previsto uma peça de madeira, que no caso, optei por não colocá-la. 



![cubetto](images/photos/cubetto-04.jpg)



Assim como no caso da interface de controle, fiz uso de uma bateria 18650 de 3.7V, módulo de carregamento TP4056 e o módulo conversor DC/DC XL6009 para elevar a tensão para 7V e assim alimentar o Arduino. Fiz um furo na base o Cubetto para colocar uma [mini chave liga/desliga de alavanca](images/mini-chave-liga.jpg).

![cubetto](images/photos/cubetto-11.jpg)



Fiz alguns testes e percebi que a bateria 18650 não teria corrente suficiente para muitos movimentos do Cubetto. Sendo assim, optei por colocar 4 pilhas AA recarregáveis para alimentar exclusivamente o driver para motor SN754410. Ficou bem apertado, mas coube tudo dentro do Cubetto.

![cubetto](images/photos/cubetto-08.jpg)

![cubetto](images/photos/cubetto-10.jpg)

Como não pude fugir da ideia de ter que abrir o Cubetto para recarregar as 4 pilhas AA, fiz uso de 4 ímas, do mesmo tipo daqueles que foram usados na interface e blocos de controle, para ter uma forma fácil de abrir a parte superior do Cubetto e que não fosse tão fácil para uma criança, pois é necessário aplicar um pouco de força.

![cubetto](images/photos/cubetto-09.jpg)



Eu também preciso ter um acesso fácil aos motores, rodas, Arduino, etc para fazer manutenção, ou como constatei, para fazer inúmeros ajustes até conseguir fazer o Cubetto se movimentar corretamente. Sendo assim, colei as 4 laterais do Cubetto e deixei a tampa superior fixa somente por ímas e a parte de baixo fixa por 4 parafusos.

Tive que fazer 4 furos de 3mm na base do Cubetto e colei [cantoneiras](images/cantoneira.png) nas laterais. Essas cantoneiras são fáceis de achar em lojas que vendem peças para móveis planejados. Colei as porcas nas cantoneiras e assim, consigo abrir facilmente todo o Cubetto.

![cubetto](images/photos/cubetto-03.jpg)



![cubetto](images/photos/cubetto-02.jpg)



Os furos mais externos da placa de fenolite que usei tem a mesma largura de um *shield* para Arduino, então aproveite os pinos do XBee Shield para levar para essa placa os pinos 2 e 3 do Arduino, usados pelos *encoders* ópticos das rodas e os pinos PWM para cada motor.

![cubetto](images/photos/cubetto-14.jpg)

![cubetto](images/photos/cubetto-15.jpg)

![cubetto](images/photos/cubetto-05.jpg)



Abaixo um diagrama com todos os componentes dentro do Cubetto.



![cubetto](images/componentes-cubetto.png)





## Códigos fonte para Arduino

Fiz algumas alterações nos códigos originais do Cubetto e da interface de controle. As alterações corrigiram pequenos *bugs*, adicionaram facilidades como o retorno visual para a criança, quando os blocos são inseridos incorretamente. [Os códigos fontes estão disponíveis aqui](https://github.com/emersonmello/arduino-sketches). 