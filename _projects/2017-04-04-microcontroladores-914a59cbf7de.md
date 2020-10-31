---
title: 'Microcontroladores'
subtitle: ''
date: 2017-04-04 00:00:00
featured_image: '/images/microcontroladores/microcontroladores_thumb.png'
---

Um circuito integrado bastante versátil e muito utilizado em aplicações de sistemas digitais é o microcontrolador, sendo objeto de estudo quase que obrigatório para aqueles que tem interesse na área, e como um grande número de fabricantes e famílias de microcontroladores pode ser encontrado no mercado, cada uma com suas especificidades e características, a escolha de um circuito integrado em específico depende bastante da aplicação, portanto conhecer este componente é fundamental. Este artigo tem o intuito de descrever algumas das características e funcionalidades dos microcontroladores.

![](/images/microcontroladores/microcontroladores_01.png)

Muito associado a processadores o microcontrolador é mais do que somente uma unidade central de processamento (CPU, do inglês Central Processing Unit), ele possuí periféricos que o tornam capaz de exercer muitas funções sem depender de muitos outros componentes a ele conectados. Pode se dizer que um microcontrolador é uma espécie de computador, constituído de um processador(CPU), memória de armazenamento de programa, memória para armazenamento de variáveis, além de alguns possuírem periféricos para comunicação, conversão analógico/digital etc, e como um computador é programado por meio das chamadas linguagens de programação, como a linguagem C.

![](/images/microcontroladores/microcontroladores_02.png)

Se novamente comparado a computadores pessoais os microcontroladores possuem recursos limitados que trazem algumas limitações se comparados a computadores, como frequência de clock, tamanho de memória de programa e memória RAM etc, mas trazem como grande vantagem o baixo custo, baixo consumo energético e pequenas dimensões, tendo assim inúmeras aplicações.

O microcontrolador é o principal componente presente nas placas de desenvolvimento compatíveis Arduino, muito popular entre estudantes por conta da vasta documentação e principalmente pela grande comunidade de usuários, além de ser uma plataforma bastante amigável para iniciantes.

![](/images/microcontroladores/microcontroladores_03.png)

---

### Aplicações de microcontroladores

Em nosso cotidiano utilizamos muitos equipamentos que possuem internamente um microcontrolador, como eletroeletrônicos e eletrodomésticos. O timer de um aparelho microondas, o controle remoto de um aparelho televisor ou ar condicionado, um relógio digital, o controlador de voo de um drone, uma impressora 3D e muitos outros dispositivos podem ser construídos fazendo uso de microcontroladores.

### Principais constituintes de um microcontrolador:

* **CPU(Unidade central de processamento):** responsável por executar operações lógicas e matemáticas programadas.
* **Frequência de clock:** base de tempo para as operações desempenhadas pela CPU e demais periféricos presentes no microcontrolador.
* **Memória flash:** memória não volátil, ou seja, não tem seu conteúdo apagado com a falta de alimentação. É responsável por armazenar o programa a ser executado.
* **Memória RAM:** memória volátil responsável por armazenar temporariamente variáveis do programa, como variáveis de entrada, ou variáveis de cálculo.
* **Memória EEPROM:** memória não volátil, assim como a memória flash, tendo em comparação a esta uma menor velocidade de escrita.
* **Entradas:** pinos configurados como entradas digitais detectam a tensão presente externamente neles, dados alguns valores limiares. Quando abaixo de determinado valor de tensão, dado presente na folha de dados do microcontrolador de interesse, o nível lógico lido é 0, já se dentro de uma faixa próxima do valor de alimentação, também dependente do microcontrolador em questão, o nível lógico lido é 1. Conectando chaves ou interruptores a pinos de entrada é possível alterar estados de variáveis dentro do software em execução no microcontrolador, fazendo com que o programa execute alguma tarefa de interesse.
* **Saídas:** pinos configurados como saídas digitais podem ser comandados por meio do software e ter seu valor de tensão assim alterado. Nível lógico 0 representa valor de tensão nulo, já nível lógico 1 representa valor de tensão de alimentação do circuito. A saída digital dos microcontroladores é a principal interface deste componente com o mundo real, bastando conectar um LED e fazê-lo piscar, ou um pequeno alto-falante para emitir um sinal sonoro.

Alguns outros periféricos são comumente encontrados em um grande número de microcontroladores, e trazem funcionalidades muito interessantes, abaixo são listados alguns:

### Conversão analógico/digital

Um grande número de sensores operam com valores contínuos de tensão, e portanto não podem ser usados diretamente por meio das portas digitais dos microcontroladores. Para ler os valores de tensão destes sensores e manipula-los de forma digital é preciso primeiramente convertê-los, e um dispositivo capaz disto é o conversor analógico/digital(ADC, do inglês Analog to digital converter). Muitos microcontroladores possuem ADC integrado, não necessitando que este dispositivo seja conectado externamente.

### Comunicação serial

A comunicação serial permite a interligação entre um microcontrolador e um computador, ou outros dispositivos. Este periférico é bastante comum em muitas famílias de microcontroladores e trás capacidades muito interessantes, como a leitura de dados de sensores, ou interfaces de entrada, por meio dos microcontroladores que enviam estas leituras para um computador, capaz de usar estes dados em aplicações robustas, como a visualização de dados em uma tela de alta resolução. Utilizar um microcontrolador como dispositivo de saída também é possível, para por exemplo acionar motores por meio de comandos oriundos de um computador. É por meio deste periférico também que se conectam módulos de comunicação sem fio bastante populares, como módulos Bluetooth e WiFi, que expandem as capacidades de operação de circuitos microcontrolados.

![](/images/microcontroladores/microcontroladores_04.png)

Em resumo microcontroladores são componentes capazes de executar programas que fazem uso de seus recursos internos, como a leitura e escrita digital na forma de valores de tensão em suas portas, além da comunicação com componentes externos, permitindo expansão de suas capacidades. Com simples recursos os microcontroladores podem ser utilizados em uma inúmera gama de aplicações.

<a href='/' class="button button--large">Voltar</a>