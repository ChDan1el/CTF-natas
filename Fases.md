<img width="1003" height="198" alt="image" src="https://github.com/user-attachments/assets/dad7e826-f3b3-4366-afb6-172df1e95deb" /># Introdução

O CTF [Natas](https://overthewire.org/wargames/natas/) é um desafio focado em hacking real, tendo fases de 1 a 34, aumentando o nível de dificuldade e conhecimento ao extremo.

## [natas0](http://natas0.natas.labs.overthewire.org)
###### Usuário: natas0
###### Senha: natas0

Quando começamos uma questão de web hacking, o primeiro procedimento é verificar o HTML do site. E aqui já está a *flag*

[![Captura-de-tela-2025-11-05-105804.png](https://i.postimg.cc/VLJ5rnh4/Captura-de-tela-2025-11-05-105804.png)](https://postimg.cc/56MfDYbF)

**FLAG:** 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq

## [natas1](http://natas1.natas.labs.overthewire.org)
###### Usuário: natas1
###### Senha: 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq

Essa questão é semelhante ao natas0

Tentei inspecionar o código HTML clicando com o botão direito, mas o site não permitiu

[![Captura-de-tela-2025-11-05-110059.png](https://i.postimg.cc/Sxj5pNJQ/Captura-de-tela-2025-11-05-110059.png)](https://postimg.cc/qNVQsrsW)

Então uso o atalho de teclado **Ctrl + U** para inspecionar o código da página e assim encontro a *flag*

[![Captura-de-tela-2025-11-05-110249.png](https://i.postimg.cc/1tKMqL8Z/Captura-de-tela-2025-11-05-110249.png)](https://postimg.cc/BLXxW75h)

**FLAG:** TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI

## [natas2](http://natas2.natas.labs.overthewire.org)
###### Usuário: natas2
###### Senha: TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI

Ao pressionar **Ctrl + U** na página, sou levado ao código-fonte HTML

[![Captura-de-tela-2025-11-05-111133.png](https://i.postimg.cc/h45T5DW9/Captura-de-tela-2025-11-05-111133.png)](https://postimg.cc/rz5DdLpm)

Há um novo arquivo indexado chamado "files/pixel.png", então verifico o que há nele

[![Captura-de-tela-2025-11-11-202317.png](https://i.postimg.cc/j2mghBrD/Captura-de-tela-2025-11-11-202317.png)](https://postimg.cc/BP5BSYb3)

A página exibe apenas um único pixel, porém, ao observar a URL, percebo que o caminho passa pelo diretório /files. Diante disso, decido explorar o conteúdo desse diretório em busca de novas pistas da flag

[![Captura-de-tela-2025-11-05-111630.png](https://i.postimg.cc/mrnHh438/Captura-de-tela-2025-11-05-111630.png)](https://postimg.cc/B8x6wdVK)

Clicando no users.txt encontro a *flag*

[![Captura-de-tela-2025-11-05-111727.png](https://i.postimg.cc/W3Ps5fsv/Captura-de-tela-2025-11-05-111727.png)](https://postimg.cc/XZQMJLZH)

**FLAG:** 3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH

## [natas3](http://natas3.natas.labs.overthewire.org)
###### Usuário: natas3
###### Senha: 3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH

O primeiro passo foi inspecionar o código da página, onde encontrei uma dica

[![Captura-de-tela-2025-11-12-104016.png](https://i.postimg.cc/CK34VNXz/Captura-de-tela-2025-11-12-104016.png)](https://postimg.cc/f3vdcxwN)

Essa dica me leva a pasta [robots.txt](https://www.cloudflare.com/pt-br/learning/bots/what-is-robots-txt/)

<img width="562" height="115" alt="image" src="https://github.com/user-attachments/assets/ff5a4983-1987-48aa-9d14-60abe90114d5" />

Ao analisar a página, identifico um diretório oculto, /s3cr3t, que não está indexado no Google. Em seguida, adiciono esse caminho ao final da URL para acessar seu conteúdo

<img width="633" height="287" alt="image" src="https://github.com/user-attachments/assets/0c7ba5a0-0ed0-43ca-b828-0ce49e3c6286" />

Aqui encontro um link para usuários e, por fim, encontro a *flag*

<img width="609" height="100" alt="image" src="https://github.com/user-attachments/assets/de5da0fc-2714-4ee0-b333-b8b51bc40264" />

**FLAG:** QryZXc2e0zahULdHrtHxzyYkj59kUxLQ

## [natas4](http://natas4.natas.labs.overthewire.org)
###### Usuário: natas4
###### Senha: QryZXc2e0zahULdHrtHxzyYkj59kUxLQ

De cara, já encontro uma mensagem informando que não tenho acesso à página, sendo permitido o acesso apenas com a URL de natas5. Após recarregar a página, confirmo a mensagem, pois estou utilizando a URL de natas4

<img width="956" height="365" alt="image" src="https://github.com/user-attachments/assets/450e744f-99a6-45db-a1de-dbf1f743a247" />

Como o acesso à flag só é possível pela URL natas5, irei utilizar o [Burp Suite](https://pt.wikipedia.org/wiki/Burp_Suite) do Kali Linux para interceptar a [requisição HTTP](https://www.hostinger.com/br/tutoriais/servidor-proxy) e alterar a URL para natas5

Com o **Burp Suite** aberto, navego até a aba Proxy, inicio o browser integrado e insiro a URL de natas4. Em seguida, ativo a interceptação de requisições para capturar a requisição HTTP e poder modificá-la

<img width="1621" height="592" alt="image" src="https://github.com/user-attachments/assets/f5e22b71-b2c4-4d09-a0d7-3f5fef2e9f9a" />

Ao recarregar a página, o **Burp Suite** intercepta a requisição HTTP

<img width="1590" height="846" alt="image" src="https://github.com/user-attachments/assets/8de900c9-c7e2-4630-ab2a-7e2c7d60d553" />

Basta alterar o cabeçalho **Referer** para "http://natas5.natas.labs.overthewire.org/" e, em seguida, encaminhar a requisição ao proxy usando o botão laranja

<img width="1028" height="186" alt="image" src="https://github.com/user-attachments/assets/f0916438-0355-4383-b835-b11980e96481" />

Ao ganhar acesso à página, consigo a *flag*.

<img width="923" height="273" alt="image" src="https://github.com/user-attachments/assets/df8b47c3-7a26-46e9-bc64-0fd724e9c9d9" />

**FLAG:** 0n35PkggAPm2zbEpOU802c0x0Msn1ToK

## [natas5](http://natas5.natas.labs.overthewire.org)
###### Usuário: natas5
###### Senha: 0n35PkggAPm2zbEpOU802c0x0Msn1ToK

Acesso negado, pois não estou *autenticado*. Isso dá uma dica sobre os [cookies](https://www.kaspersky.com.br/resource-center/definitions/cookies) do site

<img width="656" height="235" alt="image" src="https://github.com/user-attachments/assets/8d942baa-d3b1-45d3-9cce-c9b1d4a8e535" />

O valor de **loggedin** está definido como 0, o que normalmente indica negação.

<img width="1046" height="464" alt="image" src="https://github.com/user-attachments/assets/f75636ac-56c1-4f19-b5bd-d190f530a2fc" />


Então, altero o valor para 1, recarrego a página e, em seguida, a *flag* é exibida

[![Captura-de-tela-2025-11-12-125652.png](https://i.postimg.cc/sXzfNT5h/Captura-de-tela-2025-11-12-125652.png)](https://postimg.cc/R3Pz3QsS)

**FLAG:** 0RoJwHdSKWFTYR5WuiAewauSuNaBXned

## [natas6](http://natas6.natas.labs.overthewire.org)
###### Usuário: natas6
###### Senha: 0RoJwHdSKWFTYR5WuiAewauSuNaBXned

Logo na primeira página da fase já disponibilizam o acesso do código do login, então clico para analisar

<img width="621" height="205" alt="Captura de tela 2025-11-18 151244" src="https://github.com/user-attachments/assets/734e8cba-4d96-4ce4-9160-e13a06569d62" />

Analisando o código percebo que ele puxa informações de outro diretório, sendo o includes/secret.inc

<img width="519" height="159" alt="image" src="https://github.com/user-attachments/assets/54869012-dcb6-4d4f-ac05-b93875ea06de" />

Então adiciono o nome do diretório no final da URL e consigo a senha da página

<img width="445" height="33" alt="image" src="https://github.com/user-attachments/assets/7050c1ef-7632-43ca-8c84-f503d27cdd02" />

<img width="313" height="78" alt="Captura de tela 2025-11-18 151436" src="https://github.com/user-attachments/assets/d1040b7d-d778-4e13-b9f0-d6044b80bf8e" />

Após inserir a senha no input secret, consigo a *flag*

<img width="623" height="248" alt="Captura de tela 2025-11-18 151501" src="https://github.com/user-attachments/assets/e33eafee-3e4e-40a7-8382-28976428c694" />


**FLAG:** bmg8SvU1LizuWjx3y7xkNERkHxGre0GS

## [natas7](http://natas7.natas.labs.overthewire.org)
###### Usuário: natas7
###### Senha: bmg8SvU1LizuWjx3y7xkNERkHxGre0GS

Logo na pagina inicial há somente dois botões, de *home* e *about*. Então ao clicar neles percebo um padrão de URL, sempre terminando com **index.php?page=** e o nome da pagina

<img width="682" height="280" alt="Captura de tela 2025-12-01 205528" src="https://github.com/user-attachments/assets/94ad4c1b-ef1c-4527-ad4e-ec2a17d589a2" />

<img width="654" height="261" alt="Captura de tela 2025-12-01 205540" src="https://github.com/user-attachments/assets/5e532944-ed3a-4269-b50d-c61144d346da" />

Inspecionando o HTML encontro uma dica: A *flag* está na pagina /etc/natas_webpass/natas8

<img width="912" height="730" alt="Captura de tela 2025-12-01 205558" src="https://github.com/user-attachments/assets/13767eb7-29b0-49a4-9639-f74ec10c8b5b" />

Então já que a URL puxa a pagina com o nome, coloco o nome na pagina da *flag* na URL

<img width="1304" height="376" alt="Captura de tela 2025-12-01 205436" src="https://github.com/user-attachments/assets/eb8f0721-4420-444b-99a1-1d2a3b832f04" />

E aqui já está a *flag*

**FLAG:** xcoXLmzMkoIP9D7hlgPlh9XD7OgLAe5Q

## [natas8](http://natas8.natas.labs.overthewire.org)
###### Usuário: natas8
###### Senha: xcoXLmzMkoIP9D7hlgPlh9XD7OgLAe5Q

Logo na pagina inicial já posso analisar o código por trás do desafio

<img width="1125" height="350" alt="Captura de tela 2025-12-01 212128" src="https://github.com/user-attachments/assets/3d541c7a-67d9-4345-ab7e-02a79ac85bce" />

Analisando um pouco já identifico que a senha já está exposta, mas criptografada

<img width="500" height="228" alt="Captura de tela 2025-12-01 212116" src="https://github.com/user-attachments/assets/c07fc9f5-911e-4f63-a9fd-b2f7ddacbea1" />

A forma que o código criptografa minha entrada está na função de return, passando na ordem: Base64, *strrev* que inverte a ordem dos caracteres e por fim hexadecimal. 
Logo depois comparando com a chave $encodedSecret.

Então preciso fazer o processo inverso da função. Primeiro começo decriptando o hexadecimal

<img width="1480" height="862" alt="image" src="https://github.com/user-attachments/assets/c4e32c3b-d6d5-46a5-b741-d4bb04be4b96" />

Estou no caminho certo, já que o formato da senha está no padrão Base64, só que invertido. Dito isso, peço para o chatGPT inverter a ordem dos caracteres

<img width="1003" height="198" alt="image" src="https://github.com/user-attachments/assets/2f888094-b45f-4485-bd08-e136d25e9844" />

b3ViV1lmMmtCcQ==

Depois disso decripto de Base64 para a senha

<img width="1345" height="869" alt="image" src="https://github.com/user-attachments/assets/cd812e9f-d512-42cf-ae4b-4dab24a9bcc0" />

oubWYf2kBq

Então agora é só colocar essa senha na pagina inicial e ganhar a *flag*

<img width="626" height="205" alt="image" src="https://github.com/user-attachments/assets/d092a827-e620-4e77-929d-737be5413cf4" />

<img width="1297" height="385" alt="image" src="https://github.com/user-attachments/assets/18b2ea82-b4da-4004-96c4-2d2afbe287f5" />




**FLAG:** ZE1ck82lmdGIoErlhQgWND6j2Wzz6b6t
