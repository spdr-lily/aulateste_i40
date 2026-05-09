# Arquitetura de Sistemas para Indústria 4.0

Pipeline de dados em Python para integração de sensores IoT com modelos de Inteligência Artificial voltados para manutenção preditiva.

## Visão Geral

Este projeto demonstra uma arquitetura simplificada de um sistema de Indústria 4.0 utilizando:

- Simulação de ingestão de dados de sensores IoT
- Pipeline ETL para processamento de dados
- Integração com modelo de Machine Learning
- Inferência em tempo real para detecção de falhas
- Monitoramento contínuo do sistema

O objetivo principal é exemplificar como dados industriais podem ser coletados, processados e utilizados por modelos de IA para apoiar estratégias de manutenção preditiva.

---

## Tecnologias Utilizadas

- Python 3
- Pandas
- NumPy
- Scikit-learn

---

## Estrutura do Projeto

```bash
.
├── aulateste_i40.ipynb
└── README.md
```

---

## Fluxo da Arquitetura

O sistema segue o seguinte fluxo:

1. **Ingestão de Dados**
   - Simulação de sensores IoT enviando dados de temperatura e vibração.
   - Representação de leitura via broker MQTT.

2. **Pipeline ETL**
   - Recebimento e tratamento dos dados.
   - Normalização básica da temperatura.

3. **Modelo de Inteligência Artificial**
   - Treinamento de um modelo de regressão logística.
   - Classificação de falha iminente.

4. **Monitoramento Contínuo**
   - Processamento em loop contínuo.
   - Geração de alertas em tempo real.

---

## Funcionalidades

### Simulação de Sensores

O sistema gera dados simulados de:

- Temperatura (°C)
- Vibração (mm/s)

Exemplo:

```python
{
    'temperatura': 95.2,
    'vibracao': 7.8
}
```

---

### Pipeline de Dados

O pipeline realiza:

- Leitura dos dados
- Estruturação em DataFrame
- Normalização de variáveis
- Preparação para inferência do modelo

---

### Modelo de Machine Learning

O modelo utilizado é:

- Logistic Regression (`LogisticRegression`)

Objetivo:

- Prever possíveis falhas industriais com base nos dados dos sensores.

Saídas possíveis:

| Resultado | Significado |
|---|---|
| 0 | Operação normal |
| 1 | Falha iminente |

---

## Exemplo de Execução

```bash
--- Iniciando Sistema Indústria 4.0 ---
LOG: Recebendo dados do broker MQTT...
Dados: Temp=102.35°C | Status: ALERTA: Falha Iminente!
----------------------------------------
```

---

## Como Executar

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

### 2. Instale as dependências

```bash
pip install pandas numpy scikit-learn
```

### 3. Execute o notebook

Utilize:

- Jupyter Notebook
- VS Code
- Google Colab

Arquivo:

```bash
aulateste_i40.ipynb
```

---

## Conceitos Demonstrados

Este projeto aborda conceitos fundamentais de:

- Indústria 4.0
- Internet das Coisas (IoT)
- Data Pipeline
- ETL
- Machine Learning aplicado à indústria
- Manutenção preditiva
- Monitoramento em tempo real

---

## Possíveis Melhorias Futuras

- Integração real com MQTT
- Uso de Apache Kafka para streaming
- Persistência em banco de dados
- Dashboard em tempo real
- Deploy do modelo em API
- Monitoramento com Grafana e Prometheus
- Uso de modelos mais avançados de IA
- Integração com Apache Airflow

---

## Aplicações Reais

Esse tipo de arquitetura pode ser aplicado em:

- Linhas de produção industriais
- Monitoramento de máquinas
- Manutenção preditiva
- Smart factories
- Controle de qualidade
- Automação industrial

---

## Referências

- Scikit-learn Documentation
- Pandas Documentation
- NumPy Documentation
- Conceitos de Indústria 4.0 e IoT

---

## Licença

Este projeto possui finalidade acadêmica e educacional.
