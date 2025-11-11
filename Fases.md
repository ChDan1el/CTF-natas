# Introdução

O CTF [Natas](https://overthewire.org/wargames/natas/) é um desafio focado em hacking real, tendo fases de 1 a 34, aumentando o nível de dificuldade e conhecimento ao extremo.

## [natas0](http://natas0.natas.labs.overthewire.org)

A primeira fase é uma etapa da introdução do CTF

Inspecionando a página já se encontra a flag

[![Captura-de-tela-2025-11-05-105804.png](https://i.postimg.cc/VLJ5rnh4/Captura-de-tela-2025-11-05-105804.png)](https://postimg.cc/56MfDYbF)

**FLAG:** 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq

## [natas1](http://natas1.natas.labs.overthewire.org)
Tentei inspecionar o HTML com o botão direito, mas não fui permitido

[![Captura-de-tela-2025-11-05-110059.png](https://i.postimg.cc/Sxj5pNJQ/Captura-de-tela-2025-11-05-110059.png)](https://postimg.cc/qNVQsrsW)

Então uso um comando de teclado que inspeciona uma página, Ctrl + U e já encontro a flag

[![Captura-de-tela-2025-11-05-110249.png](https://i.postimg.cc/1tKMqL8Z/Captura-de-tela-2025-11-05-110249.png)](https://postimg.cc/BLXxW75h)

**FLAG:** TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI

## [natas2](http://natas2.natas.labs.overthewire.org)

Usando o comando Ctrl + U na página sou redirecionado para o HTLM.

[![Captura-de-tela-2025-11-05-111133.png](https://i.postimg.cc/h45T5DW9/Captura-de-tela-2025-11-05-111133.png)](https://postimg.cc/rz5DdLpm)

Há um novo arquivo indexado chamado "files/pixel.png", então verifico oque há nele

[![Captura-de-tela-2025-11-11-202317.png](https://i.postimg.cc/j2mghBrD/Captura-de-tela-2025-11-11-202317.png)](https://postimg.cc/BP5BSYb3)

Há somente um pixel na página, mas percebo no URL que antes de chegar a esse diretório, passou pelo files antes. Então decido procurar no diretório files

[![Captura-de-tela-2025-11-05-111630.png](https://i.postimg.cc/mrnHh438/Captura-de-tela-2025-11-05-111630.png)](https://postimg.cc/B8x6wdVK)

Clicando no users.txt encontro a flag

[![Captura-de-tela-2025-11-05-111727.png](https://i.postimg.cc/W3Ps5fsv/Captura-de-tela-2025-11-05-111727.png)](https://postimg.cc/XZQMJLZH)

**FLAG:** 3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH
