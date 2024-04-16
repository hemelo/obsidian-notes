Breve síntese de todos os parágrafos e notas que sobre termos e conteúdos que não estavam tão claros para mim durante a leitura do livro de Tenebaum

- Tradicionalmente, as redes de trânsito são conhecidas como **<font color="#953734">redes de backbone</font>,** pois têm a função de transportar o tráfego entre duas extremidades.
- A maioria das WANs, a rede contém muitas linhas de transmissão, cada uma conectando um par de roteadores. Dois roteadores que não cornpartilham uma linha de transmissão precisam fazer isso por rneio de outros roteadores.
- Pode haver muitos caminhos na rede conectando dois roteadores. 
- O processo em que o roteador torna a decisão sobre qual caminho usar é charnado de algoritmo de roteamento. Como cada roteador torna a decisão quanto a onde enviar um pacote em seguida é chamado de <font color="#953734">algoritmo de encaminhamento</font>.
- Muitas WANs de fato serão redes interligadas, ou redes compostas, que são criadas a partir de 1nais de urna rede.
- as organizações distribuídas por regiões geográficas e que precisa1n conectar seus locais estão projetando e implantando as chamadas WANs definidas por software (ou SD-WANs), que usam tecnologias diferentes e complementares para conectar diversos locais, inas fornecem um único acordo de nível de serviço, ou SLA (Service-Levei Agreement) por toda a rede. Por exemplo, uma rede pode usar uma combinação de li- nhas alugadas dedicadas e mais caras para conectar vários.
- O dispositivo que faz uma conexão entre duas ou mais redes e oferece a conversão necessária, tanto em termos de hardware quanto de software, é um <font color="#953734">gateway</font>. Os gateways são distinguidos pela camada em que operam na hierarquia de protocolos.

## Arpanet

Vários anos se passaram e o Departamento de Defesa dos Estados Unidos ainda não tinha um sistema melhor de comando e controle. Para entender o que aconteceu e1n seguida, temos de retornar a outubro de 1957, quando a União Soviética derrotou os Estados Unidos na corrida espacial com o lançamento do pri1neiro satélite artificial, o Sputnik. 
Quando tentou descobrir quem tinha "dormido no ponto'', o Presidente Dwight Eisenhower acabou detectando a disputa entre o Exército, a Marinha e a Força Aérea pelo orçamento de pesquisa do Pentágono. Sua resposta imediata foi criar uma <font color="#953734">organização centralizada</font>
<font color="#953734">de pesquisa de defesa, a ARPA, ou Advanced Research Projetcs Agency. </font>A ARPA não tinha cientistas nem laboratórios; de fato, ela não tinha nada além de um escritório e
de um pequeno orçan1ento (para os padrões do Pentágono).
A agência realizava seu trabalho oferecendo concessões eS contratos a universidades e empresas cujas ideias lhe pareciam promissoras.

![[Pasted image 20240415215203.png]]![[Pasted image 20240415215356.png]]

Inicialmente a ARPANET tinha quatro “nós”. Em 1981, já eram mais de 200 computadores conectados à rede, com um novo se juntando a ela a cada 20 dias.

Apesar do crescimento, a ARPANET era apenas “uma” rede. O pulo do gato, que levou à criação da Internet como a conhecemos, foi a conexão dela a outras redes de pesquisa que surgiram mais tarde, como a NSFNet, a NASA Science Network e redes educacionais como 
a Bitnet e CSNET, que conectavam universidades nos EUA.

Para ter algo concreto com que começar, a NSF decidiu construir uma rede de backbone para conectar seus seis centros de supercomputadores. Utilizavam do mesmo hardware da ARPANET. Contudo, a tecnologia de software era diferente: os fuzzballs se comunicavam diretamente com o TCP/IP desde o início, criando assim a primeira WAN TCP/IP.

A rede completa, incluindo o backbone e as redes regionais, foi chamada NSFNET. Ela se conectava à ARPANET por meio de um link entre um IMP e um fuzzball.

Os testes foram mostrando que era necessário que todas estas redes usassem uma “linguagem”, ou protocolo comum. Isso foi resolvido a partir de 1974 com a criação do Transmission Control Program (TCP). Junto com o protocolo IP ele se tornou o TCP/IP, que é a base para todas as conexões à Internet até hoje. Aliás o documento que detalha o TCP, chamado [RFC 675](https://tools.ietf.org/html/rfc675), contém o primeiro uso registrado da palavra _Internet_, referente à uma conexão entre redes – a rede mundial de computadores.

Para facilitar a transição e garantir que todas as redes regionais pudessem se cornunicar entre si, a NSF contratou quatro diferentes operadoras de redes para estabelecer um ponto de acesso de rede, ou <font color="#953734">NAP (Network Access Point).</font>

## Arquitetura da Internet

![[Pasted image 20240416065924.png]]

- A rede a cabo, às vezes cha1nada de rede híbrida fibra-coaxial, ou <font color="#953734">HFC (Hybrid Fiber-Coaxial)</font>, é uma única infraestrutura integrada que utiliza um transporte baseado em pacotes, chamado <font color="#953734">DOCSIS (Data Over Cable Service Interface Specification),</font> para trans1nitir diversos serviços de dados, incluindo canais de televisão, dados de alta velocidade e voz. 
- O dispositivo na residência é chamado modem a cabo, e o dispositivo no terminal de cabo é chamado <font color="#953734">CMTS (Cable Modem Termination System)</font>. A palavra modem é uma contração de "modulador/demodulador" e refere-se a qualquer dispositivo que faz a conversão entre bits digitais e sinais analógicos.
- Outra opção para a implantação da última milha envolve o uso de fibra óptica até as residências, usando urna tecnologia conhecida como <font color="#953734">FTTH (Fiber to the Home).</font> 
- Para empresas em áreas comerciais, pode fazer sentido alugar uma linha de transmissão dedicada, de alta velocidade, dos escritórios até o ISP nais próximo.
- Chamamos o local em que os pacotes do cliente entram na rede do ISP de ponto de presença, ou <font color="#953734">POP (Point of Presence)</font>
- Se um pacote é destinado para um host servido diretamente pelo ISP, ele é roteado pelo backbone e entregue ao host. Caso contrário, ele deve ser entregue a outro ISP.

![[Pasted image 20240416070542.png]]
- As ISPs conectam suas redes para trocar tráfego nos <font color="#953734">IXPs (Internet eXchange Points).</font>
- Os ISPs conectados são emparelhados (peer). 
- Existem muitos IXPs em cidades do mundo inteiro. 
- As redes de ISP se sobrepõem geograficamente. 
- Um IXP é uma sala cheia de roteadores, pelo menos um por ISP. 
- Uma LAN na sala conecta todos os roteadores, de modo que os pacotes podem ser encaminhados de qualquer backbone ISP para qualquer outro backbone ISP. 
- Os IXPs podem ser instalações grandes e independentes, que competem entre si por negócios

Por convenção, a arquitetura da Internet tem sido vista como uma hierarquia, com os provedores de nível 1 no topo e outras redes mais abaixo, dependendo se são grandes redes regionais ou redes de acesso menores

![[Pasted image 20240416071856.png]]

O ímpeto para essa mudança foi o surgimento de provedores de conteúdo "hipergigantes", incluindo Google, Netflix, Twitch e Amazon, além de CDNs grandes e distribuídas globalmente, corno Akamai, Limelight e Cloudflare. Eles mudaram a arquitetura da Internet mais uma vez. Embora, no passado, esses provedores de conteúdo tivessem que depender de redes de trânsito para entregar conteúdo a ISPs de acesso local, tanto ISPs de acesso quanto provedores de conteúdo se proliferaram e se tornaram tão grandes que muitas vezes se conectam diretan1ente uns aos outros em muitos locais distintos. Às vezes, o caminho comum da Internet será diretamente do seu ISP de acesso ao provedor de conteúdo. Em alguns casos, o provedor de conteúdo até mesmoo hospedará servidores dentro da rede do ISP de acesso.

### Rede Móvel

- <font color="#953734">E-UTRAN (Evolved UMTS Terrestrial Radio Access Network)</font>, que é um nome sofisticado para o protocolo de comunicação por rádio usado pelo ar entre os dispositivo móveis (p. ex ., o telefone celular)
- Estação-base celular, que agora é chamado de eNodeB. 
- <font color="#953734">UMTS (Universal Mobile telecommunications System) </font>é o nome formal da rede de telefonia celular.
- A interface do ar é baseada em <font color="#953734">CDMA (Code Division Multiple Access)</font>
- A estação-base da rede celular forma, com seu controlador, a rede de acesso por rádio. Essa parte é o lado sem fio da rede de telefonia Lnóvel. O nó controlador ou <font color="#953734">RNC (Radio Network Controller)</font> controla como o espectro é utilizado. A estação-base implementa a interface com o ar.
- O restante da rede de telefonia móvel transporta o tráfego para a rede de acesso por rádio. Ela é chan1ada núcleo da rede. Em redes 4G, seu núcleo passou a ser comutado por pacotes, e agora é chamado de <font color="#953734">EPC (Evolved Packet Core).</font>
- o 4G EPC completou a transição para uma rede de núcleo totahnente comutada por pacotes. O sistema 5G também é totalmente digital.
- Para transportar dados, os nós do núcleo da rede UMTS se conectam diretamente a uma rede de comutação de pacotes. O <font color="#953734">S-GW (Serving Network Gateway)</font> e o <font color="#953734">P-GW (Packet Data Network Gateway) </font>entregam pacotes de dados de e para smartphones e se conectama redes externas de pacotes, como a Internet.

![[Pasted image 20240416072424.png]]

- Outra diferença entre redes de telefonia móvel e a Internet tradicional é a mobilidade. Quando um usuário sai do alcance de uma estação-base celular e entra no alcance de outra, o fluxo de dados deve ser redirecionado da estação-base antiga para a nova. Essa técnica é conhecida como transferência <span style="background:#ff4d4f">(handover ou handoft)</span>
- Ou o dispositivo móvel ou a estação-base podem solicitar uma transferência quando a qualidade do sinal cai. Em algumas redes de celular, normalmente nas baseadas na tecnologia CDMA, é possível conectar-se à nova estação-base antes de se desconectar da estação antiga. Isso melhora a qualidade da conexão para o smartphone, pois não existe interrupção no serviço - o aparelho fica conectado a duas estações-base por um pequeno período. Esse modo de fazer uma transferência é chamado de <span style="background:#ff4d4f">soft handover.</span>

>[!INFO]
>*Como encontrar um aparelho móvel em primeiro lugar quando existe urna chamada?*
>
>Cada rede de telefonia móvel tem um <font color="#953734">HSS (Home Subscriber Server) </font>no núcleo da rede, que sabe o local de cada assinante, bem cotno outras informações de perfil usadas para autenticação e autorização. Desse modo, cada aparelho poderá ser encontrado contatando o HSS.
>
>O chip é chamado informalmente de cartão SIM, abreviação de <font color="#953734">Subscriber ldentity Module </font>(módulo de identificação do assinante).
>
>Para reduzir a chance de fraudes, as informações nos cartões SIM também são usadas pela rede de telefonia móvel para autenticar os assinantes e verificar se eles têm permissão para usar a rede. Com UMTS, o aparelho móvel também usa as informações no cartão SIM para verificar se está falando co1n uma rede legítima.
>
>Outra consideração iinportante é a privacidade. Os sinais sem fio são transn1itidos para todos os receptores vizinhos, de modo que, para dificultar a escuta das conversas, chaves criptográficas no cartão SIM são usadas para encriptar as trans1nissões. Essa técnica oferece un1a priva- cidade muito melhor do que os sistemas 1G, que eram facilmente interceptados, mas não resolve todos os problemas, em virtude das deficiências nos esquemas de encriptação.




















