# Tema 2: Classificação de Lixo para Reciclagem
**Disciplina:** Fundamentos de Inteligência Artificial (FIA)  
**Professor:** Edjard Mota

## 👥 Equipe
• Estefany Licinha Mendes da Silva  
• Karen Juliana Báez González  
• Luna Veiga Horta Braga  
• Rebeca Gabrielle Xavier Martins de Mello  
• Samuel Davi Silva de Lima Chagas  

## 📋 Sumário  
1. [Descrição do Projeto](#1-descrição-do-projeto)
2. [Análise do Dataset](#2-análise-do-dataset)

## 1. Descrição do Projeto  
### Objetivo
O projeto tem como objetivo desenvolver um classificador de imagens multiclasse utilizando Redes Neurais Convolucionais (CNN) para categorizar resíduos em seis categorias distintas: glass (vidro), paper (papel), cardboard (papelão), plastic (plástico), metal e trash (lixo orgânico/rejeito). 

### Importância  
O desenvolvimento de um sistema de classificação de resíduos é fundamental para tornar a reciclagem mais rápida, eficiente e acessível. A proposta apresentada no projeto permite desenvolver sistemas inteligentes capazes de identificar e separar diferentes tipos de materiais recicláveis com rapidez e precisão.  

De acordo com a Organização das Nações Unidas (ONU), a produção anual de resíduos ultrapassa 2 bilhões de toneladas. Nessa perspectiva, a geração de rejeitos aumenta continuamente e torna-se essencial buscar soluções que tornem o processo de triagem mais eficiente. A automação desempenha um papel central nesse contexto, pois aumenta as taxas de reciclagem, reduz a contaminação entre materiais e diminui custos operacionais. Além disso, iniciativas como esta aproximam a tecnologia das metas globais de sustentabilidade, alinhando-se a agendas internacionais, como os Objetivos de Desenvolvimento Sustentável da ONU e as discussões da COP 30. Assim, o projeto demonstra como técnicas de inteligência artificial podem gerar impactos significativos quando aplicadas aos problemas reais.  

## 2. Análise do Dataset  
O dataset TrashNet contém 2.527 imagens divididas em seis categorias de resíduo: vidro, papel, papelão, plástico, metal e lixo orgânico/rejeito. As imagens possuem resolução padronizada (512×384), o que ajuda a manter consistência no pré-processamento. Entretanto, a baixa quantidade de dados torna necessário aplicar técnicas de data augmentation, como rotações, zoom e espelhamentos, para ampliar artificialmente o conjunto de treino e reduzir o risco de overfitting.  


Embora seja um dataset útil para exercícios de visão computacional, ele apresenta algumas limitações importantes. A primeira é o tamanho relativamente reduzido: para problemas de classificação de imagens, 2.527 amostras é considerado pouco. Além disso, as classes não estão balanceadas, por exemplo: a classe trash possui menos imagens do que as demais. Esse desbalanceamento pode prejudicar o aprendizado do modelo, fazendo com que ele tenha dificuldade em reconhecer as categorias menos representadas.


## Resultados
(acurácia e matriz de confusão)

## Conclusão

