
## Conceitos

### Design Thinking

>Foco no Cliente

- Estética + Usabilidade
- Conhecer o usuário
- Descobrir oportunidades
- Levantar ideias
- Protótipos
- Testes
- Implementação

![[Pasted image 20230207221419.png]]

### Lean UX

- Trabalhar com MVP
- Ser ágil na criação de protótipos
- Validação com usuários
- Definir e acompanhar métricas

### Agile UX

- Time 
- Priorizar o produto
- Foco no usuário
- Flexibilidade

![[Pasted image 20230207221719.png]]

### Product Design Sprint

1. Antes de iniciar

Definir qual a dor que precisa ser resolvida, qual é o desafio e qual será o time que vai participar desse processo.

2. Dia 1

- Levantamento de dados 
	- Qual é o desafio?
	- Por que ele existe?
	- O que o time sabe sobre isso?
	- Qual será, de fato, o ponto a ser atacado para a solução deste problema?
	- O que os usuários dizem sobre isso?

3. Dia 2

- Foco na solução
	- Quais são as hipóteses e as ideias?
- Filtragem de ideias
- Separar usuários para teste em um dia próximo

4. Dia 3

- Extração de soluções
- Base sólida para a criação do protótipo até o fim do dia

5. Dia 4

- Criar protótipo navegável
- Criar roteiro de testes para os usuários
	- Quais tarefas eles devem cumprir?
	- Quais dúvidas precisam responder?

6. Dia 5

- Validação
- Como os usuários estão usando o protótipo

# Usabilidade e Arquitetetura da Info.

1) **Aprendizagem:** seus usuários conseguem cumprir tarefas básicas no seu site logo na primeira vez que eles acessam?
   
2) **Eficiência:**  agora  que  eles  já  aprenderam  a  usar  seu  produto,  eles conseguem fazer isso com rapidez?
   
3) **Memorabilidade:** eles conseguem se lembrar como devemusar o seu site ou app depois de passar algum tempo sem acessar?
   
4) **Prevenção de erros:** a usabilidadedo seu produto é tão boa que evita que seus  usuários  comentamerros  ou,  pelo  menos,  ajuda-os  a desfazer um  erro facilmente?
5) **Satisfação:** é gostoso acessar seu site? Seu usuário se sente feliz porque conseguefazer tudo aquilo que ele precisa?

>[!INFO] Exemplo de Usabilidade: Uma balança
>Um dia eu resolvicomeçar aquela dieta que já tinha prometidofazerháuns 5 anos. Daí,na segunda-feira,comisó alface e caminheina esteira por 15 minutos (mas parecia bem mais, porque na esteira o tempo é diferente). Bem, como foi um grande sacrifício  isso  tudo, eu  acheique  na  terça-feira  de  manhã  já  teria  perdido  alguns quilinhos. Então pegueiaquelabalançasimplesdo banheiro e....subi...só isso! Ela me mostrou  o  resultado  da  minha segunda-feira  de  dieta  e  exercícios  rígidos.Legal!
>- A aprendizagem foi tranquila? 
Demais!
>- Eu consigo fazer  isso  com  eficiência?  
>Muita!Subir  na  balança  virou  minhaespecialidade.
>
>- Eu  memorizei como  faz  para  repetir  daqui  uma  semana  (ou  um  dia)?
>Claro!Assunto dominado.
>
>- Tive  alguma  dificuldade  ou  cometi  algumerro  na  hora  de  subir  na  balança? Fiqueicom alguma dúvida de como faziapara descobrir meupeso? 
>Que nada! Foi de primeira.
>- Fiqueisatisfeita? Digo, com o fato de conseguir ver meu peso...não com o peso de fato? 
>É, fiquei meio chateada porque não perdi os 2kg que queria, mas pelo menos consegui ver o resultado ☺

# Heurísticas de Nielsen

## Mantenha o status visível

Você precisa informar seu usuário sobre o que está acontecendo, dizer para onde ele está indo, como está indoou o que vem depois.

- Passos 
	- Preenchimento de formulários
- Spinners
	- Loadings

>[!INFO] Só toma cuidado pra não dar erro no final do loading após fazer o usuário esperar

## Tenha proximidade com o mundo real

>[!INFO] O caso Netflix
>Quando é acessado o site da Netflix, ele sabe que já estive lá e dá "Boas vindas de volta" e quando se cadastra ele diz "Escolha o melhor plano pra você. Troque de plano quando quiser."

## Exerça o controle, sem tirar a liberdade

É importante que você direcione o usuário para ajudá-lo a cumprir com sua tarefa, mas sem tirar dele as opções de fazer o que quiser em seu site (desde que não haja problema comafuncionalidade ou regras do negócio).

>[!INFO] Sites de desapego
> Eu  posso  criar  um  anúncio e,  quando  eu  quiser,  posso apagar esse anúncio. Mas eu não posso mudar as fotos dele. Isso porque não seria legal anunciar uma coisa, depois alteraras fotos para outro produto e dizer que alguém comprou o que viuno site. O comprador poderia ser enganado

## Manter os padrões consistentes

Os botões CTA (*Call to Action*) devem ter o mesmo padrão

>[!INFO] Instagram
>O  Instagram  mantém  seus  botões  de  interação  com  a  publicação sempre abaixo do post, alinhado à esquerda. Já ou outros botões que chamam para ações como “comprar”, “seguir” ou “entrar em contato”, também seguem um padrão entre si de cor e tipografia

>[!IMPORTANT] Mobile
> Quando falamos de aplicativos, querer reinventar a roda não é  uma  grande  ideia. Os  usuários  de  Android  e  de  iPhone  já têm um  conhecimento prévio  dos  padrões  adotados  pelo  sistema.  É  muito  complicado  querer  inventar  a usabilidade do seu app. Dificilmente você terá sucesso, exceto se o seu serviço for algo muito, mas muito inovador!

## Trabalhe na prevenção de erros

É preciso  entender  onde  e  como  seu usuário pode errar para, então, evitar que isso aconteça. O ideal é que seja tudo tão perfeito, que ele nem cometa erros de percurso dentro do seu site ou aplicativo

>[!INFO] Google
>Quando estou no Google e quero fazer uma busca, ele me ajuda a não  errar em  dois  momentos:primeiro,quando  dá  sugestões  de  palavras  ou expressões enquanto digito;e a segunda quando ele corrige uma palavra que digitei errado

>[!HELP] Máscaras em formulários
>Se  preencho  um  cadastro  que  os  campos já  tenham  máscaras predefinidas e, de quebra, ainda exibe só o que preciso do teclado, é bem provável que eu faça isso mais rápido, com poucas chances de cometer algum erro que torne essa tarefa ainda mais chata e demorada

## Criar reconhecimento

Seu  usuário  nem  sempre  vai  decorar  o  caminho que ele fez para chegar a um determinado produto ou página de interesse. Então, é sua obrigação deixar bem visível esse passo a passo, para que ele navegue e refaçaseu caminho sem problemas, quando quiser

>[!INFO] Utilização de Breadcrumbs
>Quem faz isso muito bem é a Amazon Shipping. No site ou aplicativo tem o histórico de últimos produtos acessados.
>Na AliExpress o campo de pesquisa já vem automaticamente preenchido com a última coisa que analisou pra comprar

## Flexibilidade e eficiência de uso

Você deve se lembrar que o seu site pode ser acessado por pessoas com perfis diferentes. Por mais que o seu produto tenha um público definido, dentre eles podem existir pessoas mais ou menos experientes no uso desites eaplicativos. Pensando nisso, a usabilidade deve ser boa para qualquer pessoa que resolver acessar seu produto.

>[!INFO] Arquivar um email
>No  Gmail  eu tenho duas  formas  de  arquivar uma  mensagem.  Uma delas é  por  meio  de  um  atalho,  movendo  o  card  da  mensagem  para  esquerda. Provavelmente, essa opção é mais usada por pessoas mais experientes e habituadas com esse tipo de comportamento. A outra maneira é entrar na mensagem e escolher a opção de “arquivar”, no topo da tela. Essa deve ser a opção de pessoas menos experientes no uso de sites ou apps

## Design Minimalista

As telas do seu produto precisam ser simples e conter somente o que o usuário realmente precisa saber ou fazer. 

>[!IMPORTANT]
>Quanto mais informação desnecessária, maiores são as chances das pessoas se perderem e não conseguirem cumprir com o objetivo delas

## Diagnóstico de erros

Mesmo com todo o cuidado, seu usuário pode encontrar obstáculos para cumprir sua tarefa usando seu produto. Então,é importante que as mensagens de erro sejam claras, de maneira  que as pessoas consigam consertar rapidamente o erro cometidoe, assim, seguir adiante

>[!SUCCESS] Exibição de erros em formulários
>Exibir alerta de senha inválida

>[!DANGER]
É muito comum apps e sites exibirem mensagens técnicas como "erro na conexão com banco de dados" ou "serviço indisponível”. Isso não é legal. 
O usuário não entende e ainda pensa que osite é cheio de  erros.  O  ideal  é deixar  uma  linguagem simples  e,  sempre  que  possível,  alguma  instrução  para  o usuário. Dependendo do erro, da situação e da importância daquela tarefa, você pode surpreender e deixar uma opção para seu usuário acessar o atendimento ao cliente

## Documentação e ajuda

O ideal é que tudo em seu site ou aplicativo possa ser feito de forma bem intuitiva, mas em alguns casos é preciso oferecer informação ou ajuda para seus usuários. Isso amenizará qualquer impacto que uma dúvida possa ter quando ele pretende concluir alguma tarefa

## Síntese

Se o seu site for difícil de usar, difícil de ler, se o usuário tiver  dificuldade  para  encontrar  o  que  ele  precisa  ou  não  conseguir  atingir  o seu objetivo, ele simplesmente sairáe não voltará mais. Existem  muitos  sites  de  produtos  e serviços, e se o usuário não conseguir usar o seu, certamente irápara outro. E muito provavelmente isso já aconteceu com você, não é?

---
# Arquitetura da Informação

- Identificação e definição do conteúdo e funcionalidades do site
- Organização, estrutura e nomenclatura do conteúdo

>[!HELP] Quando  você  desenha  o  mapa  de  um  site,  por  exemplo,  você  está definindo como seu conteúdo vai ser agrupado e apresentado para seu usuário

- **Inventário de conteúdo**

Momento  de  levantar  e  identificar  todo  o conteúdo existente no seu site

- **Auditoria de conteúdo**

O conteúdo deve ser avaliado para saber o quanto ele é útil, qualéo seu tom de voz e se deve mesmo entrar no site

- **Agrupamento de informações**

De  forma  bastante  coerente  e  lógica, essa é a hora de agrupar o conteúdo por temas similares ou relação entre si

- **Taxonomia**

É  a  nomenclatura  que  você  dá  para  os  agrupamentos  que você crioue deve contemplar todo o conteúdo do site

- **Informações descritivas**

É  quando  você  define  metadados  úteis  que poderão ser usados para gerar listas de "conteúdo relacionado" ou outros componentes de navegação que vão auxiliar os usuários a encontrar o que eles precisam

#### Caso Americanas

>[!INFO] Categorização de produtos

![[Pasted image 20230207183528.png]]

## Identificando problemas

- Baixo tráfego em determinada categoria
- Conversão baixa
- Altas taxas de rejeição
- Baixo número de entradas
- Alto volume de pesquisas

## Melhorando UX

- Equipe Multidisciplinar
- Entender usuários
- Seguir boas práticas de design
- Não reinventar a roda
- Não encher linguiça
- Fazer testes

# Para quem você está criando sua UX?

- Você não é seu usuário
- Se insistir em fazer o que ACHA que é bom para o seu usuário, estará correndo o risco de errar feio

## Por que precisa conhecer o seu usuário?

- Será mais fácil aprimorar o desenvolvimento do produto
- Vai melhorando o conteúdo
- Vai descobrir quem são os melhores clientes
- Vai ver impacto nos resultados

### A diferença entre público-alvo e persona

>[!INFO] Público Alvo
>Definição ampla do público qwue se interessa pelo seu produto. Não se refere a algúem específico. Não aborda os hábitos do usuário

>[!SUCCESS] Persona
>Definição de cliente real, de forma mais humanizada. Faz referência a uma personagem específica. Aboreda detalhes dos seus hábitos ou comportamento

A persona tem detalhes mais ricos que podem facilitar a comunicação daquilo que é mais relevante para seus usuários, daquilo que eles realmente precisam saber ou fazer para atingir seus objetivos.

>[!HELP]
>Nem todo produto conta com apenas uma persona. É comum ter negócios com mais de uma persona


## Como criar uma persona

- Basear em dados de pessoas reais
- Melhor que seja feito em equipe
- Agrupar por características comuns

### A criação

- Nome
- Idade
- Nível de escolaridade
- Ocupação
- Meios de comunicação
- Objetivos
- Desafios
- Como podemos ajudar
- Foto

### Casos de usos de personas

>O  Tinder  também  fez  mudanças  em  seu  cadastro  depois  de  entender  um pouco melhor o perfil de seus usuários. Ainda não está disponível na versão do app brasileiro,  mas  a  partir  de  agora,os  usuários  poderão  especificar  melhor  sua identidade de gênero.Eles discutiram bastante o fluxo e a comunicação dessa etapa do cadastro para que atendesse à necessidade de todos.A escolha principal continua sendo entre “mulher” e “homem”, mas com a opção de especificar melhor o gênero

>Depois  de  implantar  novos  serviços  como  uberX, uberPOOL,uberBAG, uberBIKE, oUber percebeu que a sua usabilidade estava ficando mais complicada, apesar desses serviços terem entrado para atender às necessidades de seus usuários (como naquela história da balança, lembra? Quanto mais ferramenta, mais difícil pode ser  a  usabilidade).Então  eles  fizeram  uma  revisão  de  arquitetura  e  layout  do  app, buscando uma experiência mais prática e simples. Facilitaram a escolha do tipo de serviço, colocaram mais ícones para melhorar o design e aprimoraram a criaçãode atalhos de acordo com o uso

### Quando devo revisar as personas?

- Mudança no negócio
- Mudança no perfil dos usuários
- Tempo

### No que mais a persona pode contribuir?

- Ajudar na área de marketing
- Melhorar o discurso ou tom de voz da área de comunicação
- Segmentar melhor seus dados para análise de comportamento dos usuários reais

---
# Protótipos e Design

## Design Persuasivo

Design que  tem  a  função  de  fazer  seu  usuário  encontrar  o  que  ele precisa  e  gostar  tanto  de  estar ali,  que  isso  vai  ser  convertido  em  leads,visitas, vendas,  cadastros  e  todas  aquelas  coisas  maravilhosas  que  você  espera  que aconteça.

Se a intenção é motivar e direcionar seus usuários, eles precisam sesentir segurose  a  interface  (o  que  o  usuário  vê) faráesse  papel.  Então, será  preciso consideraros quatro fatores a seguir, na hora de pensar no design do seu produto.

### Qualidade

Não  adianta  inventar coisas e prejudicar a sua usabilidade, como dar nomes exóticos para suas categorias ou  usar  ícones  totalmente  desconhecidos  para  representar  seus  produtos.  

>[!IMPORTANT] Seu usuário precisa saber onde clicar

Quanto mais informação e mais cores na tela = Pior

### Informação, fotos e vídeos atualizados

- Além de o site precisar conter todo o seu portfólio,seusprodutosou serviços devem estar bem explicadose ilustradospara que eles sintam essa confiança. 

- Essa também é uma forma de mostrar que você realmente quer ajudar seus usuários a entender o que está sendo oferecido e, assim, fazer uma boa escolha.

- As fotos ou vídeos precisam ter uma boa qualidade

>[!INFO] 
>O que está no site deve ser constantemente atualizado. Informação e imagens ultrapassadas com certeza sóvão causar dúvidas e descrença.

### Jogo Aberto

Não adianta esconder preço, deixar para exibir o prazo de entrega só no final da compra ou não deixar claro qual é a política de troca. E se puder fazer tudo isso sem exigir dados desnecessários, melhor ainda.

>[!IMPORTANT] Usuário gosta mesmo é de transparência

### Carousel de Opiniões

Tudo bem colocar um carousel com opiniões sobre seu site/negócio. Mas que tal colocar link de ReclameAqui e publicações reais em redes sociais?

## Protótipo

Aplicativo para teste de público-alvo/personas, ou uma representação como:

### Wireframe

Basicamente, um **rascunho**

![[Pasted image 20230207193705.png]]

### Mockup

![[Pasted image 20230207193752.png]]

# Por onde começa o Design

- Defina o conteúdo
- Siga os princípios e padrões de design

>[!INFO]
>No caso de aplicativos, hádiferenças entre os comportamentos comuns para apps Android e iOS. Então cada um deles tem seus patterns que devem ser respeitados para facilitara usabilidade

## Acessibilidade

- Tamanho e estilo de fonte
- Cores e contraste
- Imagens, vídeo e áudio

### Usuário

- Idade
- Habilidade cognitiva
- Audção e visão
- Compreensão da língua e linguagem
- Dispositivo, tecnologia e conexão

## Dispositivo

- Mobile, desktop ou app?

Dá para construir um design para todos, mas sempre levando em consideração onde está a maior quantidade de acessos

### Responsividade

- O site responsivo é uma versão única de site que se adapta aos diferentes tamanhos  de  tela,  seja  desktop,  tablet  ou  celular.

- Conforme  o  dispositivo,  os elementos  da  tela  são  reposicionados  para  facilitar  a  leitura  e  aproveitamento  do espaço

>[!INFO] O Google  gosta  de  sites  responsivos porque  privilegiam  a experiência do usuário

### Site mobile

- O site mobile é uma segunda versão do seu site, feito só para o acesso por celular, ou seja, ele não vai funcionar bem em um desktop. 

- A parte boa de fazer um site mobile é que ele pode ser construído pensando apenas na experiência no celular, o que vai deixar o site muito mais amigável e útil para seus usuários

- A parte ruim dele é que vai exigir mais da atualização e manutenção, por ser uma versão diferente dodesktop

### Aplicativo mobile

Um  app,  geralmente, tem  a  função  de  engajar  o  usuário  e  isso  acontece porque ele oferece uma experiência muitomais rica.

As vantagens de um app é quenele é possível usar ferramentas quepodem torná-lo muito mais personalizado, como GPS, câmera, notificações efunções offline

O  “touch”  também  torna  muito  mais  fácil  o  clique  ou  qualquer  gesto  de navegação e a disponibilidade, o fato de estar sempre perto e fácil de achar favorece muito mais o uso espontâneode um app. 

>[!DANGER] Depende muito do seu produto e do seu público, então analise bem antes de investir
>
>Não é barato ter um app. Isso porque há diferenças de comportamentos e design entre iOS, Android ou Windows Phone, então é preciso personalizar cada um deles, e isso leva tempo e usa recursos do seu time

## Design Mobile

> Motivação: Mundo cada vez mais mobile first

- Targets amplos e óbvios

Se a zona de clique ficar pequena demais ou perto demais uma da outra, seu usuário pode ter problemas para cumprir sua missão e vai desistir muito rápido do que desistiria no desktop

>[!SUCCESS] 1cm x 1cm de área de clique

- Otimização de imagens

Cuidado com pacote de dados

### Fácil de clicar não significa fácil de ver

É sempre bom levar em conta o mapa de calor da visão e dos dedos na sua aplicação/site.

#### Campo de visão

![[Pasted image 20230207202844.png]]



#### Zona do clique

![[Pasted image 20230207202510.png]]

![[Pasted image 20230207202552.png]]

![[Pasted image 20230207202736.png]]

>[!INFO] Lembre-se
>O dedo mais importante é o polegar

### Navegação por barra, menu e ícones

Tudo tem a sua ordem eprecisamos ajudar os usuários a se encontrarem no site  ou  app.  Então,  nesse  sentido,  as  barras  e  menu  de  navegação têm uma importante função.Vamos falar um pouco sobre elas


#### Action Bar

Essa  barra  fica no  topo  da  tela.  Éaquele  lugar  que  dever  ser  bem  fácil  de reconhecer e lembrar como usar. Nela geralmente fica o título do app e botões como “voltar”, “buscar” ou  ainda  o  símbolo  do  “carrinho”  para  um  e-commerce. 
É  bem arriscado querer colocar outros tipos de funções que não sejam comuns a esse lugar, porque as pessoas podem se confundir

#### Tab Bar

É aquela que fica no <font color="#f79646">topo (para Android)</font> ou na <font color="#0070c0">parte inferior da tela (para iOS)</font>. Nela ficam os itens mais importantes para a navegação do usuário, então seusitens devem ser muito bem escolhidos. 

- Os ícones
	- precisam ser comuns à maioria dos apps ou   pelo   menos   similares   aos   de   seus   concorrentes. 
	- devem descrever visualmente a função do botão
	- fazer com que seu usuário vai conseguir identificar mais rapidamente  o  que  significa  cada  um  deles 

>[!IMPORTANT] menos  adivinhação  =  menos  carga cognitiva = desempenho mais rápido do usuário

>[!INFO]
>Sempre que possível, opte por usar ícone e legenda. Ícones sozinhos dificilmente performam melhor que textos.

### Menu e lista de ícones

Se usar ícones dentro de um menu ou lista, deve ser bem contextualizado

Se usar ícones para tudo, tudo ganha destaque. Onde tudo se destaca, nada se destaca

>[!WARNING] Se usar ícones para tudo, tudo ganha destaque. Onde tudo se destaca, nada se destaca

### Ações claras

 - Se o seu layout é bom, ele não precisa de explicação! 
 - Se os ícones precisam ser explicados, refaça ou use textos

![[Pasted image 20230207204218.png]]

Textos são úteis para novos comportamentos ou funcionalidades na aplicação


### Interações

#### Botões
![[Pasted image 20230207204348.png]]
#### Links

![[Pasted image 20230207204446.png]]

#### Slides

![[Pasted image 20230207204548.png]]

>[!IMPORTANT] Indicadores visuais são melhores que númericos em slides

#### Scroll

Sempre deixe algo picotado, para deixar o usuário curioso em saber pelo conteúdo particionado

![[Pasted image 20230207204735.png]]

#### Hierarquia
![[Pasted image 20230207205023.png]]

### Performance

A percepção  de  performance  se  dá  pelo  tempoe representação de carregamento  de  telas,  transições  e  animações

#### Carregamento da página

Vale a  pena  planejar  alguns steps para  mostrar o  carregamento  de  página.

>[!ERROR] Tela branca
>O que  não  é  legal  acontecer  é  ficar  tudo  em  branco, esperando   [[#Mantenha o status visível|carregamento total]], pois isso pode dar a sensação de que o site está lento demais

![[Pasted image 20230207205325.png]]


### Feedback
![[Pasted image 20230207205408.png]]
![[Pasted image 20230207205613.png]]


### Cadastro/Login

![[Pasted image 20230207210803.png]]

### Formulários

Ninguém gosta de preencher formulário. Principalmente no celular!

Alternativas:
- Preenchimento de dados automáticos
- Uso de dropdowns

>[!INFO]
>Evite usar legenda dentro do campo que desaparececom o preenchimento. Isso acaba forçando o usuário a ter que lembrar oquedeve ser digitado naquele campo

![[Pasted image 20230207211110.png]]


### Footer

Não dá pra manter o footer  tradicional do desktop porque ele ocupa muito espaço. Uma opção é escolher alguns itens mais importantes e colocar no menu.

![[Pasted image 20230207211135.png]]

Como pode ver, acaba ocupando muito espaço neste escroll e até briga com as opções da barra inferior

### Campo de pesquisa

![[Pasted image 20230207211423.png]]
![[Pasted image 20230207211434.png]]

Normalmente no topo da tela. É bom que ele exista para que as pessoas possam encontrar o que precisam, em qualquer parte do site ou app

De qualquer forma, ao acessar osite, já é possível mostrar alguns itens, mas é importante que eles tenham alguma relevância para seus usuários

Deixe sempre uma opção ou sugestão de busca para eles

>[!WARNING] Nunca direcione para uma página 404

##### Filtros

Quando seu resultado de busca oferece muita informação, é preciso dar ao usuário a opção de filtrar

Cuidado ao usar filtros representados   apenas   por   ícones,   sem   textos,   porque   precisam ser  muito autoexplicativos 

- Os filtros podem funcionar de duas formas: 
	- o usuário seleciona tudo o que deseja e clica para filtrar, atualizando o resultado da busca
	- o usuário ver o  resultado  mudar  a cada  filtro  acrescentado (talvez uma  opção  mais perigosa,  porque  recarrega  muitas  vezes  a  página  e  pode  parecer  mais  lento). 

Independentemente da opção, deve-se criarum espaço para mostrar os filtros usados para chegar àquele resultado e, assim, permitir alteração,se necessário

### Mapa
![[Pasted image 20230207211821.png]]

>[!TIP] Quando o usuário vê mapa na tela, a sua expectativa é que possa manipular ele

### Notificações

 Funcionam como um aviso para o usuário, incentivando seu engajamento por meio de informações que consideram importantes, como uma nova solicitação de amizade ou um novo conteúdo do seu interesse 
 
 A notificação precisa ser clara e estar o mais perto possível do que se refere
![[Pasted image 20230207212002.png]]

### [[#Heurísticas de Nielsen#Flexibilidade e eficiência de uso|Gestos Ocultos]]

Por exemplo: no WhatsApp há duas formas  de apagar uma conversa. Uma delas é deslizar para a esquerda, em cima da conversa que você quer apagar (esse é o gesto oculto), você consegue clicar em “mais” e em seguida aparece a opção de apagar   ou   limpar   a   conversa. Também   pode   ser   feito dentro   da   conversa, independente de um gesto oculto         

### Legibilidade

- O conteúdo deve ser fácil e rápido de ler
- Os espaços devem ser bem aproveitados
- Foto à esquerda, texto à direita
- Fontes diferentes apenas para títulos e contrastes

---
# Pesquisas e dados

>Motivação: UX não pode ser só feeling, precisa ter base em dados, testes e boas análises de resultado

##### Por que usar pesquisas e dados para melhorar sua UX?

- Eliminar projetos desnecessários
- Diminuir a tomada de decisão baseada em opinião pessoal
- Possibilitar levantamento de hipóteses e testes

## Dados Quantitativos vs Qualitativos

### Análise de dados quantitativos

- Identificação dos problemas

Audiência, cliques, aquisição, comportamento, conversão

- Orientação estratégica

Através dos dados, você pode orientar estrategicamente a evolução do produto. 

Por meio deles, você percebe a necessidade de um projeto ou feature, fica sabendo da jornada do seu usuário, identifica oportunidades, criando personas

- Monitoramento
	- Google Analytics
	- Firebase

Fazer acompanhamento de metas é essencial. Os dados entram aqui, como parte importante da análise ep para identificação de necessidades e resultados 

>[!WARNING] Importante ressaltar que os números sozinhos não dizem nada

### Análise de dados qualitativos

Demandam tempo porque dependem de uma interação direta com usuário

- Testes de usabilidade
	- Devem ter como orientação um <font color="#0070c0">problema</font>
	- Levantamento de <font color="#f79646">hipóteses</font>
	- Realização de <font color="#c0504d">experimentos</font>
	- <font color="#938953">Meta</font>

Exemplo: <font color="#0070c0">Os usuários se frustram porque querem ver os preços dos serviços no site e essa informação não está disponível lá.</font> <font color="#f79646">Talvez os usuários não se freustrem se houver uma explicação sobre a complexidade de deixar o preço no site, já que o serviço oferecido é personalizado.</font> <font color="#c0504d">Colocar essa informação sobre a personalização na página, em lugar dos preços pode salvar.</font> <font color="#938953">E com isso, pretende-se aumentar o número de leads, fazendo com que mais pessoas enviem formulário com dados de contato ou entrem em contato com um representante de chat.</font>

- Pesquisas
	- de satisfação
	- de intenção
	- de feedback

>[!SUCCESS] É uma boa maneira ter um canal de comunicação em aberto, utilizando sua base de emails para disparar as pesquisas

- Focus Group

Reunião de usuários para discussão bem definida

### O que fazer com esses dados?

- Desenvolver soluções para melhorar seus resultados
- Encontrei mais de uma solução
	- Teste comparativo em ambiente de produção (pessoas reais)
		- Não se frustrar caso dê errado

>[!HELP] Até onde testar?
>Desde a cor de um botão até o layout inteiro é preciso testar caso necessário

- Estabelecimento de metas
	- [[Gestão de Qualidade#Indicadores de Desempenho|Indicadores]]


---

# Ferramentas

## Por que trackear e identificar usuários?

> Para ter alguns UX insights

- Quantos devices os nossos usuários costumam usar para acesar nosso conteúdo?
- Eles estão completando tarefas com devices diferentes?
- Qual conteúdo fideliza mais nossos usuários e aumenta a frequência deles no site ou seu tempo médio?
- Quais ações dos usuários os levam para o final de seu funil de conversão?
- Eventos
	- Downloads
	- Play e pause
	- Clicks em 
		- banners de publicidade
		- categorias e tags
		- artigos relacionados
		- detalhes do produto


> Usando o tracking

- Se muitas pessoas começam a ver o vídeo, mas não terminam de assistir. Isso significa que o vídeo precisa ser melhorado e tornar mais atraente para os usuários
- Se a maioria nem começa a ver o vídeo, isso significa que você precisa rever se ele está no lugar certo, se está chamativo, se tem o devido destaque e se aquele momento é o melhor pra exibí-lo

### Formas

| Método  | +        | -                            |
| ------- | -------- | ---------------------------- |
| Cookie  | Fácil    | Atrelado a um navegador e IP |
| User ID | Não muda | Cadastro                     |
| Email   | Fácil    | Pode mudar                   | 

## SEO

s ferramentas  de  tráfego  e  SEOte  ajudam  a  entender  o  que  seus usuários  estão  buscando  e,  com  isso,  você consegue adequar  e  criar  novos conteúdos   que   possam   atrair   mais   audiência   orgânica   para   seu   site.   Essas ferramentas  sugerem  palavras  amplas  e long  tailse,  junto  com  elas,  uma  ideia  de quantidade  de  buscas  mensais  e  uma  escala  de  dificuldade  para  posicionamentonas  buscas  do  Google.Elas  também  dão informações  relacionadas a backlinks e tudo que possa contribuir com ações de SEO.

## Web Analytics e In-Page Analytics

- Medição de tráfego e sua origem
- Acompanhamento de interações
- Customização de dados
- Análise de histórico

![[Pasted image 20230207224528.png]]
![[Pasted image 20230207224542.png]]