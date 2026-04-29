# Classificação de Superfícies de Vias
 
> Solução desenvolvida para o desafio técnico da **Voxar Labs**, que propõe classificar imagens de superfícies urbanas e rurais em três categorias: **Asphalt**, **Belgian Blocks** e **Off-road**.
 
---
 
## 📋 Sobre o desafio
 
O objetivo não era maximizar performance, mas demonstrar capacidade de:
 
- Estruturar um problema de visão computacional
- Desenvolver uma solução inicial viável
- Investigar criticamente os resultados
- Comunicar as decisões de forma clara
O dataset é real, **altamente desbalanceado**, e inclui condições visuais desafiadoras — variações de iluminação, chuva, período noturno e diferentes dispositivos de captura.
 
---
 
## 🧠 Abordagem
 
A solução é baseada em **Transfer Learning** com a arquitetura **ResNet18** pré-treinada no ImageNet, escolhida por sua eficiência e bom desempenho em tarefas de classificação com datasets de tamanho moderado.
 
---
 
## 📁 Estrutura do notebook
 
O arquivo `road_classification.ipynb` concentra toda a solução — tanto a documentação técnica quanto o código — seguindo o formato exigido pelo edital. Está organizado nas seguintes seções:
 
| # | Seção | Descrição |
|---|-------|-----------|
| 1 | **Identificação da abordagem** | Descrição do modelo, justificativa e bibliotecas utilizadas |
| 2 | **Entendimento do problema** | Análise inicial do dataset e dos desafios esperados |
| 3 | **Pré-processamento e carregamento dos dados** | Transformações de entrada e análise de distribuição de classes |
| 4 | **Pipeline de treinamento e avaliação** | Estrutura reutilizável entre os experimentos |
| 5 | **Baseline** | Modelo com fine-tuning apenas na camada final, sem tratamento de desbalanceamento |
| 6 | **Experimento 1 — Class Weights** | Hipótese: penalizar classes majoritárias melhora recall nas minoritárias |
| 7 | **Experimento 2 — Fine-Tuning** | Hipótese: descongelar camadas mais profundas aumenta a capacidade de adaptação ao domínio |
| 8 | **Experimento 3 — Data Augmentation** | Hipótese: variações sintéticas reduzem overfitting e melhoram generalização |
| 9 | **Comparação entre os modelos** | Tabela consolidada de métricas |
| 10 | **Análise crítica** | Onde a abordagem funcionou, onde falhou e próximos passos |
| 11 | **Uso de ferramentas** | Transparência sobre o uso de LLMs no processo |
 
---
 
## 🛠️ Tecnologias
 
| Biblioteca | Uso |
|------------|-----|
| `torch` / `torchvision` | Modelo, treinamento e carregamento de dados |
| `scikit-learn` | Métricas e matriz de confusão |
| `matplotlib` / `seaborn` | Visualizações |
