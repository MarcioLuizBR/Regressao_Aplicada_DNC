# 🏗️ Regressão Aplicada à Engenharia de Materiais
## Predição da Resistência do Concreto com Modelos Preditivos

## 📋 Sobre o Projeto

Este repositório contém o desenvolvimento de modelos de regressão para **prever a resistência à compressão do concreto** com base em variáveis como cimento, água, idade e outros componentes. O projeto foi desenvolvido como parte do curso da **DNC (Escola de Negócios e Tecnologia)** e demonstra como a ciência de dados pode ser aplicada na engenharia civil para otimizar a produção e garantir a qualidade do concreto.

## 🎯 Contexto e Motivação

No setor da **engenharia civil**, especialmente na indústria de construção de infraestrutura urbana e obras de grande porte, prever com precisão a resistência do concreto é um desafio central para:

- ✅ **Garantir segurança** estrutural nas construções
- 💰 **Reduzir custos** com testes e materiais
- 🌱 **Melhorar a sustentabilidade** dos projetos
- 📊 **Ajustar a produção** conforme parâmetros desejados
- 🔬 **Economizar** com estudos e coleta de amostras
- 📈 **Melhorar o planejamento** de substituição e manutenção

## 🛠️ Tecnologias Utilizadas

- **Python** - Linguagem principal
- **Pandas** - Manipulação e análise de dados
- **NumPy** - Computação numérica
- **Scikit-learn** - Machine learning e modelagem
- **Matplotlib/Seaborn** - Visualização de dados
- **Jupyter Notebook** - Ambiente de desenvolvimento interativo

## 📊 Dataset

O conjunto de dados contém informações detalhadas sobre a composição de diferentes amostras de concreto e sua respectiva **resistência à compressão**. Cada registro representa uma mistura de concreto com:

**Variáveis disponíveis:**
- **Cimento** - Quantidade de cimento utilizada
- **Escória de Alto Forno** - Quantidade de escória
- **Cinza Volante** - Quantidade de cinza volante
- **Água** - Quantidade de água na mistura
- **Superplastificante** - Aditivo superplastificante
- **Agregado Graúdo** - Quantidade de agregado graúdo
- **Agregado Miúdo** - Quantidade de agregado miúdo
- **Idade** - Idade da amostra em dias
- **Strength Category** - Categoria de resistência (Alta, Média, Baixa)
- **Concrete compressive strength** - Variável alvo (resistência à compressão)

## 🎯 Etapas de Desenvolvimento

### **Etapa 01: Análise Exploratória de Dados (EDA)**

**Objetivo**: Entender os dados e identificar padrões visuais através de análise estatística e visual.

**Questões investigadas:**
1. **Quais fatores estão mais associados à resistência do concreto?**
   - Análise de correlação entre variáveis numéricas
   - Matrizes de correlação e gráficos de dispersão

2. **Como a quantidade de cimento afeta a resistência?**
   - Gráfico de dispersão: Cimento vs Resistência à compressão

3. **Como a água afeta a resistência do concreto?**
   - Gráfico de dispersão: Água vs Resistência à compressão

4. **Qual é a resistência média por categoria de força?**
   - Análise por Strength Category (Alta, Média, Baixa)
   - Gráficos de barras horizontais

### **Etapa 02: Tratamento de Dados**

**Preparação do dataset para modelagem:**

1. **Verificação da qualidade dos dados**
   - Identificação de valores nulos e ausentes
   - Análise da consistência dos dados

2. **Codificação de variáveis categóricas**
   - Aplicação de One-Hot Encoding na variável `Strength Category`
   - Remoção da primeira categoria (`drop_first=True`) para evitar multicolinearidade

3. **Tratamento de valores ausentes**
   - Limpeza e preparação final do dataset

### **Etapa 03: Construção e Avaliação de Modelos**

**Modelos implementados:**

1. **Random Forest Regressor**
   - Modelo principal para predição da resistência
   - Avaliação com métricas R² e MAE

2. **Regressão Linear**
   - Modelo de comparação
   - Avaliação com métricas R² e MAE

**Métricas de avaliação:**
- **R² (Coeficiente de Determinação)** - Qualidade do ajuste
- **MAE (Mean Absolute Error)** - Erro médio absoluto

### **Etapa 04: Predição de Resultados**

**Análise de importância das variáveis** e predição para uma amostra específica:

```python
# Exemplo de predição
Cimento: 550
Escória de Alto Forno: 150
Cinza Volante: 0
Água: 180
Superplastificante: 2.5
Agregado Graúdo: 1000
Agregado Miúdo: 700
Idade: 25
```

## 📁 Estrutura do Projeto

```
Regressao_Aplicada_DNC/
│
├── data/
│   └── dados_concreto_-_Sheet1.csv    # Dataset principal
│
├── notebooks/
│   └── Regressao_Aplicada_DNC.ipynb
│
├── LICENSE 
├── requirements.txt                   # Dependências
└── README.md                         # Este arquivo
```

## 🚀 Como Executar

### Pré-requisitos
- Python 3.8 ou superior
- Jupyter Notebook ou JupyterLab

### Instalação
1. Clone o repositório:
```bash
git clone https://github.com/MarcioLuizBR/Regressao_Aplicada_DNC.git
cd Regressao_Aplicada_DNC
```

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

3. Execute os notebooks na sequência:
```bash
jupyter notebook
```

## 📈 Principais Descobertas

### Correlações Identificadas
- **Cimento**: [Correlação com resistência]
- **Água**: [Impacto na resistência]
- **Idade**: [Influência temporal na resistência]
- **Superplastificante**: [Efeito dos aditivos]

### Performance dos Modelos
- **Random Forest Regressor**
  - R²: [0.8177]
  - MAE: [5.01] MPa

- **Regressão Linear**
  - R²: [0.5193]
  - MAE: [9.34] MPa

### Importância das Variáveis
- Ranking das variáveis mais importantes para predição
- Insights sobre otimização da composição do concreto

## 🔍 Aplicações Práticas

Este modelo pode ser utilizado para:

- **Otimização de misturas** de concreto antes da produção
- **Controle de qualidade** em usinas de concreto
- **Redução de custos** com testes laboratoriais
- **Planejamento de obras** com diferentes especificações de resistência
- **Desenvolvimento** de novas formulações de concreto

## 🤝 Contribuições

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do projeto
2. Crie uma branch (`git checkout -b feature/improvement`)
3. Commit suas mudanças (`git commit -m 'Add improvement'`)
4. Push para a branch (`git push origin feature/improvement`)
5. Abra um Pull Request

## 👨‍💻 Autor

**Márcio Luiz**
- GitHub: [@MarcioLuizBR](https://github.com/MarcioLuizBR)
- Linkedin: [Marcio Luiz](https://www.linkedin.com/in/marcioluiz-multicloud/)

## 🎓 Agradecimentos

- **DNC - Escola de Negócios e Tecnologia** pelo curso e orientação
- Comunidade de ciência de dados e engenharia de materiais
- Desenvolvedores das bibliotecas Python utilizadas

## 📚 Referências

- Documentação Scikit-learn para Random Forest e Regressão Linear
- Literatura técnica sobre resistência à compressão do concreto
- Boas práticas em ciência de dados aplicada à engenharia

---

⭐ **Se este projeto foi útil para você, considere dar uma estrela no repositório!**

🏗️ **Para engenheiros e cientistas de dados interessados em aplicações práticas na construção civil**