---
title: 'Como usar joysticks para controlar seus projetos com Arduino'
subtitle: ''
date: 2011-02-13 00:00:00
featured_image: '/images/logo_02.jpeg'
---

Neste primeiro post vou descrever através de um simples projeto uma forma de utilizar seus periféricos (mouse, teclado, joysticks etc.) conectados ao pc como entrada de parâmetros para o Arduino utilizando a comunicação serial. A forma mais trivial que encontrei para fazer isto foi através do Processing, utilizando a biblioteca proCONTROLL, escrita por Christian Riekoff, a documentação detalhada e cheia de exemplos facilita bastante na hora de escrever o código. Fiz esse projeto com a simples intenção de entender melhor a comunicação serial com o processing e brincar com a biblioteca proCONTROLL. Vamos para o projeto em si, ele consiste em mandar simples comandos com meu controle de Guitar Hero para acionar leds, enquanto um botão está pressionado o led referente a este botão fica aceso.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/VTTamp6J508?controls=0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<a href='/' class="button button--large">Voltar</a>