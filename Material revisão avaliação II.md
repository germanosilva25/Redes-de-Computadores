# Apostila de Redes de Computadores – Conteúdo da Avaliação II

1. Modelo OSI e Funcionamento dos Pacotes na Rede

1.1 Comunicação em rede e hops

Em uma rede de computadores, os dados enviados de um dispositivo para outro não viajam diretamente até o destino. Eles passam por diversos **nós intermediários**, como switches e roteadores. Cada passagem por um nó é chamada de **hop**.

O nó intermediário analisa o pacote para decidir a rota correta. Contudo, ele **não processa todas as camadas** do modelo OSI.

1.2 Processamento de camadas em cada nó

* **Switches** trabalham na **Camada 2 (Enlace)**.
* **Roteadores** trabalham na **Camada 3 (Rede)**.

Isso significa que o pacote **não sobe até a camada 7** em cada nó. Ele sobe **apenas até a camada necessária para encaminhamento**, geralmente a **camada 3**.

1.3 A camada onde se inicia uma requisição HTTP

Requisições HTTP começam na **Camada 7 – Aplicação**, que é onde os softwares interagem com os protocolos de rede.

Mesmo que os dados acabem sendo transmitidos fisicamente pela Camada 1, o processo lógico começa na camada mais alta.

---

2. Conceitos de Cliente e Servidor

Um único computador pode atuar tanto como **cliente** quanto como **servidor**. Por exemplo:

* Cliente: ao solicitar uma página web.
* Servidor: ao compartilhar arquivos para outros dispositivos.

Isso mostra que o papel do dispositivo depende do serviço realizado, e **não há limitação** que impeça um nó de ser ambos simultaneamente.

---

3. Camada 7: A Camada Mais Próxima do Usuário

A **Camada 7 (Aplicação)** é considerada a mais próxima do usuário, pois nela operam protocolos como:

* HTTP
* HTTPS
* DNS
* FTP

É nessa camada que os softwares utilizam os serviços de rede.

---

4. Endereços Lógicos e Físicos

4.1 Endereço Lógico (IP)

* Pode mudar dependendo da rede.
* Identifica dispositivos em redes **diferentes**.
* Utilizado por roteadores para encaminhar pacotes.

4.2 Endereço Físico (MAC)

* Gravado de fábrica na placa de rede.
* Praticamente único no mundo.
* Utilizado **dentro da rede local**.

Switches usam MAC para decidir para qual porta enviar quadros.

---

5. Conceitos de VPN

5.1 O que é uma VPN

Uma VPN é uma tecnologia que cria um **túnel criptografado** entre o dispositivo e a internet, protegendo:

* Dados transmitidos
* Privacidade do usuário
* Localização e identidade digital

5.2 Como funciona

O tráfego passa por um servidor remoto da VPN. Isso:

* Oculta o IP real
* Impede espionagem
* Protege em redes públicas (cafés, aeroportos, hotéis)

5.3 Uso corporativo

Empresas utilizam VPN para permitir acesso seguro aos sistemas internos.

5.4 VPN e liberdade de acesso

VPN pode contornar:

* Censura digital
* Bloqueios geográficos

5.5 VPN em sistemas de biometria condominial

No contexto de biometria facial:

* Evita expor o módulo local na internet pública.
* Garante comunicação criptografada entre módulo e servidor.
* Atende à LGPD.

---

6. Protocolos TCP e UDP

6.1 TCP

* Confiável
* Garante entrega
* Ordena pacotes
* Retransmite quando há perda
* Usa o processo **three-way handshake**

6.2 UDP

* Sem conexão
* Mais rápido
* Usado em transmissões ao vivo
* Não garante entrega
* Não faz three-way handshake

6.3 Uso simultâneo

Sistemas podem usar TCP e UDP ao mesmo tempo, conforme a necessidade.

Exemplo: jogos online.

* TCP: login
* UDP: posição do jogador

---

7. Tráfego Dentro da Mesma Rede

Quando dois dispositivos estão:

* Na mesma sub-rede
* Conectados ao mesmo switch

Os pacotes **não** passam pelo roteador. Eles percorrem apenas o switch.

O roteador só é utilizado quando há comunicação entre redes **diferentes**.

---

8. Requisições e a Posição da Camada 3

Se uma requisição começa na Camada 7 e desce até a 1, então:

* Camada 3 é realmente a **quinta** camada de cima para baixo.

Isso ajuda estudantes a memorizar a ordem das camadas.

---

9. Endereço MAC: Quase Único

Cada placa de rede possui um endereço físico (MAC) praticamente único.
A chance de dois dispositivos possuírem o mesmo MAC é extremamente baixa, pois:

* Fabricantes recebem faixas exclusivas
* MAC possui 48 bits

Esse identificador é essencial para comunicação na rede local.



