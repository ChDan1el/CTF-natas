# Introdução

O CTF [Natas](https://overthewire.org/wargames/natas/) é um desafio focado em hacking real, tendo fases de 1 a 34, aumentando o nível de dificuldade e conhecimento ao extremo.

## [natas0](http://natas0.natas.labs.overthewire.org)
###### Usuário: natas0
###### Senha: natas0

A primeira fase é uma etapa da introdução do CTF

Inspecionando a página já se encontra a flag

[![Captura-de-tela-2025-11-05-105804.png](https://i.postimg.cc/VLJ5rnh4/Captura-de-tela-2025-11-05-105804.png)](https://postimg.cc/56MfDYbF)

**FLAG:** 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq

## [natas1](http://natas1.natas.labs.overthewire.org)
###### Usuário: natas1
###### Senha: 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq

Tentei inspecionar o HTML com o botão direito, mas não fui permitido

[![Captura-de-tela-2025-11-05-110059.png](https://i.postimg.cc/Sxj5pNJQ/Captura-de-tela-2025-11-05-110059.png)](https://postimg.cc/qNVQsrsW)

Então uso um comando de teclado que inspeciona uma página, Ctrl + U e já encontro a flag

[![Captura-de-tela-2025-11-05-110249.png](https://i.postimg.cc/1tKMqL8Z/Captura-de-tela-2025-11-05-110249.png)](https://postimg.cc/BLXxW75h)

**FLAG:** TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI

## [natas2](http://natas2.natas.labs.overthewire.org)
###### Usuário: natas2
###### Senha: TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI

Usando o comando Ctrl + U na página sou redirecionado para o HTLM.

[![Captura-de-tela-2025-11-05-111133.png](https://i.postimg.cc/h45T5DW9/Captura-de-tela-2025-11-05-111133.png)](https://postimg.cc/rz5DdLpm)

Há um novo arquivo indexado chamado "files/pixel.png", então verifico oque há nele

[![Captura-de-tela-2025-11-11-202317.png](https://i.postimg.cc/j2mghBrD/Captura-de-tela-2025-11-11-202317.png)](https://postimg.cc/BP5BSYb3)

Há somente um pixel na página, mas percebo no URL que antes de chegar a esse diretório, passou pelo **files** antes. Então decido procurar no diretório files

[![Captura-de-tela-2025-11-05-111630.png](https://i.postimg.cc/mrnHh438/Captura-de-tela-2025-11-05-111630.png)](https://postimg.cc/B8x6wdVK)

Clicando no users.txt encontro a flag

[![Captura-de-tela-2025-11-05-111727.png](https://i.postimg.cc/W3Ps5fsv/Captura-de-tela-2025-11-05-111727.png)](https://postimg.cc/XZQMJLZH)

**FLAG:** 3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH

## [natas3](http://natas3.natas.labs.overthewire.org)
###### Usuário: natas3
###### Senha: 3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH

Primeira coisa que faço é inspecionar a página, assim encontro uma dica

[![Captura-de-tela-2025-11-12-104016.png](https://i.postimg.cc/CK34VNXz/Captura-de-tela-2025-11-12-104016.png)](https://postimg.cc/f3vdcxwN)

Essa dica me leva a pasta [robots.txt](https://www.cloudflare.com/pt-br/learning/bots/what-is-robots-txt/)

<img width="562" height="115" alt="image" src="https://github.com/user-attachments/assets/ff5a4983-1987-48aa-9d14-60abe90114d5" />

Nessa página encontro um diretório que não está indexado diretamento no google, /s3cret, então coloco esse diretório no final da URL

<img width="633" height="287" alt="image" src="https://github.com/user-attachments/assets/0c7ba5a0-0ed0-43ca-b828-0ce49e3c6286" />

Aqui encontro um link de usuários, achando por fim a flag

<img width="609" height="100" alt="image" src="https://github.com/user-attachments/assets/de5da0fc-2714-4ee0-b333-b8b51bc40264" />

**FLAG:** QryZXc2e0zahULdHrtHxzyYkj59kUxLQ

## [natas4](http://natas4.natas.labs.overthewire.org)
###### Usuário: natas4
###### Senha: QryZXc2e0zahULdHrtHxzyYkj59kUxLQ

De cara já encontro uma mensagem que não tenho acesso a página, só sendo permitido acessar com o URL de natas5. Recarregando a página, confirmo a mensagem, pois estou com a URL de natas4

<img width="956" height="365" alt="image" src="https://github.com/user-attachments/assets/450e744f-99a6-45db-a1de-dbf1f743a247" />

Já que só consigo acessar a flag através da URL de natas5, usarei uma ferramenta do Kali Linux, [Burp Suite](https://pt.wikipedia.org/wiki/Burp_Suite), para inteceptar a [requisição de site](https://www.hostinger.com/br/tutoriais/servidor-proxy) e mudar o 
meu endereço para natas5

Após abrir o burp suite vou para a aba Proxy, abro o browser próprio, coloco a URL do natas4 e clico para interceptar a requesição

<img width="1621" height="592" alt="image" src="https://github.com/user-attachments/assets/f5e22b71-b2c4-4d09-a0d7-3f5fef2e9f9a" />

Depois de recarregar a página o programa intercepta a requisição

<img width="1590" height="846" alt="image" src="https://github.com/user-attachments/assets/8de900c9-c7e2-4630-ab2a-7e2c7d60d553" />

Então é só alterar o endereço na parte de **Referer** para o qual o desafio pede, mudando para "http://natas5.natas.labs.overthewire.org/" e encaminhar para o Proxy bo botão laranja

<img width="1028" height="186" alt="image" src="https://github.com/user-attachments/assets/f0916438-0355-4383-b835-b11980e96481" />

Ganhando o acesso a página consigo a flag

<img width="923" height="273" alt="image" src="https://github.com/user-attachments/assets/df8b47c3-7a26-46e9-bc64-0fd724e9c9d9" />

**FLAG:** 0n35PkggAPm2zbEpOU802c0x0Msn1ToK

## [natas5](http://natas5.natas.labs.overthewire.org)
###### Usuário: natas5
###### Senha: 0n35PkggAPm2zbEpOU802c0x0Msn1ToK

Acesso negado, pois não estou *logado*. Isso dá uma dica sobre os [cookies](https://www.kaspersky.com.br/resource-center/definitions/cookies) do site

<img width="656" height="235" alt="image" src="https://github.com/user-attachments/assets/8d942baa-d3b1-45d3-9cce-c9b1d4a8e535" />

O valor de **loggedin** está com valor 0, oque normalmente significa negação, então defino o valor como 1, recarrego a página e logo é mostrado a flag



