# Modelo KNN para Previsão de Taxa de Engajamento no Instagram

Este projeto implementa um modelo de regressão KNN (K-Nearest Neighbors) para prever a taxa de engajamento de influenciadores no Instagram com base em diferentes métricas.

## 📋 Pré-requisitos

- Python 3.6+
- Bibliotecas necessárias (instaláveis via pip):
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

## 🚀 Como executar

1. Clone este repositório ou baixe os arquivos do projeto

2. Instale, crie e entre num ambiente virtual:
```bash
python3 -m venv venv .
. ./venv/bin/activate
```
3. Instale as dependências:
```bash
pip install -r requirements.txt
```
4. Execute o Jupyter Notebook:
```bash
jupyter notebook
```

5. Abra o arquivo knn.ipynb no navegador

### Obs: Pode usar o vsCode se preferir, nesse caso instale a extenção Jupyter e configure o kernel para rodar com o python instalado no ambiente virtual (venv/bin/python).

## 📊 Sobre o Modelo

O modelo utiliza as seguintes features para fazer a previsão:
- Número de posts
- Número de seguidores 
- Média de likes
- Média de likes em posts recentes
- Taxa de engajamento em 60 dias

### Pipeline do Modelo
1. Carregamento e pré-processamento dos dados
2. Normalização das features usando StandardScaler
3. Divisão em conjuntos de treino (80%) e teste (20%)
4. Grid Search para encontrar o melhor valor de K
5. Treinamento do modelo KNN com o K otimizado
6. Avaliação usando métricas como MAE, MSE, RMSE e R²

## 📈 Resultados

O modelo apresentou excelentes resultados após a normalização dos dados:
- R² score: 0.96
- Baixo erro médio absoluto (MAE)
- Alta correlação entre valores previstos e reais

## 🔍 Estrutura do Projeto

```
.
├── knn.ipynb       # Notebook principal com o código do modelo
├── top_insta_influencers_data.csv    # Dataset
├── requirements.txt         # Dependências do projeto
└── README.md               # Este arquivo
```

## 📝 Notas Importantes

- A normalização dos dados é crucial para o desempenho do modelo
- O melhor valor de K encontrado foi 3
- O modelo apresenta performance significativamente melhor (R² 0.96) com dados normalizados em comparação com dados não normalizados (R² 0.46)

## 👥 Contribuições

Contribuições são bem-vindas! Para contribuir:
1. Faça um fork do projeto
2. Crie uma branch para sua feature
3. Commit suas mudanças
4. Push para a branch
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT.

## ✉️ Contato

Para dúvidas ou sugestões, por favor abra uma issue no repositório.