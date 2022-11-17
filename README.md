# Trabalho-INC75-ClassificaçãoDePosesDoYoga

 ![Logo da UDESC Alto Vale](http://www1.udesc.br/imagens/id_submenu/2019/marca_alto_vale_horizontal_assinatura_rgb_01.jpg)
 
O projeto idealiza um trabalho de reconhecimento de imagens de yoga, desenvolvido para contemplar o trabalho prática da disciplina de inteligência artificial.

 - [**Felipe Rohr Hoinoski**](mailto:felipehoinoski@gmail.com) 

# Sumário
* [Problema](#problema)
* [Dataset](#dataset)
* [Técnica](#tecnica)
* [Resultados Obtidos](#resultados)
* [Instruções de uso do software](#instrucoes)
* [Vídeo](#video)

## [Problema](#problema)
 A tarefa de classificação e reconhecimento de imagens é uma das tarefas mais requisitadas e desenvolvidas na área de IA, o desafio é treinar um modelo que possa reconhecer de forma automática um objeto, gesto ou pose de imagens. O treinamento depende da estratégia escolhida por cada sistema, como algoritmos específicos de machine learning ou arquiteturas neurais de aprendizado, nesta etapa são aprendidas as características (features) das imagens que serão utilizadas como parâmetro para as futuras previsões. A Yoga descreve um cenário que a identificação de poses é válida através de imagens, as poses são normalmente estáticas utilizando de técnicas de alongamento e respiração, ou seja a captura das poses são de facilitadas e através de uma foto o sistema pode dizer qual o nome da pose.

## [Dataset](#dataset)
Para o desenvolvimento do modelo, foi utilizado um dataset disponibilizado em: https://www.kaggle.com/niharika41298/yoga-poses-dataset/tasks?taskId=2436. 
O dataset é dividido em imagens de treinamento e teste, e uma segunda divisão de 5 poses diferentes da yoga: downdog, goddess, plank, tree, warrior2.

## [Técnica](#tecnica)

Para resolver o problema e construir o sistema de classificação de imagens, foi aplicado um modelo de rede neural e uma interface web simples para captar o imput de imagens do usuário.

- Para a extração das features das poses foi utilizada uma rede neural disponibilizada pelo TensorFlow, mais especificamente pelo módulo Keras (InceptionV3). InceptionV3 é uma rede neural de transferência do tipo CNN (rede neural convolucional). O modelo utilizado neste sistema é descrito por um modelo customizado que implementa os layers de entrada da arquitetura do Inception e como layers para saída utiliza nodos neurais densos, o número de nodos corresponde ao número de labels (classes) do dataset, ou seja, as poses de yoga.
- https://keras.io/api/applications/inceptionv3/

- O modelo depois de treinado poderá prever o nome da pose conforme a imagem passada na aplicação web utilizando servidor criado utilizando o framework Flask do Python.
- https://flask.palletsprojects.com/en/2.0.x/

## [Resultados Obtidos](#resultados)

Para os resultados do modelo foi utilizado de testes baseados na precisão (precision) e perda (loss) do modelo durante a fase de treinamento. Utilizamos de testes que envolveram graficar as proporções dos valores de precisão e perda conforma ajustados em cada época que o modelo testava. As épocas permitem a rede neural alterar os pesos e dessa maneira aprender com as características das imagens. Todos os testes que foram aplicados tentando controlar os valores e proporções de precisão e perda, seja utilizando maior número de épocas ou mudando algumas configurações como embaralhar o datase, os resultados gerais apresentaram dados como accuracy superior a 0.88, em contrapartida, os valores de loss tb ficaram altos, o'que tornou os valores falsos positivos apresentados pela matriz de confusão muito altos. Abaixo estão apresentados os gráficos e a matriz de confusão do dataset de teste.

![Loss](https://github.com/feliperohr/trabalho-inc75-AnaliseDePoses/blob/main/img/LossVal_loss.png)

![Accuracy](https://github.com/feliperohr/trabalho-inc75-AnaliseDePoses/blob/main/img/AccVal_acc.png)

![Matriz](https://github.com/feliperohr/trabalho-inc75-AnaliseDePoses/blob/main/img/Matriz.png)

Por fim, os resultados mostram que os gráficos, ou seja, os valores de precisão e perda se mantiveram satisfatórios, apesar da matriz apresentar um aspecto misto de informações, previsões erradas no sistema. 

## [Instruções de uso do software](#instrucoes)

Os detalhes para preparar o ambiente e conseguir rodar o projeto estão no arquivo de instrucoes.txt










