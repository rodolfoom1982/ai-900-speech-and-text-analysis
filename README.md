# AI-900: Análise de Sentimentos com Language Studio no Azure AI

## Descrição do Projeto

Este projeto é um dos laboratórios do Bootcamp [Microsoft Azure AI Fundamentals](https://web.dio.me/track/microsoft-azure-ai-fundamentals), promovido através da parceria entre a Microsoft e a Dio.me.

Os alunos deste bootcamp tem, como principal objetivo, se prepararem para o exame de certificação Microsoft AI-900, dominando conceitos como visão computacional, classificação inteligente de imagem e inteligência de documentos com IA, enquanto se familiarizam com as tecnologias da Microsoft Azure.

Este desafio é o de número 3 do bootcamp e consiste na execução prática de 2 exercícios, relacionados aos seguintes temas:

- [LAB 1: Azure Speech Studio](http://aka.ms/ai900-bing-copilot): experimentar os recursos do Azure AI Speech usando o Azure AI Speech Studio
- [LAB 2: Azure Language Studio](http://aka.ms/ai900-azure-openai): explorar os recursos da Linguagem de IA do Azure

<br>

## Acessos necessários

Para realizar estes laboratórios, é necessário criar uma [Subscrição do Microsoft Azure](https://azure.microsoft.com/)

<br>

## LAB 1 - Introdução

O serviço de Fala de IA do Azure transcreve fala em texto e texto em fala audível.

Você pode usar o AI Speech para criar um aplicativo que possa transcrever anotações de reuniões ou gerar texto a partir da gravação de entrevistas.

Neste laboratório, serão abordados os recursos do Azure AI Speech usando o Azure AI Speech Studio.

<br>

## LAB 1 - Aprovisionamento dos recursos do Azure AI Service

Para executar o LAB 1 é necessário aprovisionar o serviço Azure IA Service, atravé os seguintes passos:

1) Acesse o [Azure Portal](https://portal.azure.com/) e efetue o login com a sua conta Microsoft
2) Efetue as configurações conforme apresentadas abaixo:
   
   > ![alt text](readmeFiles/gifs/001.gif)

3) O serviço estará aprovisionado quando você ver a mensagem **Your deployment is complete**

   > ![alt text](readmeFiles/images/002.png)

<br>

## LAB 1 - Explorando a conversão de voz em texto no Speech Studio (legendagem)

1) Acessar o [Azure AI Speech Studio](https://speech.microsoft.com/)
2) Aqui é necessário associar o AI Speech Studio ao recurso Azure IA Service, que foi aprovisionado [anteriormente](#Aprovisionamento-dos-recursos-do-Azure-AI-Service):
   
   > ***Mudar o recurso:***
   > ---
   > ![alt text](readmeFiles/images/003.png)

   ---
   
   > ***Selecionar o recurso:***
   > ---
   > ![alt text](readmeFiles/images/004.png)

3) Selecionar a *feature* **Legendar com conversão de fala em texto**:

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


7) Ao executar o vídeo, as legendas são geradas automaticamente e exibidas em tempo real ou próximo ao tempo real, de acordo com a configuração do parâmetro **Limite parcial estável**:

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
















![alt text](readmeFiles/gifs/018.gif)
![alt text](readmeFiles/images/019.png)
![alt text](readmeFiles/images/020.png)
![alt text](readmeFiles/images/021.png)
![alt text](readmeFiles/images/022.png)
![alt text](readmeFiles/images/023.png)
![alt text](readmeFiles/images/024.png)
![alt text](readmeFiles/images/025.png)
![alt text](readmeFiles/images/026.png)
