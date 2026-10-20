# 🐥 Previsão de peso de pintinhos com Regressão Linear Múltipla

![Capa do trabalho](./Capa.png)

Trabalho de extensão da matéria de Inteligência Artificial (Estácio), feito com dados da empresa Avecon, do segmento agropecuário: um modelo em Python que prevê o peso médio dos pintinhos de 7 a 42 dias de idade a partir de idade, sexo, estação do ano e linhagem.

**Stack:** Python · Pandas · scikit-learn · Plotly · Google Colab
**Período:** nov. de 2024

[📖 Ler o ebook](./Trabalho%20de%20Extens%C3%A3o.pdf) · [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Dayanebiaerafa/trabalho-de-extensao-ia/blob/main/Trabalho_de_Extens%C3%A3o.ipynb)

---

## Onde está o código

Este repositório tem o notebook do Google Colab ([Trabalho_de_Extensão.ipynb](./Trabalho_de_Extens%C3%A3o.ipynb)) e um ebook em PDF que explica o código passo a passo, com os resultados.

Os dados reais da empresa (um arquivo CSV) **não estão neste repositório**, por isso o notebook não roda sem esse arquivo. Para entender o trabalho, leia o ebook.

## O problema

Estimar o peso médio dos pintinhos ao longo do crescimento (de 7 a 42 dias) para apoiar decisões de manejo na granja.

## Os dados

- **Entradas:** idade (em dias), sexo, estação do ano e linhagem (10 linhagens).
- **Valor previsto:** peso médio (`peso_misto_avg`), em kg.

## O que foi feito

1. **Carregar os dados** de um arquivo CSV com o Pandas.
2. **Separar entradas e resultado:** o peso estava como texto com vírgula e foi convertido para número.
3. **Dividir os dados:** 80% para treino e 20% para teste (`random_state=42`, para o resultado ser repetível).
4. **Preparar as categorias:** sexo, estação e linhagem viraram números com OneHotEncoder.
5. **Treinar o modelo:** Regressão Linear Múltipla dentro de um pipeline (primeiro transforma as colunas, depois aplica a regressão).
6. **Avaliar:** erro medido com o MSE (erro quadrático médio) nos dados de teste.
7. **Visualizar:** gráfico de barras interativo (Plotly) com o peso previsto por idade, com colunas por linhagem, linhas por estação e cores por sexo.
8. **Prever cenários:** previsões de peso aos 42 dias para todas as combinações de sexo, linhagem e estação.

## Explicando os termos

- **Regressão Linear Múltipla:** técnica que prevê um número (aqui, o peso) a partir de várias variáveis (idade, sexo, estação e linhagem).
- **OneHotEncoder:** transforma categorias em colunas de 0 e 1, que o modelo consegue usar.
- **Pipeline:** junta as etapas (preparar os dados e treinar o modelo) em um único objeto.
- **Treino e teste:** o modelo aprende com 80% dos dados e é avaliado nos 20% que ele não viu.
- **MSE (erro quadrático médio):** mede o quanto as previsões se afastam dos valores reais. Quanto menor, melhor.

## Ferramentas

- **Código:** Python, Pandas, scikit-learn e Plotly, no Google Colab.
- **Ebook:** PowerPoint; imagens feitas com Lexica.art, Remove.bg e Showcode.
- **ChatGPT:** usei para corrigir erros e melhorar o código.

## Limitações e próximos passos

- O trabalho usa um único modelo (regressão linear) e uma única divisão entre treino e teste.
- Os dados da empresa não estão publicados, então o notebook não pode ser reproduzido por outras pessoas.

- [ ] Comparar com outros modelos de regressão
- [ ] Usar validação cruzada para avaliar o modelo com mais confiança
- [ ] Criar um arquivo de dados fictício, com as mesmas colunas, para o notebook rodar sem os dados da empresa

## Contato

- **LinkedIn:** [Dayane Teodoro](https://www.linkedin.com/in/dayaneteodoro/)
- **GitHub:** [Dayanebiaerafa](https://github.com/Dayanebiaerafa)
- **E-mail:** dayaneteodorob@outlook.com

💞 Feito com amor por Dayane Teodoro⁉ 
