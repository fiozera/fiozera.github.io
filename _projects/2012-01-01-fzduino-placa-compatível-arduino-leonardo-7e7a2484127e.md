---
title: 'FZDUINO'
subtitle: 'Placa compatível Arduino Leonardo'
date: 2012-01-01 00:00:00
featured_image: '/images/fzduino/fzduino_01.jpg'
---

Com o propósito de fazer uma placa compatível Arduino de baixo custo que pudesse ser acomodada em uma matriz de contatos e após a liberação da versão release candidate 1.0 da IDE do Arduino, que já contém o bootloader empregado aqui, a possibilidade de uma placa utilizando o microcontrolador Atmel AVR atmega32u4, que já possui suporte USB, se tornou uma tarefa mais simples. O suporte a USB nativo dado pelo microcontrolador dispensa o uso de conversores serial/USB necessários em outras placas a exemplo do Arduino Duemilanove e UNO o que torna a placa mais simples e reduzida, embora o microcontrolador atmega32u4 somente exista em encapsulamento smd o que dificulta a montagem para aqueles que não possuem muita pratica em soldagem desse tipo de componente. Para reduzir ainda mais as dimensões da placa para permitir o uso em uma matriz de contatos também foram empregados resistores e capacitores smd. Para a programação inicial do bootloader no microcontrolador presente na placa foi utilizado o programador USBTINYISP, já detalhador em outro post, e a IDE Arduino 1.0 release candidate. O repositório no github contém os arquivos da placa feitos no software Eagle.

### Links:
* [Repositório](https://github.com/andrebla/fzduino)

<div class="gallery" data-columns="3">
	<img src="/images/fzduino/fzduino_02.jpg">
	<img src="/images/fzduino/fzduino_03.jpg">
	<img src="/images/fzduino/fzduino_04.jpg">
</div>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Ak8JPkltOgs?controls=0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<a href='/' class="button button--large">Voltar</a>