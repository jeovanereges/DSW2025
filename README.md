# DataCoin 📊

Conjunto de dados estruturado com informações históricas do par **BTC-USD**, abrangendo o período de **janeiro de 2017 a maio de 2025**. O repositório inclui o _dataset_ final em formato `.csv`, bem como o código-fonte em Python responsável pela extração, agregação, enriquecimento e exportação dos dados, utilizando a biblioteca `yfinance` para acesso à API pública do Yahoo Finance.

---

## 📚 Conteúdo

- `DataCoin.csv`: base final com **157 registros mensais consolidados** do par BTC-USD, contendo:
  - Preços agregados (Abertura, Máxima, Mínima e Fechamento)
  - Variação percentual mensal
  - Colunas temporais derivadas (Mês, Ano, Número do Mês)
  
- `DSW2025.ipynb`: _script_ Python modularizado e comentado, responsável pela coleta, processamento e enriquecimento do _dataset_.  
Utiliza a biblioteca `yfinance` para acessar a API pública do Yahoo Finance, realizando etapas como:
  - Extração diária
  - Agregação mensal
  - Cálculo da variação percentual
  - Geração de marcadores temporais
  - Exportação em formato `.csv`
  
- `README.md`: instruções e detalhes sobre o projeto.

---

## 🔍 Como Usar

### 1️⃣ Clonar o Repositório 📦

git clone https://github.com/jeovanereges/DSW2025.git
cd DSW2025

### 2️⃣ Instalar as Dependências 🛠️
pip install yfinance --upgrade --no-cache-dir
pip install pandas
pip install numpy

### 3️⃣ Personalizar o Script ⚙️
Edite diretamente no **DSW2025.ipynb** os parâmetros de data e ativo financeiro:
- start, end → intervalo de tempo desejado
- ticker → código do ativo no Yahoo Finance (ex: "BTC-USD")

### 📤 Formato de Saída
O arquivo .csv final contém as seguintes colunas:

| Coluna       | Descrição                                                    |
| ------------ | ------------------------------------------------------------ |
| `Date`       | Data de referência mensal                                    |
| `Open`       | Preço de abertura (média mensal)                             |
| `High`       | Preço mais alto do mês                                       |
| `Low`        | Preço mais baixo do mês                                      |
| `Close`      | Preço de fechamento (média mensal)                           |
| `Resultado%` | Variação percentual do fechamento em relação ao mês anterior |
| `Mes`        | Nome do mês                                                  |
| `Ano`        | Ano correspondente                                           |
| `No.Mes`     | Número do mês (1 a 12)                                       |

### 📄 Licença
Este projeto está licenciado sob a Licença MIT. Sinta-se livre para usar, copiar e modificar o conteúdo, mantendo a atribuição ao autor original.

### 🤝 Contribuições
Sugestões, correções e melhorias são bem-vindas!
Você pode abrir issues, enviar pull requests ou contribuir com:

- Novos ativos financeiros
- Diferentes intervalos de tempo
- Estratégias alternativas de agregação de dados
