# Tema 2: Classificação de Lixo para Reciclagem
**Disciplina:** Fundamentos de Inteligência Artificial (FIA)  
**Professor:** Edjard Mota

**Link para colab:** https://colab.research.google.com/drive/1-yusfa1KWHCgExvv30kPbbCuVvS7mM_l?usp=sharing

## 👥 Equipe
• Estefany Licinha Mendes da Silva  
• Karen Juliana Báez González  
• Luna Veiga Horta Braga  
• Rebeca Gabrielle Xavier Martins de Mello  
• Samuel Davi Silva de Lima Chagas  

## 📋 Sumário  
1. [Descrição do Projeto](#1-descrição-do-projeto)
2. [Análise do Dataset](#2-análise-do-dataset)
3. [Resultados](#3-resultados)
4. [Conclusão](#4-conclusão)

## 1. Descrição do Projeto  
### Objetivo
O projeto tem como objetivo desenvolver um classificador de imagens multiclasse utilizando Redes Neurais Convolucionais (CNN) para categorizar resíduos em seis categorias distintas: glass (vidro), paper (papel), cardboard (papelão), plastic (plástico), metal e trash (lixo orgânico/rejeito). 

### Importância  
O desenvolvimento de um sistema automático para classificação de resíduos é essencial para tornar o processo de reciclagem mais rápido, eficiente e acessível. A solução proposta demonstra como técnicas de visão computacional podem apoiar a triagem de materiais, permitindo identificar e separar diferentes tipos de resíduos com maior precisão e agilidade.   

Segundo dados da Organização das Nações Unidas (ONU), a produção anual de resíduos já ultrapassa 2 bilhões de toneladas, e esse número cresce continuamente. Nesse cenário, torna-se urgente buscar alternativas tecnológicas que tornem a gestão de resíduos mais eficaz. A automação exerce um papel estratégico ao aumentar as taxas de reciclagem, reduzir a contaminação entre materiais e diminuir custos operacionais, especialmente em ambientes industriais e urbanos.  

Além de seus benefícios diretos, iniciativas como esta fortalecem a integração entre tecnologia e sustentabilidade, contribuindo para metas globais como os Objetivos de Desenvolvimento Sustentável (ODS) da ONU e para discussões internacionais sobre clima, como as previstas para a COP 30. Dessa forma, o projeto evidencia como soluções baseadas em inteligência artificial podem gerar impactos reais e significativos ao enfrentar desafios ambientais contemporâneos.  

## 2. Análise do Dataset  
O dataset TrashNet está sendo utilizado como base para a classificação de resíduos, contendo 2.527 imagens divididas em seis categorias: vidro, papel, papelão, plástico, metal e lixo orgânico/rejeito. As imagens possuem resolução padronizada (512×384), o que ajuda a manter consistência no pré-processamento. Entretanto, a baixa quantidade de dados torna necessário aplicar técnicas de data augmentation, como rotações, zoom e espelhamentos, para ampliar artificialmente o conjunto de treino e reduzir o risco de overfitting.  

Embora seja um dataset útil para exercícios de visão computacional, ele apresenta algumas limitações importantes. A primeira é o tamanho relativamente reduzido: para problemas de classificação de imagens, 2.527 amostras é considerado pouco. Além disso, as classes não estão balanceadas, por exemplo: a classe trash possui menos imagens do que as demais. Esse desbalanceamento pode prejudicar o aprendizado do modelo, fazendo com que ele tenha dificuldade em reconhecer as categorias menos representadas.  

## 3. Resultados
O modelo foi treinado utilizando o dataset TrashNet com técnicas de data augmentation para aumentar a variabilidade das amostras. Os gráficos de acurácia e loss demonstram que o desempenho do modelo evoluiu de forma consistente ao longo das épocas. A acurácia aumentou progressivamente, aproximando-se de 0,75 tanto no conjunto de treino quanto de validação, enquanto o erro apresentou queda contínua. Essa trajetória indica aprendizado estável e ausência de sobreajuste significativo, uma vez que as curvas de treino e validação evoluem de maneira próxima.

![graficos](https://github.com/user-attachments/assets/7c8e1644-9a5a-4180-a447-add960349646)


Apesar do bom comportamento geral, a classe trash apresentou desempenho consideravelmente inferior às demais. Isso ocorreu mesmo após a aplicação combinada de três estratégias: data augmentation, Focal Loss e Fine-Tuning das camadas superiores. Embora essas técnicas tenham ampliado a robustez do treinamento, elas não foram suficientes para superar as limitações impostas pelo baixo número de amostras e pela grande variação visual presente na classe trash, fatores que dificultaram a consolidação de padrões discriminativos.

A avaliação final no conjunto de teste evidencia esse comportamento. As classes cardboard, glass, metal, paper e plastic obtiveram bons níveis de acerto, com forte concentração de valores na diagonal da matriz de confusão. Essas classes apresentam características mais estruturadas e visualmente consistentes, o que favorece o aprendizado da rede. Por outro lado, a classe trash foi a menos precisa, ainda que tenha obtido algum nível de acerto (18 classificações corretas), apresentando confusões distribuídas principalmente com paper, metal e cardboard. Essa dispersão reforça que o modelo não identificou um padrão visual estável para essa categoria.

![matrizConfusao](https://github.com/user-attachments/assets/54166dc9-7247-48fa-a1f7-b8ca9a2d696c)

A matriz de confusão ilustra esses resultados. Observa-se que:
*paper possui o melhor desempenho absoluto, com 106 acertos, sem grandes confusões com outras classes.
*cardboard, glass e metal também apresentam acertos altos, com pequenos erros distribuídos.
*plastic mantém desempenho razoável, mas mostra confusão relevante com paper (27 casos), o que pode ser explicado por texturas semelhantes quando visualizadas em determinadas condições de iluminação.
*trash apresenta o pior resultado, mesmo com as técnicas extras aplicadas, evidenciando forte influência do desbalanceamento e da diversidade visual da classe.

De forma geral, o modelo demonstra bom aprendizado para a maior parte do dataset, mas sua capacidade de generalização para a classe trash permanece limitada, sugerindo a necessidade de estratégias adicionais, como coleta de mais amostras, aumento da qualidade das imagens ou uso de arquiteturas pré-treinadas mais robustas em cenários de alta variabilidade.


## 4. Conclusão

Este trabalho desenvolveu um classificador de resíduos utilizando Redes Neurais Convolucionais (CNN) para categorizar imagens em seis classes. O principal desafio enfrentado foi o tamanho reduzido do dataset TrashNet (2.527 imagens) e seu desbalanceamento, especialmente na classe "trash" com apenas 137 exemplos.
Para superar essas limitações, foram implementadas técnicas complementares: data augmentation para expandir artificialmente o dataset através de transformações como rotação e zoom, fine-tuning para otimizar os pesos da rede, e Focal Loss para lidar com o desbalanceamento entre classes. A combinação dessas estratégias foi bem-sucedida no combate ao overfitting, demonstrando convergência equilibrada entre as métricas de treino e validação.

Apesar do sucesso no controle do overfitting, a acurácia final do modelo não atingiu valores elevados. Essa limitação pode ser atribuída ao tamanho reduzido do dataset original, à similaridade visual entre algumas categorias e à variabilidade dos objetos descartados. Os resultados evidenciam que, mesmo com técnicas avançadas de regularização, a quantidade e qualidade dos dados de treino continuam sendo fatores limitantes fundamentais no desempenho de modelos de deep learning.
O projeto demonstra que é possível desenvolver soluções de inteligência artificial para triagem automática de resíduos mesmo com recursos limitados, contribuindo para processos de reciclagem mais eficientes e sustentáveis.

