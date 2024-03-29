# AI-900: Análise de Sentimentos com Language Studio no Azure AI

![Static Badge](https://img.shields.io/badge/Status_Projeto:-Concluído_(12/Mar/2024)-green)

![Static Badge](https://img.shields.io/badge/Inteligência_Artificial_(IA)-blue)
![Static Badge](https://img.shields.io/badge/IA_Generativa-blue)
![Static Badge](https://img.shields.io/badge/IA_Speech_(Legendagem)-blue)
![Static Badge](https://img.shields.io/badge/IA_Processamento_de_Linguagem_Natural-blue)
![Static Badge](https://img.shields.io/badge/IA_Análise_de_Sentimentos-blue)

![Static Badge](https://img.shields.io/badge/Microsoft_Azure-orange)
![Static Badge](https://img.shields.io/badge/Azure_AI_Services-orange)
![Static Badge](https://img.shields.io/badge/Azure_Language_Services-orange)
![Static Badge](https://img.shields.io/badge/Azure_Speech_Studio-orange)
![Static Badge](https://img.shields.io/badge/Azure_Language_Studio-orange)

<br>

## Índice

- [Descrição do Projeto](#Descrição-do-Projeto)
- [Acessos necessários](#Acessos-necessários)
- [LAB 1 - Introdução](#LAB-1---Introdução)
- [LAB 1 - Aprovisionamento dos recursos do Azure AI Service](#LAB-1---Aprovisionamento-dos-recursos-do-Azure-AI-Service)
- [LAB 1 - Explorando a conversão de voz em texto no Speech Studio (legendagem)](#LAB-1---Explorando-a-conversão-de-voz-em-texto-no-Speech-Studio---Legendagem)
- [LAB 1 - Conclusão](#LAB-1---Conclusão)
- [LAB 2 - Introdução](#LAB-2---Introdução)
- [LAB 2 - Aprovisionamento dos recursos do Azure Language Service](#LAB-2---Aprovisionamento-dos-recursos-do-Azure-Language-Service)
- [LAB 2 - Explorando a análise de sentimentos com o Azure Language Studio](#LAB-2---Explorando-a-análise-de-sentimentos-com-o-Azure-Language-Studio)
- [LAB 2 - Conclusão](#LAB-2---Conclusão)
- [Limpando o ambiente](#Limpando-o-ambiente)
- [Certificados e Certificações Associados ao Projeto](#Certificados-e-Certificações-Associados-ao-Projeto)

<br>

## Descrição do Projeto

Este projeto é um dos laboratórios do Bootcamp [Microsoft Azure AI Fundamentals](https://web.dio.me/track/microsoft-azure-ai-fundamentals), promovido através da parceria entre a Microsoft e a Dio.me.

Os alunos deste bootcamp tem, como principal objetivo, se prepararem para o exame de certificação Microsoft AI-900, dominando conceitos como visão computacional, classificação inteligente de imagem e inteligência de documentos com IA, enquanto se familiarizam com as tecnologias da Microsoft Azure.

Este desafio é o de número 3 do bootcamp e consiste na execução prática de 2 exercícios, relacionados aos seguintes temas:

- [LAB 1: Azure Speech Studio](http://aka.ms/ai900-speech): experimentar os recursos do Azure AI Speech usando o Azure AI Speech Studio
- [LAB 2: Azure Language Studio](http://aka.ms/ai900-text-analysis): explorar os recursos da Linguagem de IA do Azure

<br>

## Acessos necessários

Para realizar estes laboratórios, eu precisei criar uma [Subscrição do Microsoft Azure](https://azure.microsoft.com/)

A Microsoft permite criar uma subscrição de teste, na qual vários serviços podem ser experimentados gratuitamente por 12 meses, além de receber $200 para serem utilizados nos primeiros 30 dias.

---

<br>

## LAB 1 - Introdução

O serviço de Fala de IA do Azure transcreve fala em texto e texto em fala audível.

Podemos utilizar o AI Speech para criar um aplicativo que possa transcrever anotações de reuniões ou gerar texto a partir da gravação de entrevistas.

Neste laboratório, abordei, especificamente, os recursos do Azure AI Speech dentro do Azure AI Speech Studio para realizar a legendagem automática de um vídeo.

<br>

## LAB 1 - Aprovisionamento dos recursos do Azure AI Service

Para executar o LAB 1, primeiramente, precisei aprovisionar o serviço Azure IA Service, através os seguintes passos:

1) Acessei o [Azure Portal](https://portal.azure.com/) e efetuei o login com a minha conta Microsoft
2) Efetuei as configurações conforme apresentadas abaixo:
   
   > ![](readmeFiles/gifs/001.gif)

3) O serviço foi aprovisionado quando recebi a mensagem **Your deployment is complete**:

   > ![](readmeFiles/images/002.png)

<br>

## LAB 1 - Explorando a conversão de voz em texto no Speech Studio - Legendagem

1) Acessei o [Azure AI Speech Studio](https://speech.microsoft.com/)
2) Aqui foi necessário associar o AI Speech Studio ao recurso Azure IA Service, que aprovisionei [anteriormente](#Aprovisionamento-dos-recursos-do-Azure-AI-Service):
   
   > ***Mudar o recurso:***
   > ---
   > ![](readmeFiles/images/003.png)

   ---
   
   > ***Selecionar o recurso:***
   > ---
   > ![](readmeFiles/images/004.png)

3) Selecionei a *feature* **Legendar com conversão de fala em texto**:

   > ![](readmeFiles/images/005.png)

4) Esta *feature* permite utilizar vídeos de amostra previamente carregados. Porém, optei por carregar um vídeo próprio para testar a efetividade (o vídeo que utilizei está disponível neste [link](inputs/videoSpeechToText.mp4):

   > ![](readmeFiles/images/006.png)


5) Existem vários parâmetros que podem ser configurados para melhorar a legendagem do vídeo:

   > ![](readmeFiles/images/007.png)

6) Seguem os detalhes de cada uma das configurações de legendagem:

   > ***Limite parcial estável:***
   > ---
   > ![](readmeFiles/images/009.png)

   ---
   
   > ***Identificação de idioma:***
   > ---
   > ![](readmeFiles/images/010.png)

   ---
   
   > ***Identificação de idioma no início:***
   > ---
   > ![](readmeFiles/images/011.png)

   ---
   
   > ***Identificação de idioma contínuo:***
   > ---
   > ![](readmeFiles/images/012.png)

   ---
   
   > ***Lista de frases:***
   > ---
   > ![](readmeFiles/images/013.png)

   ---
   
   > ***Ponto de extremidade personalizado:***
   > ---
   > ![](readmeFiles/images/014.png)


7) Quando executei o vídeo, as legendas foram geradas automaticamente e exibidas em tempo real ou próximo ao tempo real, de acordo com a configuração que fiz no parâmetro **Limite parcial estável**:

   > ![](readmeFiles/images/015.png)

8) Existe um recurso muito interessante para os desenvolvedores que é o **código de exemplo**, permitindo a integração das aplicações com o serviço de legendagem:

   > ![](readmeFiles/images/016.png)

9) Além disso, todo o texto que foi gerado pode ser acessado através da opção **legenda detectada** e, inclusive, pode ser baixado em um arquivo .txt:

   > ![](readmeFiles/images/017.png)

<br>

## LAB 1 - Conclusão

Neste estudo, explorei o serviço Azure Speech Studio, com foco especial na sua capacidade de legendar através da conversão de fala em texto. Esta funcionalidade é uma ferramenta poderosa que pode ser aplicada em diversas situações, desde a transcrição de reuniões e conferências até a criação de legendas para vídeos.

No entanto, é importante lembrar que o Azure Speech Studio é muito mais do que apenas um serviço de transcrição. Ele oferece uma gama de outras funcionalidades que não foram abordadas em detalhe neste estudo, mas que são igualmente valiosas. Estas incluem a conversão de texto em fala, a tradução de fala e a personalização do modelo de fala, entre outras.

A versatilidade do Azure Speech Studio torna-o uma ferramenta indispensável para qualquer pessoa ou organização que procure melhorar a acessibilidade, a eficiência e a comunicação. Encorajos os leitores a explorarem estas outras funcionalidades para descobrir como elas podem ser aplicadas para atender às suas necessidades específicas.

Em resumo, o Azure Speech Studio é uma ferramenta robusta e multifuncional que tem o potencial de transformar a maneira como interagimos com a tecnologia e uns com os outros. Através da exploração contínua e da experimentação com suas diversas funcionalidades, podemos continuar a inovar e a melhorar nossas práticas de comunicação.

---

<br>

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
   
   > ![](readmeFiles/gifs/018.gif)

3) O serviço foi aprovisionado quando recebi a mensagem **Your deployment is complete**

   > ![](readmeFiles/images/019.png)

<br>

## LAB 2 - Explorando a análise de sentimentos com o Azure Language Studio

1) Acessei o [Azure Language Studio](https://language.cognitive.azure.com/?azure-portal=true/)
2) Logo após logar com minha conta Microsoft, tive que associar o serviço Languange que aprovisionei [anteriormente](#LAB-2---Aprovisionamento-dos-recursos-do-Azure-Language-Service):

      > ![](readmeFiles/images/020.png)

3) Selecionei a *feature* **Analyze sentiment and mine opinions**, que fica dentro do grupo **Classify text**:

     > ![](readmeFiles/images/021.png)

4) Neste primeiro momento, quis ver como o Language Studio realiza a análise de uma avaliação negativa do cliente para um hotel. Para tanto, peguei uma avaliação aleatória *ipsis litteris* no site [Trip Advisor](https://www.tripadvisor.com), cujo texto retorna o seguinte:
   > Este acima é somente um trecho da avaliação, que pode ser visualizada, de forma completa, [aqui](inputs/texto01AnalyzeSentiment.txt)

   ```
   Péssima experiencia - Propaganda Enganosa
   Bom dia aos responsáveis pelo Resort Vila Galé Angra dos Reis
   Venho através desta dar o meu parecer sobre a minha estadia no Resort acima citado.
   Como vocês podem ver no meu histórico de agendamento eu havia contratado o Vila Galé de Maceió,
   infelizmente meu pai adoeceu e foi internado as pressa na UTI e tive que retornar Para SP tendo
   que adiar minha estadia que eram para 3 noites, pois bem, nos deram 12 meses para utilizar
   aonde eu quiser. Antes de tudo isso minha irmã (...)
   ```

5) Selecionei o idioma da avaliação no campo ***Select text language*** e marquei a opção ***Enable opinion mining***, que permite ao serviço mineirar opiniões constantes na avaliação:

   > ![](readmeFiles/images/022.png)

6) Antes de continuar, tive que marcar que estava ciente de que a execução deste serviço iria consumir recursos da minha Azure Subscription:

   > ![](readmeFiles/images/023.png)

7) O resultado foi muito interessante:

   O Language Studio identificou que a avaliação possui um mix de sentimentos, sendo predominantemente de pontos negativos (78%), além de 17% de pontos positivos e 5% de neutralidade:
   
   > ![](readmeFiles/images/024A.png)
   
   Além disso, ele fez uma análise sentença a sentença, procurando um nexo entre os termos das opiniões dadas. Por exemplo, para a expressão **péssima experiência**, ele identificou uma negatividade de 99%. Já na expressão **propaganda enganosa**, a negatividade também foi percebida (94%)
   
   > ![](readmeFiles/images/024B.png)

8) Resolvi fazer um novo teste. Desta vez, utilizei uma avaliação positiva extraída *ipsis litteris*, também, do site [Trip Advisor](https://www.tripadvisor.com):

   ```
   melhor viagem da vida!
   Os quartos são super confortáveis, a cama maravilhosaa. Passei todos os dias com o tio Pudim,
   um monitor super legal e atencioso. A comida bastante diversa e saborosa! as piscinas super
   relaxantes tambem, adorei muito! Minha hospedagem foi maravilhosa. Não tenho o que reclamar
   ```

9) Mantive os mesmos parâmetros da pesquisa anterior:

    > ![](readmeFiles/images/025.png)

10) Como resultado, a análise foi predominante positiva (99%), o que era esperado. E isso pode ser comprovado, também, através da mineração das opiniões por frase, como na expressão **melhor viagem**, com 100% de positividade:

    > ![](readmeFiles/images/026.png)

<br>

## LAB 2 - Conclusão

Neste estudo, explorei o poder do Azure Language Studio, com foco especial na análise de sentimentos e na mineração de opiniões. Essas ferramentas oferecem uma visão profunda dos dados textuais, permitindo que as empresas entendam melhor seus clientes e tomem decisões informadas.

No entanto, é importante lembrar que o Azure Language Studio oferece muito mais do que apenas essas funções. Existem outras capacidades poderosas, como a extração de frases-chave, a detecção de idioma e a identificação de entidades nomeadas, que não foram abordadas em detalhes neste artigo.

O Azure Language Studio é uma ferramenta versátil e robusta que pode ser adaptada a uma variedade de cenários de uso. Seja você um cientista de dados procurando entender grandes volumes de texto ou uma empresa procurando obter insights de dados de clientes, o Azure Language Studio tem algo a oferecer.

Com suas diversas funcionalidades, o Azure Language Studio ele abre um mundo de possibilidades para análise de dados e inteligência de negócios.

---

<br>

## Limpando o ambiente

> [!WARNING]
> Após a conclusão do projeto, se não for reaproveitar os recursos utilizados, é aconselhável excluí-los, bem como os grupos de recursos, para que não haja cobranças indevidas na sua Azure Subscription

<br>

## Certificados e Certificações Associados ao Projeto

![](https://github.com/rodolfoom1982/meus-certificados/blob/main/dio-bootcamp-ai-900-azure-ai-fundamentals/conceitos-de-processamento-de-linguagem-natural.png)

![](https://github.com/rodolfoom1982/meus-certificados/blob/main/dio-bootcamp-ai-900-azure-ai-fundamentals/analise-de-sentimentos-com-language-studio-no-azure-ai.jpg)

![](https://github.com/rodolfoom1982/meus-certificados/blob/main/dio-bootcamp-ai-900-azure-ai-fundamentals/microsoft-azure-ai-fundamentals.png)
