---
title: 'USBTINYISP'
subtitle: 'Programador de microcontroladores AVR'
date: 2017-04-11 00:00:00
featured_image: '/images/usbtiny/usbtiny_01.jpeg'
---

![](/images/usbtiny/usbtiny_01.jpeg)

Uma das principais ferramentas no desenvolvimento de projetos com microcontroladores é o chamado programador, ou gravador, responsável por entre diversas coisas enviar o programa desenvolvido para a memória de programa do microcontrolador, para ele assim desempenhar a função desejada. Existem diversos equipamentos que desempenham esta função e eles são basicamente uma interface entre um computador e o microcontrolador que se deseja programar, variando em compatibilidade de famílias de microcontroladores e porta de comunicação com um computador, sendo hoje mais usual ferramentas USB, embora programadores que utilizavam portas paralela tenham sido muito populares num tempo em que este barramento era comum, principalmente em computadores de mesa.

O projeto aqui descrito é de um programador para microcontroladores AVR e interface SPI por meio de conexão USB de baixo custo e fácil montagem, sendo muito interessante para pessoas que estão iniciando estudos com microcontroladores e tem interesse em montagem em placa de circuito impresso. Baseado no projeto de código aberto USBtinyISP, desenvolvido por Ladyada, a versão aqui proposta possui como principal modificação, com a finalidade de facilitar a sua montagem, a troca do ressonador cerâmico, dada a baixa disponibilidade no mercado brasileiro, por um cristal de mesma frequência e dois capacitores. Outras alterações feitas consistem basicamente no desenho da placa de circuito impresso. Como restrições este programador somente suporta microcontroladores com 64KBytes de memória flash ou menos. Microcontroladores com interface TPI, como Attiny4/5/9/10 também não podem sem programados com este dispositivo.

### Montagem do circuito

Para a montagem é indicado o uso das seguintes **ferramentas**:

* Ferro ou estação de solda
* Estanho
* Sugador de solda
* Alicate de corte
* Suporte com lupa
* Multímetro

![](/images/usbtiny/usbtiny_02.jpeg)

Abaixo a lista de *componentes* usados na montagem do circuito:

* 1 x Placa de circuito impresso
* 1 x Capacitor cerâmico 0,1 uF
* 1 x Capacitor eletrolítico 100 uF
* 2 x Capacitor cerâmico 22 pF
* 2 x Resistor 33Ω
* 1 x Resistor 10KΩ
* 5 x Resistor 1,5KΩ
* 1 x Cristal 16 MHz
* 2 x Diodo zener 3V6
* 1 x LED 5mm verde difuso
* 1 x LED 5mm vermelho difuso
* 1 x ATtiny2313A
* 1 x 74HC125
* 1 x Conector USB B fêmea
* 1 x Soquete estampado 20 pinos
* 1 x Soquete estampado 14 pinos
* 1 x Pin header 1x2
* 1 x Pin header 2x3
* 1 x Jumper

![](/images/usbtiny/usbtiny_03.jpeg)

Com o uso do multímetro no modo de teste de continuidade deve ser feita uma busca por possíveis problemas na montagem, como curto-circuitos e falsos contatos oriundos de soldas mal feitas.

![](/images/usbtiny/usbtiny_04.jpeg)

Após checagem do circuito basta inserir os circuitos integrados em seus respectivos soquetes e o programador está pronto para ser conectado a um computador.

![](/images/usbtiny/usbtiny_05.jpeg)

## Como usar o programador
### Jumper para seleção de alimentação

Enquanto o jumper fechar os contatos do pin header JP2 presente na placa a conexão USB do programador alimentara o circuito ao qual o cabo ISP está conectado, fornecendo 5V. Caso a tensão de operação do circuito seja menor, como 3,3V por exemplo, ou o circuito de interesse consumir mais do que 100mA basta remover o jumper e alimentar o circuito de forma independente.

### LEDs indicadores

São presentes na placa dois LEDs, um verde e um vermelho. O LED verde indica presença de conexão USB, enquanto o LED vermelho indica progresso no procedimento de programação.

### Programação do Bootloader em uma placa Arduino

A programação de bootloader em uma placa Arduino pode ser feita diretamente por meio do próprio software para desenvolvimento Arduino, conhecido como IDE(Integrated Development Environment).

![](/images/usbtiny/usbtiny_06.jpeg)

Com o uso de um cabo ISP de 6 pinos é feita a conexão entre o programador e a placa Arduino. Atente ao fato de que se deve conectar o cabo respeitando a ordem dos pinos, sendo o pino número 1 sinalizado pela linha vermelha no cabo. No conector ISP do programador um chanfro impede que o cabo seja conectado ao contrário.

![](/images/usbtiny/usbtiny_07.jpeg)

No menu **Ferramentas** deve ser escolhida a placa de interesse no sub-menu **Placa**, e o programador no sub-menu **Programador**, devendo ser selecionado o programador **USBtinyISP**.

<div class="gallery" data-columns="2">
	<img src="/images/usbtiny/usbtiny_08.png">
	<img src="/images/usbtiny/usbtiny_09.png">
</div>

Para iniciar a gravação do *bootloader* deve ser pressionado o comando **Gravar Bootloader**.

![](/images/usbtiny/usbtiny_10.png)

Após comando de gravação o progresso pode ser visto acima do console da IDE, onde também é sinalizada a sua conclusão.

<div class="gallery" data-columns="2">
	<img src="/images/usbtiny/usbtiny_11.png">
	<img src="/images/usbtiny/usbtiny_12.png">
</div>

### Gravação de sketch Arduino com o uso de programador

Outro recurso presente na *IDE Arduino* é de o carregamento da *sketch* diretamente para um microcontrolador sem que seja necessária a gravação do *bootloader* e transferência via comunicação serial. Isso é feito por meio do comando **Carregar usando programador** presente no menu **Sketch**. Este recurso é muito interessante pois torna possível a montagem de circuitos programados em *Wiring* na IDE Arduino com poucos componentes e menor custo.

![](/images/usbtiny/usbtiny_13.png)

### Uso com a ferramenta AVRDUDE

A ferramenta [AVRDUDE](http://www.nongnu.org/avrdude/) é um programa em linha de comando bastante popular utilizado na gravação de microcontroladores da família AVR da Atmel, e está presente na ferramenta de desenvolvimento [WinAVR](http://www.webring.org/l/rd?ring=avr;id=59;url=http%3A%2F%2Fwinavr%2Esourceforge%2Enet%2F) para sistemas Windows.

Para testar o funcionamento do programador basta executar o comando **avrdude -c <programmer> -p <partno>**, sendo o argumento -c o referente ao tipo de programador e o argumento -p referente ao dispositivo AVR que será gravado. Utilizando a montagem apresentada anteriormente com a ligação do programador a uma placa Arduino Duemilanove, que possui um microcontrolador ATmega328p, o comando a ser executado é **avrdude -c usbtiny -p atmega328p**. Se tudo estiver correto uma resposta como a da imagem a seguir é apresentada.

![](/images/usbtiny/usbtiny_14.png)

## Aviso importante!

O conteúdo aqui presente contém muitas referências ao projeto desenvolvido por [*Adafruit Industries*](https://www.adafruit.com/), ao qual se baseia, cujo conteúdo original pode ser acessado através do seguinte link [USBtinyISP](https://learn.adafruit.com/usbtinyisp/overview).

O [repositório github](https://github.com/andrebla/usbtinyispfzrs) guarda os arquivos de esquemático e desenho de placa de circuito impresso para o *software* EagleCAD.

<a href='/' class="button button--large">Voltar</a>