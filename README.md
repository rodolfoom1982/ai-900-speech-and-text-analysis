# AI-900: Análise de Sentimentos com Language Studio no Azure AI

## Descrição do Projeto

Este projeto é um dos laboratórios do Bootcamp [Microsoft Azure AI Fundamentals](https://web.dio.me/track/microsoft-azure-ai-fundamentals), promovido através da parceria entre a Microsoft e a Dio.me.

Os alunos deste bootcamp tem, como principal objetivo, se prepararem para o exame de certificação Microsoft AI-900, dominando conceitos como visão computacional, classificação inteligente de imagem e inteligência de documentos com IA, enquanto se familiarizam com as tecnologias da Microsoft Azure.

Este desafio é o de número 3 do bootcamp e consiste na execução prática de 2 exercícios, relacionados aos seguintes temas:

- [LAB 1: Azure Speech Studio](http://aka.ms/ai900-bing-copilot): experimentar os recursos do Azure AI Speech usando o Azure AI Speech Studio
- [LAB 2: Azure Language Studio](http://aka.ms/ai900-azure-openai): explorar os recursos da Linguagem de IA do Azure

<br>

## Acessos necessários

Para realizar estes laboratórios, eu precisei criar uma [Subscrição do Microsoft Azure](https://azure.microsoft.com/)

A Microsoft permite criar uma subscrição de teste, na qual vários serviços podem ser experimentados gratuitamente por 12 meses, além de receber $200 para serem utilizados nos primeiros 30 dias.

---

## LAB 1 - Introdução

O serviço de Fala de IA do Azure transcreve fala em texto e texto em fala audível.

Podemos utilizar o AI Speech para criar um aplicativo que possa transcrever anotações de reuniões ou gerar texto a partir da gravação de entrevistas.

Neste laboratório, abordei, especificamente, os recursos do Azure AI Speech dentro do Azure AI Speech Studio para realizar a legendagem automática de um vídeo.

<br>

## LAB 1 - Aprovisionamento dos recursos do Azure AI Service

Para executar o LAB 1, primeiramente, precisei aprovisionar o serviço Azure IA Service, através os seguintes passos:

1) Acessei o [Azure Portal](https://portal.azure.com/) e efetuei o login com a minha conta Microsoft
2) Efetuei as configurações conforme apresentadas abaixo:
   
   > ![alt text](readmeFiles/gifs/001.gif)

3) O serviço foi aprovisionado quando recebi a mensagem **Your deployment is complete**

   > ![alt text](readmeFiles/images/002.png)

<br>

## LAB 1 - Explorando a conversão de voz em texto no Speech Studio (legendagem)

1) Acessei o [Azure AI Speech Studio](https://speech.microsoft.com/)
2) Aqui foi necessário associar o AI Speech Studio ao recurso Azure IA Service, que aprovisionei [anteriormente](#Aprovisionamento-dos-recursos-do-Azure-AI-Service):
   
   > ***Mudar o recurso:***
   > ---
   > ![alt text](readmeFiles/images/003.png)

   ---
   
   > ***Selecionar o recurso:***
   > ---
   > ![alt text](readmeFiles/images/004.png)

3) Selecionei a *feature* **Legendar com conversão de fala em texto**:

   > ![alt text](readmeFiles/images/005.png)

4) Esta *feature* permite utilizar vídeos de amostra previamente carregados. Porém, optei por carregar um vídeo próprio para testar a efetividade (o vídeo que utilizei está disponível neste [link](inputs/videoSpeechToText.mp4):

   > ![alt text](readmeFiles/images/006.png)


5) Existem vários parâmetros que podem ser configurados para melhorar a legendagem do vídeo:

   > ![alt text](readmeFiles/images/007.png)

6) Seguem os detalhes de cada uma das configurações de legendagem:

   > ***Limite parcial estável:***
   > ---
   > ![alt text](readmeFiles/images/009.png)

   ---
   
   > ***Identificação de idioma:***
   > ---
   > ![alt text](readmeFiles/images/010.png)

   ---
   
   > ***Identificação de idioma no início:***
   > ---
   > ![alt text](readmeFiles/images/011.png)

   ---
   
   > ***Identificação de idioma contínuo:***
   > ---
   > ![alt text](readmeFiles/images/012.png)

   ---
   
   > ***Lista de frases:***
   > ---
   > ![alt text](readmeFiles/images/013.png)

   ---
   
   > ***Ponto de extremidade personalizado:***
   > ---
   > ![alt text](readmeFiles/images/014.png)


7) Quando executei o vídeo, as legendas foram geradas automaticamente e exibidas em tempo real ou próximo ao tempo real, de acordo com a configuração que fiz no parâmetro **Limite parcial estável**:

   > ![alt text](readmeFiles/images/015.png)

8) Existe um recurso muito interessante para os desenvolvedores que é o **código de exemplo**, permitindo a integração das aplicações com o serviço de legendagem:

   > ![alt text](readmeFiles/images/016.png)

9) Além disso, todo o texto que foi gerado pode ser acessado através da opção **legenda detectada** e, inclusive, pode ser baixado em um arquivo .txt:

   > ![alt text](readmeFiles/images/017.png)

<br>

## LAB 1 - Conclusão

Neste estudo, explorei o serviço Azure Speech Studio, com foco especial na sua capacidade de legendar através da conversão de fala em texto. Esta funcionalidade é uma ferramenta poderosa que pode ser aplicada em diversas situações, desde a transcrição de reuniões e conferências até a criação de legendas para vídeos.

No entanto, é importante lembrar que o Azure Speech Studio é muito mais do que apenas um serviço de transcrição. Ele oferece uma gama de outras funcionalidades que não foram abordadas em detalhe neste estudo, mas que são igualmente valiosas. Estas incluem a conversão de texto em fala, a tradução de fala e a personalização do modelo de fala, entre outras.

A versatilidade do Azure Speech Studio torna-o uma ferramenta indispensável para qualquer pessoa ou organização que procure melhorar a acessibilidade, a eficiência e a comunicação. Encorajos os leitores a explorarem estas outras funcionalidades para descobrir como elas podem ser aplicadas para atender às suas necessidades específicas.

Em resumo, o Azure Speech Studio é uma ferramenta robusta e multifuncional que tem o potencial de transformar a maneira como interagimos com a tecnologia e uns com os outros. Através da exploração contínua e da experimentação com suas diversas funcionalidades, podemos continuar a inovar e a melhorar nossas práticas de comunicação.

---

## LAB 2 - Introdução

O Processamento de Linguagem Natural (PNL) é um ramo da IA que lida com a linguagem escrita e falada. Você pode usar a PNL para criar soluções que extraem significado semântico do texto e/ou da fala ou que formulem respostas significativas em linguagem natural.

O PNL pode ser utilizado, por exemplo, para realizar a análise de avaliações enviadas pelos clientes de um determinado serviço prestado, onde é possível identificar frases-chave, determinar quais avaliações são positivas e quais são negativas ou analisar o texto de revisão em busca de menções a entidades conhecidas, como locais ou pessoas.

O Serviço de Linguagem de IA do Azure inclui análise de texto e recursos de PNL. Estes incluem a identificação de frases-chave no texto e a classificação do texto com base no sentimento.

Neste laboratório, eu explorei os recursos da Linguagem de IA do Azure analisando alguns exemplos de avaliações de hotéis, utilizando Azure Language Studio para entender se as avaliações são majoritariamente positivas ou negativas.

<br>

## LAB 2 - Aprovisionamento dos recursos do Azure Language Service

Para executar o LAB 1, primeiramente, precisei aprovisionar o serviço **Azure Language Service**, através os seguintes passos:

> [!NOTE]
> Ao selecionar o parâmetro ***Pricing tier*** (ou **Nível de preço**), secolha a opção **S...** grátis somente se a opção **F0** não estiver disponível

1) Acessei o [Azure Portal](https://portal.azure.com/) e efetuei o login com a minha conta Microsoft
2) Efetuei as configurações conforme apresentadas abaixo:
   
   > ![alt text](readmeFiles/gifs/018.gif)

3) O serviço foi aprovisionado quando recebi a mensagem **Your deployment is complete**

   > ![alt text](readmeFiles/images/019.png)



## LAB 2 - Explorando a análise de sentimentos com o Azure Language Studio

1) Acessei o [Azure Language Studio](https://language.cognitive.azure.com/?azure-portal=true/)
2) Logo após logar com minha conta Microsoft, tive que associar o serviço Languange que aprovisionei [anteriormente](#LAB-2---Aprovisionamento-dos-recursos-do-Azure-Language-Service):

   > ![](readmeFiles/readmeFiles/images/020.pngf)


# IMAGENS











![alt text](readmeFiles/images/020.png)
![alt text](readmeFiles/images/021.png)
![alt text](readmeFiles/images/022.png)
![alt text](readmeFiles/images/023.png)
![alt text](readmeFiles/images/024.png)
![alt text](readmeFiles/images/025.png)
![alt text](readmeFiles/images/026.png)

---

# Fim
