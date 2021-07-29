# Trabalho-INC75-ReconheimentoDePosesHumanas

 ![Logo da UDESC Alto Vale](http://www1.udesc.br/imagens/id_submenu/2019/marca_alto_vale_horizontal_assinatura_rgb_01.jpg)
 
O projeto ideializa um aplicativo que tem o objetivo de indentificar a pose(esqueleto humano) e classificar conforma a técnica, chute ou soco.
 
 - [**Felipe Rohr Hoinoski**](mailto:felipehoinoski@gmail.com) 

# Sumário
* [Problema](#problema)
* [Dataset](#dataset)
* [Técnica](#tecnica)
* 

## [Problema](#problema)
 Criar uma aplicação que consiga analisar uma imagem e classificar se aquela imagem representa um golpe de punho utilizando os braços ou um golpe de chute utilizando as pernas. Os golpes serão baseados em qualquer forma de arte marcial ou luta, sendo apenas uma representação genérica de soco ou chute. O intuito é conseguir através do aplicativo e classificar e representar na tela através de um texto ou uma cor específica de cada golpe, seja por exemplo: um campo com o nome do golpe ou vermelho - soco, azul - chute.

## [Dataset](#dataset)
O dataset será desenvolvido através de um upload ou da captura de uma imagem conforme a utilização do aplicativo.

## [Técnica](#tecnica)

Para a implementação do modelo de classificação de poses, será utilizado o algoritmo K-NN (k-nearest neighbors algorithm) e do CNN (Convolutional Neural network). O processo do aplicativo funcionará em 2 etapas:
- Extração dos dados das imagens através de bibliotecas em Python (Phyton Solution API) baseadas na arquitetura para estimar poses humanas, proposta pelo BlazePose, que é uma rede neural convolucional (CNN). O resultado são dados com as predições do esqueleto humano marcados na imagens (landmarks) que serão exportadas para um arquivo .CSV .
- Classificação dos dados através de uma plataforma do Google colaboratory (Colab) com uma implementação de classificação genérica para poses através dos dados do arquivo CSV. Está servirá para a classificação com o algoritmo K-NN e deverá ser customizada para garantir a conformidade para a técnica proposta, socos ou chutes.


BlazePose - https://drive.google.com/file/d/11dqOT2VHsZay8KIIf_Kj0uAD9SNirAas/view

Colab - https://colab.research.google.com/drive/19txHpN8exWhstO6WVkfmYYVC6uug_oVR


