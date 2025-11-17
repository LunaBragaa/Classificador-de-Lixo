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
(acurácia e matriz de confusão)

## 4. Conclusão

