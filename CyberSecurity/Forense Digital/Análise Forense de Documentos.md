#### Técnicas de Manipulação de Fotografias

- *Splicing*
- *Feather edges*
- *Light Maching*
- *Sharpening*
- Geração em computador
- *Cloning*
- *Healing and Retouching*
- Esteganografia
- *Lazy Snapping*
	- Recorte grosseiro (preguiçoso)
- *Paint Selection*
	- Recorte trabalhado
- *Poison Matting*
	- *Alpha Matting*
	- Equações de Poisson
	- Algoritmoss de filtragem para ajuste fino
- Propagação estrutural
	- *Image completion*
	- Problema de otimização em relação a restrições estruturais de consistência
	- Preenchimento de regiões com técnicas de síntese de textura
- Seleção de objetos por cortes em grafos
	- Super-segmentação
	- Marcações do usuário
	- Casamento em grafos (Homomorfismo)
	- Refinamento (Filtros conexos, MM)

##### Questões Importantes

- Essa imagem é original ou foi criada com composição?
- Essa imagem representa um momento real ou foi digitalmente modificada para enganar o visualizador?
- Quais partes dessa imagem sofreram modificações?
- Quais partes dessa imagem sofreram qualquer tipo de processamento?
- Qual a extensão do processamento?
- Câmera de qual fabricante?

##### Esforços de Pesquisa

- Atribuição de Fontes
- Identificação de Geração por computador
- Autenticação
- Detecção de Falsificações
- Detecção de Mensagens Escondidas

##### Atribuição de Modelo

- Característica das lentes
	- Exposição, foco, estabilização
- Tipo e tamanho dos sensores
	- CCD, CMOS...
- Tipo de filtro de mosaico
	- CFA...
- Informações dos algoritmos da DIP
	- Demomosaico
	- Correções
	- Realce
	- Correção de abertura e gamma
	- Compressão

###### Análise de Artefatos CFA

- Hipótese
	- Linhas e colunas de imagens interpoladas provavelmente possuem correlações com seus vizinhos
	- Relações de vizinhança pode ser fornecida por *kernels* de tamanhos específicos

![[Pasted image 20230520044233.png]]

- Dois estágios
	- Da esperança -> estima-se a probabilidade de cada amostra pertencer a um modelo particular
	- Da maximização -> forma específica das correlações entre as amostras

- Podemos assumir que cada amostra pertence a um de dois modelos possíveis
- Se a amostra é lienarmente correlacionada com seus vizinhos ela pertence ao Modelo I, caso contrário, ao modelo II

![[Pasted image 20230520044606.png]]

- Análise de Artefatos CFA
	- Cem imagens com interpolação CFA
	- Algoritmos
		- Bilinear
		- Bicubic
		- Smooth hue
		- Median (5 x 5)
		- Gradient
		- Adaptive Color Plane
		- Variable Gradiants


##### Atribuição da Câmera em específico

- Atribuição direta
	- Características únicas da câmera em análise
		- Imperfeições dos componentes
		- Defeitos e falhas decorrentes do ambiente e condições de operação
		- *Dead* e *cold pixels*, *pixel traps*

- Padrão de Ruído
	- Fixo (FPN)
		- Aditivo e decorrente de *dark-currents*
		- Dependente do tempo de exposição e temperatura
		- Pode ser removido *in-camera* extraindo-se um quadro preto
	- Foto-responsividade não uniforme (PRNU)
		- Defeitos de baixa frequência
			- Causados pelos efeitos da refração da luz nas partículas devido a configurações de zoom e superfície ótica
		- Não uniformidade de pixels
		- Multiplicativo
		- Definido como a sensitividade que diferentes pixels têm em relação a luz
		- Inconsistências na fabricação do sensor da captura

> O ruído PNU não possui padrão de referência, é necessário estabelecer uma aproximação com fórmula 
> 
> No processo de aproximação é feito a média de K imagens de uma cena uniforme como o céu, através da média é possível determinar se uma imagem pertence a câmera calculando a correção entre o ruído residual da imagem e o padrão de referência

>[!DANGER] Dificuldades
>
>- Sincronização (modificações de escala e recorte)
>- Força bruta para achar as transformações

##### Atribuição de Scanner

- O processo de fabricação de qualquer dispositivo eletrônico de captura introduz defeitos nos sensores de imageamento

>[!INFO]  Aquisição via Scanner
>
>Fonte de Luz -> Documento Original -> Lentes, Espelhos e Sensores de Imageamento -> Amplificador, ADC -> Software de Pós-Processamento, Correção de Cores, Gamma -> Imagem Digital

- Scanners possuem
	- Resolução horizontal (sensor) e vertical (motor de passo)
	- Motor de passo
	- Estabilizador
- Como os scanners fazem escaneamentos em resolução não-nativa
	- Sub-amostragem
	- Amostragem normal seguida de ajustes in-scanner

- Padrão de Ruído
	- Construção do padrão de referência
	- Média das linhas (devido ao motor de passo)
	- Média de múltiplas imagens
	- Análise de correlação
	- Filtro de supressão/redução de ruído
	- Mesmo esquema/lógica de cálculo da câmera

>[!DANGER]
>
>- Scanners usam parcialmente a superfície de captura
>- Essa abordagem requer condições similares de captura para funcionar

>[!SUCCESS] Dica
>
>Estatísticas de ordem sobre as novas características (média, variância, moda, curtose, etc)

##### Abordagens Contra-Forenses

- Estimular ruído fixo FPN -> Imagems de um quadro preto
- Estimular ruído PRNU -> K imagens de uma cena homogênea subtraindo-se o a estimativa FPN
- Estimativa de *Flatfielding*

>[!INFO] Flatfielding
>
>Após obter a série de imagens de campo plano, é possível calcular a média ou o valor mediano dessas imagens para criar o campo plano de referência. Em seguida, a imagem original é dividida pelo campo plano para corrigir as variações de iluminação. Essa divisão pode ser feita pixel a pixel ou por meio de manipulação de matrizes.
>
>Ao aplicar a correção de campo plano, é possível eliminar gradientes de iluminação, manchas, vinhetas e outros artefatos que podem afetar a qualidade e a precisão das imagens. Isso resulta em uma imagem mais uniforme e com uma representação mais precisa das características originais da cena ou do objeto fotografado.

- Substituição do padrão de ruído -> *Flatfielding* inverso

##### Identificação de Criações Sintéticas

###### Decomposição multi-escala e análise estatística

- Imagens naturais possuem regularidades detectáveis com estatísticas de alta ordem
- O processo de criação de uma imagem em computador insere artefatos estatísticos nas imagens produzidas
- Funcionamento
	- Decomposição QMF da imagem em múltiplas escalas/resoluções
	- Análsie estática em duas fases
		- Análise direta
			- Média
			- Variância
			- Moda
			- Curtose
		- Predição linear dos erros de magnitude
			- Estimar possíveis correlações entre um pixel e seus vizinhos multi-escala

###### Diferenças físicas nos processos de captura e geração

- Autenticidade em nível de processamento (imagens capturadas por algum sensor)
- Autenticidade em nível de cena (*snapshot* de um campo de luz)
- **Dimensão fractal** local para capturar a complexidade de texturas
- **Vetores de patches** locais para capturar propriedades de arestas
- **Superfície gradiente** para capturar a forma de resposta de uma câmera
- **Geometria quadrática local** para capturar propriedades poligonais dos objetos computadorizados

#### Imagem

- Necessário estabelecer um **universo matemático** no qual seja possível definior diversos modelos abstratos de Imagem
- Em seguida, definir um **universo de representação** onde procuramos esquemas que permitam uam representação discreta desses modelos
- **Codificar a imagem no computador**

- A imagem contínua (não discreta) pode ser definida como: `I: U -> C` onde `U c R³` é uma superfície e `C` é um espaço vetorial
- Na maioria das aplicações, `U` é um subconjunto plano e `C` é um espaço de cor
- Termos
	- `I` -> função imagem
	- `U` -> suporte da imagem
	- Conjunto de valores de `I` que é um subconjunto de `C` -> valores da imagem
- Se `C` possui espaço de cor de dimensão I, a imagem é monocromática
- Representação mais comum de uma imagem espacial: subconjunto discreto `U' -> U` do domínio da imagem, um espaço de cor `C` associado a um dispositivo gráfico e representar a imagem pela amostragem `I -> U'`
- Cada ponto (x,y) do subconjunto `U'` -> pixel

>[!INFO] Quantização
>Processo de discretização onde a função imagem `I` toma valores em um subconjunto discreto do espaço de cor `C`, durante a representação em computador
>Caso mais comum: Consiste em tomar o domínio como sendo um retângulo e discretizar esse retângulo usando os pontos de um reticulado bidimensional. Acarretando em representação matricial:
>
>A<sup>(mXn)</sup> = (a<sub>ij</sub> = (I(x<sub>i</sub>, y<sub>j</sub>)))
>Dessa forma, cada ponto a<sub>ij</sub> é um vetor do espaço de cor representando a cor do pixel na coordenada (i, j) da imagem

- Cada ponto possui 3 valores associados, sendo cada um 8 bits, então cada pixel é 3x8=24 bits=3bytes, então ela é uma imagem de 24bits
	- Ela pode ter o canal de transparência, o mesmo adiciona um byte a mais de informação em cada pixel, a imagem nesse caso é de 32bits

![[Pasted image 20230520140256.png]]

##### Espaços de cor

###### RGB

- Red, Green, Blue
- Reprodução de cores em dispositivos eletrônicos
![[Pasted image 20230520140521.png]]

###### CMYK 

- Ciano, Magenta, Yellow, Black
- Modelo de cores subtrativas
- Contraposipção ao RGB
- Apropriado para impressoras

![[Pasted image 20230520140617.png]]
###### HSV 

- Hue, Saturation, Bright
- Matiz (tonalidade) -> Tipo de cor
- Saturação (pureza) -> Mais alto = Mais próximo da cor pura
- Brilho (intensidade)

##### Operações com imagens

- Warping

![[Pasted image 20230520141452.png]]

- Transformação de atributos

![[Pasted image 20230520141516.png]]

- Decomposição em canais de cores
	- Quando separamos a imagem em suas cores báscias representadas no espaço de cores `C' ∈ C` 
	- Decomposição Wavelet
	![[Pasted image 20230520141822.png]]
- Decomposição em planos de bits
	- Após a decomposição da imagem de 24 bits em seus 3 canais, ainda é possível decompor em planos de bits
	- Cada canal de cor possui 8 bits e possui 8 planos de bits por canal de cor

#### Aprendizado de Máquina

- Extração de informações e extrapolação do conhecimento a partir de dados
- Classificador -> mapeamento a partir de um espaço de características X para um conjunto discreto de rótulos Y
	- Em IA, um classificador de padrões é um tipo de motor de inferência que implementa estratégias eficientes para computar relações entre um conceito e um conjunto de instâncias
	- Classificadores podem ser:
		- Supervisionados
		- Semi-Supervisionados
		- Não-Supervisionados

- Modelagem de problemas
	- Problemas são descritos por variáveis
		- Reais
		- Categóricas
	- Como trainsitar entre os dois tipos?
	- É possível converter uma representação em outra?
	- Simplicidade vs Complexidade
	- O que é realmente importante?
	- Precisamos realmente de todos os dados possíveis para tomar uma decisão?
	- Maldição da Dimensionalidade -> Dimensão do vetor de caracterísitcas tem efeitos colaterais importantes:
		- Distâncias médicas ficam grandes
		- Dados ficam esparsos
	

###### Aprendizado supervisionado

- Consiste em técnicas em que procuramos estimar uma função de classificação `f` a partir de um conjunto de treinamento que consiste em pares de entrada X e saídas Y
- O número de variáveis que constituem cada uma das entradas em X é p -> X tem n observações, chamados de vetores de características
- Cada vetor de entrada é composto por p graus de liberdade (dimensões ou variáveis)
- A saída da função `f` pode ser um valor contínuo (regressão) ou pode predizer a etiqueta de um objeto de entrada (classificação)

>[!INFO]
>A tarefa do aprendizado é predizer o valor da função para qualquer objeto de entrada que seja válido após ter sido suficientemente treinado com um conjunto de exemplos

- Exemplos de Modelos
	- *Support Vector Machines*
	- *Linear Discriminant Analysis*
	- *Boosting*

- Exemplo KNN
	- K-Vizinhos
	- Baseado em instâncias
	- Não há "aprendizado"
		- Decisões são feitas para cada instância
	- k = 1
	![[Pasted image 20230520183602.png]]
	- k = 15
	![[Pasted image 20230520183715.png]]

###### Aprendizado não supervisionado

- Não utilizam exemplos de treinamento marcados
- Na maioria das vezes, trata o seu conjunto de entrada como um conjunto de variáveis aleatórias
- **Joint distribution model** é construído para a representação dos dados
- Objetivo desse aprendizado -> Avaliar como os dados estão organizados e agrupados

>[!INFO] Aprendizado semi-supervisionado
>Mistura os dois aprendizados


##### Avaliação e Comparação

- Viés e variância
- Treinamento e Teste
- Matriz de confusão
- Métricas e critérios
- Conjunto de validação e teste
- Validação cruzada
- Especificidade
- Sensitividade
- Curva Característica de Operação (ROC) = Sensitividade vs Especificidade

![[Pasted image 20230520183912.png]]



