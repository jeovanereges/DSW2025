# DataCoin
Conjunto de dados estruturado com informações históricas do par BTC-USD, abrangendo o período de janeiro de 2017 a maio de 2025. O repositório inclui o _dataset_ final em formato `.csv`, bem como o código-fonte em Python responsável pela extração, agregação, enriquecimento e exportação dos dados, utilizando a biblioteca _yfinance_ para acesso à API pública do Yahoo Finance.

---
## 📚 Conteúdo

- `DataCoin.csv`: base final com 157 registros mensais consolidados do par BTC-USD, contendo preços agregados (abertura, máxima, mínima e fechamento), variação percentual mensal e colunas temporais derivadas (mês, ano e número do mês).
  
- `DSW2025.ipynb`: _script_ Python modularizado e comentado, responsável pela coleta, processamento e enriquecimento do _dataset_. Utiliza a biblioteca _yfinance_ para acessar a API pública do Yahoo Finance, realizando etapas como extração diária, agregação mensal, cálculo da variação percentual, e geração de marcadores temporais (mês, ano, número do mês), exportando o resultado final em formato `.csv`.
  
- `README.md`: instruções de uso.
---
## Como usar 🚀
### 1. Clonar o repositório
git clone https://github.com/jeovanereges/DSW2025.git
cd DSW2025
### 2. Instalar as dependências
- pip install yfinance --upgrade --no-cache-dir
- pip install pandas
- pip install numpy

### 3. Personalização do script ⚙️
Você pode editar o intervalo de datas e o ativo financeiro diretamente no _script_ **DSW2025.ipynb**, ajustando os parâmetros de `início`, `fim` e `símbolo` (_start, end_ e _ticker_) para personalizar a coleta de dados via _yfinance_.

### 4. Formato de saída 📦
O arquivo final `.csv` contém as seguintes colunas: `Date`, `Open`, `High`, `Low`, `Close`, `Resultado%`, `Mes`, `Ano` e `No.Mes`, representando respectivamente a data de referência, os preços agregados mensais do BTC-USD, a variação percentual do fechamento em relação ao mês anterior e as informações temporais derivadas.

### Licença 📄
Este projeto está licenciado sob a Licença MIT. Você pode utilizá-lo, copiá-lo e modificá-lo livremente, desde que a devida atribuição ao autor original seja mantida.

### Contribuições 🤝
Sinta-se à vontade para abrir _issues_, enviar _pull requests_ ou sugerir melhorias na estrutura do código e na expansão do _dataset_ para outros ativos financeiros, diferentes intervalos de tempo ou agregações alternativas.
