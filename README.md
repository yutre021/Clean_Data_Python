# Clean_Data_Python
Here gonna show the concepts of cleaning Data in python


# Data Type Constraints and Cleaning (Restrições de Tipo de Dados e Limpeza)

In data cleaning and analysis, understanding and correctly applying data types is fundamental. Each piece of data has a specific nature (e.g., text, number, date) that dictates how it should be stored, processed, and validated. Defining and enforcing data type constraints ensures data quality and enables accurate computations and analyses.

---

## English Version

### Understanding Data Types

Data types classify the kind of values that can be stored in a variable or column, influencing how data is handled and what operations can be performed on it.

| Datatype    | Example                               | Python Data Type |
| :---------- | :------------------------------------ | :--------------- |
| **Text data** | First name, last name, address, etc.  | `str`            |
| **Integers** | Number of subscribers, products sold, etc. | `int`            |
| **Decimals** | Temperature, exchange rates, etc.     | `float`          |
| **Binary** | Is married, new customer (yes/no), etc. | `bool`           |
| **Dates** | Order dates, ship dates, etc.         | `datetime`       |
| **Categories**| Marriage status, gender, etc.         | `category`       |

* **Text data (Python `str`):**
    * **Explanation:** Represents sequences of characters. Examples include names, addresses, product descriptions, or any textual information. In Python, these are handled as strings. During data cleaning, ensuring consistent encoding (e.g., UTF-8) and handling special characters are common tasks.
* **Integers (Python `int`):**
    * **Explanation:** Represents whole numbers, typically used for counts or identifiers. For instance, the number of subscribers or products sold. In data cleaning, one might check for non-numeric values or out-of-range numbers in integer fields.
* **Decimals (Python `float`):**
    * **Explanation:** Represents numbers with fractional parts, used for measurements or monetary values. Examples include temperature readings or currency exchange rates. Cleaning decimal data often involves handling precision, rounding, or converting from string formats.
* **Binary (Python `bool`):**
    * **Explanation:** Represents values with two states, typically `True`/`False` or `1`/`0`. This can indicate a yes/no answer (e.g., "Is married," "new customer"). Data cleaning here might involve converting inconsistent textual representations (e.g., "Y", "N", "true", "false") into boolean types.
* **Dates (Python `datetime`):**
    * **Explanation:** Represents specific points in time, including dates and times. Examples include order dates or shipping dates. Data cleaning for dates is critical for time-series analysis and involves parsing various date formats, handling invalid dates, and ensuring consistent timezones.
* **Categories (Python `category`):**
    * **Explanation:** Represents a finite set of distinct values or labels. Examples include marriage status (single, married, divorced) or gender (male, female, non-binary). In Python, these can be stored as categorical types, which can be more memory-efficient than strings for repeated values and can assist in statistical analysis. Cleaning categorical data involves standardizing labels, handling typos, and managing unknown categories.

### Importance in Data Cleaning

Correctly identifying and enforcing data types is a fundamental step in data cleaning. Mismatched data types can lead to:
* **Errors in calculations:** Trying to perform arithmetic on text.
* **Incorrect sorting and filtering:** Dates sorted alphabetically instead of chronologically.
* **Inefficient storage:** Using strings for boolean values.
* **Issues with downstream analysis and machine learning models.**

Therefore, data type conversion and validation are crucial parts of the data cleaning process to ensure the integrity and usability of data.

---

## Versão em Português

# Restrições de Tipo de Dados e Limpeza

No contexto da limpeza e análise de dados, compreender e aplicar corretamente os tipos de dados é fundamental. Cada dado possui uma natureza específica (ex: texto, número, data) que dita como deve ser armazenado, processado e validado. Definir e impor restrições de tipo de dados garante a qualidade dos dados e possibilita cálculos e análises precisas.

---

## Versão em Português

### Compreendendo os Tipos de Dados

Tipos de dados classificam o tipo de valores que podem ser armazenados em uma variável ou coluna, influenciando como os dados são tratados e quais operações podem ser realizadas neles.

| Tipo de Dados | Exemplo                                 | Tipo de Dados Python |
| :------------ | :-------------------------------------- | :----------------- |
| **Dados de Texto** | Nome, sobrenome, endereço, etc.         | `str`              |
| **Inteiros** | Nº de assinantes, nº de produtos vendidos, etc. | `int`              |
| **Decimais** | Temperatura, taxas de câmbio, etc.      | `float`            |
| **Binário** | É casado, novo cliente (sim/não), etc.  | `bool`             |
| **Datas** | Datas de pedidos, datas de envio, etc.  | `datetime`         |
| **Categorias** | Estado civil, gênero, etc.              | `category`         |

* **Dados de Texto (Python `str`):**
    * **Explicação:** Representa sequências de caracteres. Exemplos incluem nomes, endereços, descrições de produtos ou qualquer informação textual. Em Python, são tratados como strings. Durante a limpeza de dados, garantir codificação consistente (ex: UTF-8) e lidar com caracteres especiais são tarefas comuns.
* **Inteiros (Python `int`):**
    * **Explicação:** Representa números inteiros, tipicamente usados para contagens ou identificadores. Por exemplo, o número de assinantes ou produtos vendidos. Na limpeza de dados, pode-se verificar valores não numéricos ou números fora do intervalo em campos inteiros.
* **Decimais (Python `float`):**
    * **Explicação:** Representa números com partes fracionárias, usados para medições ou valores monetários. Exemplos incluem leituras de temperatura ou taxas de câmbio. A limpeza de dados decimais frequentemente envolve lidar com precisão, arredondamento ou conversão de formatos de string.
* **Binário (Python `bool`):**
    * **Explicação:** Representa valores com dois estados, tipicamente `Verdadeiro`/`Falso` ou `1`/`0`. Isso pode indicar uma resposta sim/não (ex: "É casado", "novo cliente"). A limpeza de dados aqui pode envolver a conversão de representações textuais inconsistentes (ex: "S", "N", "verdadeiro", "falso") em tipos booleanos.
* **Datas (Python `datetime`):**
    * **Explicação:** Representa pontos específicos no tempo, incluindo datas e horas. Exemplos incluem datas de pedidos ou datas de envio. A limpeza de dados de datas é crítica para a análise de séries temporais e envolve a análise de vários formatos de data, o tratamento de datas inválidas e a garantia de fusos horários consistentes.
* **Categorias (Python `category`):**
    * **Explicação:** Representa um conjunto finito de valores ou rótulos distintos. Exemplos incluem estado civil (solteiro, casado, divorciado) ou gênero (masculino, feminino, não-binário). Em Python, estes podem ser armazenados como tipos categóricos, que podem ser mais eficientes em memória do que strings para valores repetidos e podem auxiliar na análise estatística. A limpeza de dados categóricos envolve padronizar rótulos, lidar com erros de digitação e gerenciar categorias desconhecidas.

### Importância na Limpeza de Dados

Identificar e impor corretamente os tipos de dados é uma etapa fundamental na limpeza de dados. Tipos de dados incompatíveis podem levar a:
* **Erros em cálculos:** Tentar realizar operações aritméticas em texto.
* **Classificação e filtragem incorretas:** Datas classificadas alfabeticamente em vez de cronologicamente.
* **Armazenamento ineficiente:** Usar strings para valores booleanos.
* **Problemas com análise e modelos de aprendizado de máquina posteriores.**

Portanto, a conversão e validação de tipos de dados são partes cruciais do processo de limpeza de dados para garantir a integridade e a usabilidade dos dados.



### Strings to integers

```python
# Import CSV file and output header
sales = pd.read_csv('sales.csv')
sales.head(2)
```

### Get in Data (Recebendo Dados)
```python
# Get data types of columns
sales.dtypes
```

### INFORMATION (Informação)

```python
# Get DataFrame information
sales.info()
```

### Function Describe (Função de escrita)

```python
df['marriage_status'].describe()
```

# Convert to categorical (Convertendo para Categórico)
```python

df["marriage_status"] = df["marriage_status"].astype('category')
df.describe()
```



# Handling Out of Range Data (Lidando com Dados Fora do Intervalo)

Out of range data refers to values that fall outside an expected or valid set of boundaries for a particular variable. These values are often errors (e.g., a person's age of 200, a temperature reading of -500°C) and can significantly distort analyses or lead to incorrect model predictions. Effectively dealing with such data is a crucial step in the data cleaning process.

---

## English Version

### Strategies for Managing Out of Range Data

When encountering data points that lie outside a plausible or defined range, several strategies can be employed, with the best choice often depending on the nature of the data, the business context, and the potential impact of the outlier.

1.  **Dropping data:**
    * **Explanation:** This involves removing the entire row or record that contains the out-of-range value. This method is simple but should be used cautiously, especially if the dataset is small or if dropping data leads to a significant loss of information or introduces bias. It's often suitable when the out-of-range data points are few and clearly erroneous, and their removal doesn't affect the overall representation.

2.  **Setting custom minimums and maximums:**
    * **Explanation:** This approach involves "clipping" or "winsorizing" the out-of-range values. Any value below a defined minimum is set to that minimum, and any value above a defined maximum is set to that maximum. This keeps the data point in the dataset but caps it within a sensible range, preventing extreme outliers from skewing results while retaining the data's presence.

3.  **Treat as missing and impute:**
    * **Explanation:** Out-of-range values can be treated as if they were missing data. Once marked as missing, imputation techniques can be applied. Imputation involves estimating and filling in the missing values based on other characteristics of the data (e.g., using the mean, median, mode, or more sophisticated machine learning models to predict the missing value). This method aims to retain the record while providing a reasonable substitute for the erroneous value.

4.  **Setting custom value depending on business assumptions:**
    * **Explanation:** In some cases, business domain knowledge provides insights into how out-of-range data should be handled. Instead of dropping or imputing statistically, a specific custom value might be assigned based on assumptions about the business process or the source of the data. For example, if a temperature sensor reports -500°C, a business rule might dictate setting it to the lowest possible valid temperature for that environment, or a specific indicator value for "sensor malfunction."

The choice among these methods depends on factors like the volume of out-of-range data, its suspected cause (e.g., data entry error, sensor malfunction, legitimate but extreme outlier), and the impact of each method on subsequent analysis or model performance.

---

## Versão em Português

# Lidando com Dados Fora do Intervalo

Dados fora do intervalo referem-se a valores que caem fora de um conjunto esperado ou válido de limites para uma determinada variável. Esses valores são frequentemente erros (ex: idade de uma pessoa de 200 anos, leitura de temperatura de -500°C) e podem distorcer significativamente análises ou levar a previsões incorretas de modelos. Lidar eficazmente com esses dados é uma etapa crucial no processo de limpeza de dados.

---

## Versão em Português

### Estratégias para Gerenciar Dados Fora do Intervalo

Ao encontrar pontos de dados que estão fora de um intervalo plausível ou definido, várias estratégias podem ser empregadas, sendo a melhor escolha frequentemente dependente da natureza dos dados, do contexto de negócio e do impacto potencial do valor atípico.

1.  **Remover dados (Dropping data):**
    * **Explicação:** Isso envolve a remoção de toda a linha ou registro que contém o valor fora do intervalo. Este método é simples, mas deve ser usado com cautela, especialmente se o conjunto de dados for pequeno ou se a remo remoção de dados levar a uma perda significativa de informações ou introduzir viés. É frequentemente adequado quando os pontos de dados fora do intervalo são poucos e claramente errôneos, e sua remoção não afeta a representação geral.

2.  **Definir mínimos e máximos personalizados (Setting custom minimums and maximums):**
    * **Explicação:** Esta abordagem envolve "cortar" ou "winsorizar" os valores fora do intervalo. Qualquer valor abaixo de um mínimo definido é ajustado para esse mínimo, e qualquer valor acima de um máximo definido é ajustado para esse máximo. Isso mantém o ponto de dado no conjunto de dados, mas o limita a um intervalo sensato, impedindo que outliers extremos distorçam os resultados, ao mesmo tempo que mantém a presença do dado.

3.  **Tratar como ausente e imputar (Treat as missing and impute):**
    * **Explicação:** Valores fora do intervalo podem ser tratados como se fossem dados ausentes. Uma vez marcados como ausentes, técnicas de imputação podem ser aplicadas. A imputação envolve estimar e preencher os valores ausentes com base em outras características dos dados (ex: usando a média, mediana, moda, ou modelos de aprendizado de máquina mais sofisticados para prever o valor ausente). Este método visa manter o registro enquanto fornece um substituto razoável para o valor errôneo.

4.  **Definir valor personalizado dependendo das suposições de negócio (Setting custom value depending on business assumptions):**
    * **Explicação:** Em alguns casos, o conhecimento do domínio de negócio fornece insights sobre como os dados fora do intervalo devem ser tratados. Em vez de remover ou imputar estatisticamente, um valor personalizado específico pode ser atribuído com base em suposições sobre o processo de negócio ou a origem dos dados. Por exemplo, se um sensor de temperatura reporta -500°C, uma regra de negócio pode ditar que ele seja ajustado para a temperatura válida mais baixa possível para aquele ambiente, ou um valor indicador específico para "mau funcionamento do sensor".

A escolha entre esses métodos depende de fatores como o volume de dados fora do intervalo, sua causa suspeita (ex: erro de entrada de dados, mau funcionamento do sensor, outlier legítimo, mas extremo) e o impacto de cada método na análise subsequente ou no desempenho do modelo.


# Common Data Types in Data Science (Tipos de Dados Comuns na Ciência de Dados)

In data science workflows, correctly identifying and managing data types is foundational. Manipulating and analyzing data with incorrect data types can lead to compromised analysis. It is crucial to always verify column data types (e.g., using `.dtypes` or `.info()` in Python) and convert them as needed before proceeding with any analysis.

---

## English Version

### Understanding Common Data Types

Data can be broadly categorized into different types, each suited for specific kinds of information and operations.

#### 1. Numeric Data Types

These types represent quantitative information that can be measured or counted.

* **Number of items purchased in a cart:**
    * **Explanation:** This is typically an integer, representing a count. It allows for arithmetic operations (e.g., summing up items across multiple carts).
* **Monthly salary received:**
    * **Explanation:** This would generally be a decimal or float type, as salaries often involve fractional amounts (e.g., currency values). It's suitable for financial calculations and aggregations.

#### 2. Text Data

Text data (or string data) represents qualitative information, such as names, descriptions, or addresses.

* **City of residence:**
    * **Explanation:** This is textual information. While it might represent a geographic location, the value itself is a string of characters (e.g., "New York," "London"). It's used for identification, categorization, and display.
* **Customer delivery address:**
    * **Explanation:** Addresses are complex strings of characters, often including numbers, letters, and special characters. They are treated as text and are crucial for logistical purposes.

#### 3. Date Data

Date data types represent specific points in time, ranging from dates to timestamps.

* **Customer birth dates:**
    * **Explanation:** Birth dates are specific calendar dates. Storing them as a date type allows for age calculations, chronological sorting, and time-based analysis (e.g., age distribution of customers).
* **Product order date:**
    * **Explanation:** The date a product was ordered is a specific point in time. Storing this as a date or datetime object enables tracking order timelines, calculating delivery durations, or analyzing sales trends over time.

### Importance of Correct Data Types

Assigning the correct data type to each column is vital because:
* It ensures data integrity and consistency.
* It allows for accurate mathematical and statistical operations.
* It optimizes memory usage and performance.
* It prevents errors in downstream analysis, visualizations, and machine learning models.

Data cleaning often involves careful inspection and conversion of data types to prepare the dataset for robust analysis.

---

## Versão em Português

# Tipos de Dados Comuns na Ciência de Dados

No fluxo de trabalho da ciência de dados, identificar e gerenciar corretamente os tipos de dados é fundamental. Manipular e analisar dados com tipos de dados incorretos pode levar a uma análise comprometida. É crucial sempre verificar os tipos de dados das colunas (ex: usando `.dtypes` ou `.info()` em Python) e convertê-los conforme necessário antes de prosseguir com qualquer análise.

---

## Versão em Português

### Compreendendo os Tipos de Dados Comuns

Os dados podem ser amplamente categorizados em diferentes tipos, cada um adequado para tipos específicos de informação e operações.

#### 1. Tipos de Dados Numéricos

Esses tipos representam informações quantitativas que podem ser medidas ou contadas.

* **Número de itens comprados em uma cesta:**
    * **Explicação:** Este é tipicamente um número inteiro, representando uma contagem. Permite operações aritméticas (ex: somar itens em vários carrinhos).
* **Salário recebido mensalmente:**
    * **Explicação:** Este seria geralmente um tipo decimal ou float, pois os salários frequentemente envolvem valores fracionados (ex: valores monetários). É adequado para cálculos financeiros e agregações.

#### 2. Dados de Texto

Dados de texto (ou dados de string) representam informações qualitativas, como nomes, descrições ou endereços.

* **Cidade de residência:**
    * **Explicação:** Esta é uma informação textual. Embora possa representar uma localização geográfica, o valor em si é uma string de caracteres (ex: "Nova York", "Londres"). É usado para identificação, categorização e exibição.
* **Endereço de entrega de um cliente:**
    * **Explicação:** Endereços são strings complexas de caracteres, frequentemente incluindo números, letras e caracteres especiais. São tratados como texto e são cruciais para fins logísticos.

#### 3. Dados de Data

Tipos de dados de data representam pontos específicos no tempo, desde datas até timestamps.

* **Datas de nascimento dos clientes:**
    * **Explicação:** Datas de nascimento são datas de calendário específicas. Armazená-las como um tipo de data permite cálculos de idade, classificação cronológica e análise baseada no tempo (ex: distribuição etária de clientes).
* **Data do pedido de um produto:**
    * **Explicação:** A data em que um produto foi pedido é um ponto específico no tempo. Armazenar isso como um objeto de data ou datetime permite rastrear cronogramas de pedidos, calcular durações de entrega ou analisar tendências de vendas ao longo do tempo.

### Importância dos Tipos de Dados Corretos

Atribuir o tipo de dado correto a cada coluna é vital porque:
* Garante a integridade e consistência dos dados.
* Permite operações matemáticas e estatísticas precisas.
* Otimiza o uso de memória e o desempenho.
* Previne erros em análises posteriores, visualizações e modelos de aprendizado de máquina.

A limpeza de dados frequentemente envolve a inspeção cuidadosa e a conversão de tipos de dados para preparar o conjunto de dados para uma análise robusta.



```python
# Print the information of ride_sharing
print(ride_sharing.info())

# Print summary statistics of user_type column
print(ride_sharing['user_type'].describe())

# Convert user_type from integer to category
ride_sharing['user_type_cat'] = ride_sharing['user_type'].astype('category')

# Write an assert statement confirming the change
assert ride_sharing['user_type_cat'].dtype == 'category'

# Print new summary statistics 
print(ride_sharing['user_type_cat'].describe())
```


# Handling Out of Range Data (Lidando com Dados Fora do Intervalo)

Out of range data refers to values that fall outside an expected or valid set of boundaries for a particular variable. These values are often errors (e.g., a person's age of 200, a temperature reading of -500°C) and can significantly distort analyses or lead to incorrect model predictions. Effectively dealing with such data is a crucial step in the data cleaning process.

---

## English Version

### Strategies for Managing Out of Range Data

When encountering data points that lie outside a plausible or defined range, several strategies can be employed, with the best choice often depending on the nature of the data, the business context, and the potential impact of the outlier.

1.  **Dropping data:**
    * **Explanation:** This involves removing the entire row or record that contains the out-of-range value. This method is simple but should be used cautiously, especially if the dataset is small or if dropping data leads to a significant loss of information or introduces bias. It's often suitable when the out-of-range data points are few and clearly erroneous, and their removal doesn't affect the overall representation.

2.  **Setting custom minimums and maximums:**
    * **Explanation:** This approach involves "clipping" or "winsorizing" the out-of-range values. Any value below a defined minimum is set to that minimum, and any value above a defined maximum is set to that maximum. This keeps the data point in the dataset but caps it within a sensible range, preventing extreme outliers from skewing results while retaining the data's presence.

3.  **Treat as missing and impute:**
    * **Explanation:** Out-of-range values can be treated as if they were missing data. Once marked as missing, imputation techniques can be applied. Imputation involves estimating and filling in the missing values based on other characteristics of the data (e.g., using the mean, median, mode, or more sophisticated machine learning models to predict the missing value). This method aims to retain the record while providing a reasonable substitute for the erroneous value.

4.  **Setting custom value depending on business assumptions:**
    * **Explanation:** In some cases, business domain knowledge provides insights into how out-of-range data should be handled. Instead of dropping or imputing statistically, a specific custom value might be assigned based on assumptions about the business process or the source of the data. For example, if a temperature sensor reports -500°C, a business rule might dictate setting it to the lowest possible valid temperature for that environment, or a specific indicator value for "sensor malfunction."

The choice among these methods depends on factors like the volume of out-of-range data, its suspected cause (e.g., data entry error, sensor malfunction, legitimate but extreme outlier), and the impact of each method on subsequent analysis or model performance.

---

## Versão em Português

# Lidando com Dados Fora do Intervalo

Dados fora do intervalo referem-se a valores que caem fora de um conjunto esperado ou válido de limites para uma determinada variável. Esses valores são frequentemente erros (ex: idade de uma pessoa de 200 anos, leitura de temperatura de -500°C) e podem distorcer significativamente análises ou levar a previsões incorretas de modelos. Lidar eficazmente com esses dados é uma etapa crucial no processo de limpeza de dados.

---

## Versão em Português

### Estratégias para Gerenciar Dados Fora do Intervalo

Ao encontrar pontos de dados que estão fora de um intervalo plausível ou definido, várias estratégias podem ser empregadas, sendo a melhor escolha frequentemente dependente da natureza dos dados, do contexto de negócio e do impacto potencial do valor atípico.

1.  **Remover dados (Dropping data):**
    * **Explicação:** Isso envolve a remoção de toda a linha ou registro que contém o valor fora do intervalo. Este método é simples, mas deve ser usado com cautela, especialmente se o conjunto de dados for pequeno ou se a remoção de dados levar a uma perda significativa de informações ou introduzir viés. É frequentemente adequado quando os pontos de dados fora do intervalo são poucos e claramente errôneos, e sua remoção não afeta a representação geral.

2.  **Definir mínimos e máximos personalizados (Setting custom minimums and maximums):**
    * **Explicação:** Esta abordagem envolve "cortar" ou "winsorizar" os valores fora do intervalo. Qualquer valor abaixo de um mínimo definido é ajustado para esse mínimo, e qualquer valor acima de um máximo definido é ajustado para esse máximo. Isso mantém o ponto de dado no conjunto de dados, mas o limita a um intervalo sensato, impedindo que outliers extremos distorçam os resultados, ao mesmo tempo que mantém a presença do dado.

3.  **Tratar como ausente e imputar (Treat as missing and impute):**
    * **Explicação:** Valores fora do intervalo podem ser tratados como se fossem dados ausentes. Uma vez marcados como ausentes, técnicas de imputação podem ser aplicadas. A imputação envolve estimar e preencher os valores ausentes com base em outras características dos dados (ex: usando a média, mediana, moda, ou modelos de aprendizado de máquina mais sofisticados para prever o valor ausente). Este método visa manter o registro enquanto fornece um substituto razoável para o valor errôneo.

4.  **Definir valor personalizado dependendo das suposições de negócio (Setting custom value depending on business assumptions):**
    * **Explanation:** Em alguns casos, o conhecimento do domínio de negócio fornece insights sobre como os dados fora do intervalo devem ser tratados. Em vez de remover ou imputar estatisticamente, um valor personalizado específico pode ser atribuído com base em suposições sobre o processo de negócio ou a origem dos dados. Por exemplo, se um sensor de temperatura reporta -500°C, uma regra de negócio pode ditar que ele seja ajustado para a temperatura válida mais baixa possível para aquele ambiente, ou um valor indicador específico para "mau funcionamento do sensor".

A escolha entre esses métodos depende de fatores como o volume de dados fora do intervalo, sua causa suspeita (ex: erro de entrada de dados, mau funcionamento do sensor, outlier legítimo, mas extremo) e o impacto de cada método na análise subsequente ou no desempenho do modelo.


```python
import pandas as pd
# Output Movies with rating > 5
movies[movies['avg_rating'] > 5]

# Drop values using filtering
movies = movies[movies['avg_rating'] <= 5]
# Drop values using .drop()
movies.drop(movies[movies['avg_rating'] > 5].index, inplace = True)
# Assert results
assert movies['avg_rating'].max() <= 5
```


```python
import datetime as dt
import pandas as pd
# Output data types
user_signups.dtypes
```

```
subscription_date object
user_name         object
Country           object
dtype:            object
```

```python
# Convert to date
user_signups['subscription_date'] = pd.to_datetime(user_signups['subscription_date']).dt.date
```

### Range Date

```python
# Drop values using filtering
user_signups = user_signups[user_signups['subscription_date'] < today_date]
# Drop values using .drop()
user_signups.drop(user_signups[user_signups['subscription_date'] > today_date].index, inplace = True)
```

### Hardcode dates with upper limit

```python
# Drop values using filtering
user_signups.loc[user_signups['subscription_date'] > today_date, 'subscription_date'] = today_date
# Assert is true
assert user_signups.subscription_date.max().date() <= today_date
```


```python
# Convert tire_sizes to integer
ride_sharing['tire_sizes'] = ride_sharing['tire_sizes'].astype('int')

# Set all values above 27 to 27
ride_sharing.loc[ride_sharing['tire_sizes'] > 27, 'tire_sizes'] = 27

ride_sharing['tire_sizes'] = ride_sharing['tire_sizes'].astype('category')

# Print tire size description
print(ride_sharing['tire_sizes'].describe())
```


```python
# Convert ride_date to date
ride_sharing['ride_dt'] = pd.to_datetime(ride_sharing['ride_date']).dt.date
# Save today's date
today = dt.date.today()

# Set all in the future to today's date
ride_sharing.loc[ride_sharing['ride_dt'] > today, 'ride_dt'] = today


# Print maximum of ride_dt column
print(ride_sharing['ride_dt'].max())
```

# Detecting Duplicate Rows in Data (Detectando Linhas Duplicadas em Dados)

Duplicate rows are a common issue in datasets and can lead to biased analyses, incorrect counts, and skewed model training if not handled properly. Identifying and managing these duplicates is a crucial step in the data cleaning process. In data manipulation libraries like Pandas in Python, the `.duplicated()` method is a powerful tool for this task.

---

## English Version

### Using the `.duplicated()` Method

The `.duplicated()` method is used to identify duplicate rows in a DataFrame (or similar tabular data structure). It returns a boolean Series indicating whether each row is a duplicate of a previous row.

#### Key Parameters:

* **`subset`**: This parameter allows you to specify a list of column names. The method will then check for duplication only across these specified columns. If `subset` is not provided, the method will consider all columns when checking for duplicates.
    * *Explanation:* This is useful when you consider a row a "duplicate" only if certain key fields (e.g., `first_name`, `last_name`, `email`) are identical, even if other non-key fields might differ.
* **`keep`**: This parameter determines which duplicate values (if any) to mark as `False` (not a duplicate) and which to mark as `True` (is a duplicate).
    * **`'first'`**: (Default) Marks duplicates as `True` except for the first occurrence.
    * **`'last'`**: Marks duplicates as `True` except for the last occurrence.
    * **`False` (or `all`)**: Marks *all* occurrences of a duplicate value as `True`. This is useful when you want to identify every instance of a duplicate.

### Importance in Data Cleaning:

By accurately identifying duplicate rows, data analysts and engineers can:
* Prevent double-counting in aggregations.
* Improve the accuracy of statistical models.
* Ensure the uniqueness of records where required.
* Reduce storage redundancy.

The `keep` parameter's flexibility allows for different strategies in handling duplicates, depending on whether you want to retain a specific instance or remove all instances of a duplicate.

---

## Versão em Português

# Detectando Linhas Duplicadas em Dados

Linhas duplicadas são um problema comum em conjuntos de dados e podem levar a análises tendenciosas, contagens incorretas e treinamento de modelos distorcidos se não forem tratadas adequadamente. Identificar e gerenciar essas duplicatas é uma etapa crucial no processo de limpeza de dados. Em bibliotecas de manipulação de dados como Pandas em Python, o método `.duplicated()` é uma ferramenta poderosa para essa tarefa.

---

## Versão em Português

### Usando o Método `.duplicated()`

O método `.duplicated()` é usado para identificar linhas duplicadas em um DataFrame (ou estrutura de dados tabular semelhante). Ele retorna uma Série booleana indicando se cada linha é uma duplicata de uma linha anterior.

#### Parâmetros Chave:

* **`subset`**: Este parâmetro permite especificar uma lista de nomes de colunas. O método verificará então a duplicação apenas nessas colunas especificadas. Se `subset` não for fornecido, o método considerará todas as colunas ao verificar duplicatas.
    * *Explicação:* Isso é útil quando você considera uma linha uma "duplicata" apenas se certos campos chave (ex: `first_name`, `last_name`, `address`) forem idênticos, mesmo que outros campos possam diferir.
* **`keep`**: Este parâmetro determina quais valores duplicados (se houver) marcar como `False` (não é uma duplicata) e quais marcar como `True` (é uma duplicata).
    * **`'first'`**: (Padrão) Marca as duplicatas como `True`, exceto a primeira ocorrência.
    * **`'last'`**: Marca as duplicatas como `True`, exceto a última ocorrência.
    * **`False` (ou `all`)**: Marca *todas* as ocorrências de um valor duplicado como `True`. Isso é útil quando você deseja identificar cada instância de uma duplicata.

### Importância na Limpeza de Dados:

Ao identificar com precisão as linhas duplicadas, analistas e engenheiros de dados podem:
* Prevenir dupla contagem em agregações.
* Melhorar a precisão dos modelos estatísticos.
* Garantir a unicidade dos registros quando necessário.
* Reduzir a redundância de armazenamento.

A flexibilidade do parâmetro `keep` permite diferentes estratégias no tratamento de duplicatas, dependendo se você deseja reter uma instância específica ou remover todas as instâncias de uma duplicata.

```python
# Column names to check for duplication
column_names = ['first_name','last_name','address']
duplicates = height_weight.duplicated(subset = column_names, keep = False)
```


# Treating Duplicate Values with Grouping and Aggregation (Tratando Valores Duplicados com Agrupamento e Agregação)

After identifying duplicate rows or values in a dataset, the next step in data cleaning is often to decide how to treat them. Instead of simply removing duplicates, which might lead to loss of valuable information, you might want to summarize or aggregate them. In data manipulation, particularly with libraries like Pandas in Python, the `.groupby()` and `.agg()` methods are powerful tools for consolidating duplicate information.

---

## English Version

### Consolidating Duplicates with `.groupby()` and `.agg()`

The `.groupby()` method allows you to group rows based on one or more column values, effectively bringing together all rows that share the same characteristics (which often include duplicates). Once grouped, the `.agg()` (aggregate) method is used to apply one or more functions to the groups, summarizing the data.

#### How it works:

1.  **`.groupby()` Method:**
    * **Purpose:** This method is used to split the DataFrame into groups based on some criterion. When dealing with duplicates, you would typically group by the columns that define the duplicate rows.
    * **Mechanism:** It creates a `GroupBy` object, which is an intermediate structure. It doesn't immediately perform any calculations but sets up the framework for applying aggregate functions.

2.  **`.agg()` Method:**
    * **Purpose:** This method is used to apply one or more aggregation functions (like `sum()`, `mean()`, `count()`, `first()`, `last()`, `min()`, `max()`, etc.) to the grouped data.
    * **Mechanism:** After grouping, `.agg()` computes a single result for each group, effectively consolidating the duplicate rows into a single, summarized row.

#### Example Scenario:

Imagine you have a DataFrame with duplicate entries for customer orders, but you want to consolidate them into a single record per customer, summing up quantities, for instance.

```python
import pandas as pd

data = {
    'customer_id': [1, 1, 2, 2, 3],
    'item': ['A', 'A', 'B', 'C', 'A'],
    'quantity': [10, 5, 20, 15, 8],
    'price': [100, 100, 50, 75, 120]
}
df = pd.DataFrame(data)
print("Original DataFrame:\n", df)

# Group by customer_id and item to consolidate duplicate entries, then sum quantities
# This effectively 'treats' duplicates by summarizing their numerical aspects
consolidated_df = df.groupby(['customer_id', 'item']).agg(
    total_quantity=('quantity', 'sum'),
    average_price=('price', 'mean'),
    num_entries=('customer_id', 'count') # Count how many original entries contributed to this consolidated row
).reset_index() # reset_index turns the groupby keys back into columns

print("\nConsolidated DataFrame:\n", consolidated_df)
```

- In this example, if customer 1 ordered item A twice, *groupby()* *.agg()* allows you to create a single entry for "customer 1, item A" with the total quantity and average price, effectively treating the duplicate entries by summarizing them. This approach is powerful for maintaining data integrity while resolving redundancy by deriving meaningful consolidated records.



### Versão em Português

### Tratando Valores Duplicados com Agrupamento e Agregação
* Após identificar linhas ou valores duplicados em um conjunto de dados, a próxima etapa na limpeza de dados é frequentemente decidir como tratá-los. Em vez de simplesmente remover duplicatas, o que pode levar à perda de informações valiosas, você pode querer resumi-las ou agregá-las. Na manipulação de dados, particularmente com bibliotecas como Pandas em Python, os métodos .groupby() e .agg() são ferramentas poderosas para consolidar informações duplicadas.

### Versão em Português
- Consolidando Duplicatas com `.groupby()` e `.agg()`
- O método .groupby() permite agrupar linhas com base em um ou mais valores de coluna, reunindo efetivamente todas as linhas que compartilham as mesmas características (que frequentemente incluem duplicatas). Uma vez agrupado, o método .agg() (agregar) é usado para aplicar uma ou mais funções aos grupos, resumindo os dados.

### Como funciona:
* Método `.groupby()`:

- Propósito: Este método é usado para dividir o DataFrame em grupos com base em algum critério. Ao lidar com duplicatas, você normalmente agruparia pelas colunas que definem as linhas duplicadas.
- Mecanismo: Ele cria um objeto GroupBy, que é uma estrutura intermediária. Não realiza imediatamente nenhum cálculo, mas configura a estrutura para aplicar funções de agregação.

* Método `.agg()`:

- Propósito: Este método é usado para aplicar uma ou mais funções de agregação (como `sum()`, `mean()`,` count()`, `first()`, `last()`, `min()`, `max()`, etc.) aos dados agrupados.
- Mecanismo: Após o agrupamento, `.agg()` calcula um único resultado para cada grupo, consolidando efetivamente as linhas duplicadas em uma única linha resumida.
- Cenário de Exemplo:
- Imagine que você tem um DataFrame com entradas duplicadas para pedidos de clientes, mas deseja consolidá-las em um único registro por cliente, somando as quantidades, por exemplo.


```python
import pandas as pd

data = {
    'customer_id': [1, 1, 2, 2, 3],
    'item': ['A', 'A', 'B', 'C', 'A'],
    'quantity': [10, 5, 20, 15, 8],
    'price': [100, 100, 50, 75, 120]
}
df = pd.DataFrame(data)
print("DataFrame Original:\n", df)

# Agrupa por customer_id e item para consolidar entradas duplicadas, então soma as quantidades
# Isso efetivamente 'trata' as duplicatas resumindo seus aspectos numéricos
consolidated_df = df.groupby(['customer_id', 'item']).agg(
    total_quantity=('quantity', 'sum'),
    average_price=('price', 'mean'),
    num_entries=('customer_id', 'count') # Conta quantas entradas originais contribuíram para esta linha consolidada
).reset_index() # reset_index transforma as chaves de agrupamento de volta em colunas

print("\nDataFrame Consolidado:\n", consolidated_df)
```

* Neste exemplo, se o cliente 1 pediu o item A duas vezes, groupby().agg() permite criar uma única entrada para "cliente 1, item A" com a quantidade total e o preço médio, tratando efetivamente as entradas duplicadas ao resumi-las. Essa abordagem é poderosa para manter a integridade dos dados, ao mesmo tempo que resolve a redundância, derivando registros consolidados significativos.


```python
# Find duplicates
duplicates = ride_sharing.duplicated(subset='ride_id', keep=False)

# Sort your duplicated rides
duplicated_rides = ride_sharing[duplicates].sort_values('ride_id')

# Print relevant columns of duplicated_rides
print(duplicated_rides[['ride_id', 'duration', 'user_birth_year']])
```


```python
# Drop complete duplicates from ride_sharing
ride_dup = ride_sharing.drop_duplicates()

# Create statistics dictionary for aggregation function
statistics = {'user_birth_year': 'min', 'duration': 'mean'}

# Group by ride_id and compute new statistics
ride_unique = ride_dup.groupby('ride_id').agg(statistics).reset_index()

# Find duplicated values again
duplicates = ride_unique.duplicated(subset = 'ride_id', keep = False)
duplicated_rides = ride_unique[duplicates == True]

# Assert duplicates are processed
assert duplicated_rides.shape[0] == 0
```


# Data Quality: Categories, Problems, Solutions, and Joins (Qualidade de Dados: Categorias, Problemas, Soluções e Junções)

Ensuring high data quality is paramount for reliable analysis and robust applications. This involves understanding common data types, identifying potential issues stemming from data entry or parsing, applying appropriate cleaning strategies, and effectively combining datasets using various join operations.

---

## English Version

### 1. Categories and Membership Constraints

Categorical data involves values that belong to a predefined, finite set of categories. These categories can often be represented numerically for easier processing, while retaining their original meaning.

| Type of data          | Example values            | Numeric representation |
| :-------------------- | :------------------------ | :--------------------- |
| **Marriage Status** | `unmarried`, `married`    | `0`, `1`               |
| **Household Income Category** | `0-20K`, `20-40K`, etc. | `0`, `1`, etc.         |
| **Loan Status** | `default`, `payed`, `no_loan` | `0`, `1`, `2`          |

* **Explanation:** These are examples where textual categories are mapped to discrete numerical values. This practice is common in data preparation, especially for machine learning models that prefer numerical inputs. The key is that the set of possible values for these categories is finite and well-defined.

### 2. Why Data Quality Problems Arise

Data quality issues, particularly concerning categorical data, can stem from various sources:

* **Data Entry Errors:** These occur when human input is inconsistent or incorrect.
    * **Free text:** Allows users to type anything, leading to typos, variations in spelling (e.g., "NY" vs. "New York"), or incorrect entries.
    * **Dropdowns:** While more controlled, dropdowns can still have issues if the predefined options are ambiguous, incomplete, or if users select the wrong option.
* **Parsing Errors:** These happen when data is extracted, transformed, or loaded, and the system fails to correctly interpret or standardize the data. This might occur when data is imported from different sources with varying formats.

### 3. How to Treat Data Quality Problems (Categories)

Addressing issues in categorical data requires specific strategies to ensure consistency and usability.

* **Dropping Data:**
    * **Explanation:** This involves removing rows or records that contain erroneous or unfixable categorical values. This is a drastic measure and should be used cautiously to avoid losing valuable information, especially if the number of problematic entries is high.
* **Remapping Categories:**
    * **Explanation:** This strategy involves standardizing inconsistent categories by mapping multiple variations of a category to a single, canonical value (e.g., mapping "NY", "New York", "N.Y." all to "New York"). This is crucial for consistency.
* **Inferring Categories:**
    * **Explanation:** When categorical values are missing or unclear, it might be possible to infer the correct category based on other available data points or patterns in the dataset. This often involves using statistical methods or machine learning models to predict the most likely category.

### 4. A Note on Joins

Joins are fundamental operations in data manipulation, particularly when combining data from different sources. They are essential for enriching datasets and establishing relationships.

* **Anti Joins:**
    * **Explanation:** An Anti Join identifies records that are present in one dataset but *not* in another. It's used to find mismatches or unique entries.
    * **Visual Representation:** If you have sets A and B, an Anti Join (A minus B) returns "What is in A and not in B."
* **Inner Joins:**
    * **Explanation:** An Inner Join combines rows from two datasets where there is a match in a specified common column(s). It returns only the records that exist in *both* datasets based on the matching condition.
    * **Visual Representation:** If you have sets A and B, an Inner Join returns "What is in both A and B."

### 5. Applying Joins: Examples with Blood Types

Let's illustrate join types with an example of blood types in `study_data` and `categories` datasets.

#### A Left Anti Join on Blood Types

* **Concept:** "What is in `study_data` only."
* **Example:** If `study_data` has blood types `A-`, `O-`, `AB+`, `A+`, `O+`, `B-`, and `Z+`, and `categories` has `A-`, `O-`, `AB+`, `A+`, `O+`, `B-`, `B+`, and `AB-`.
* **Result:** A left anti-join on `study_data` would return only the rows containing `Z+`, as `Z+` is present in `study_data` but not in `categories`.

#### An Inner Join on Blood Types

* **Concept:** "What is in `study_data` and `categories` only."
* **Example:** Using the same `study_data` and `categories` as above.
* **Result:** An inner join would return all the blood types that are common to both datasets: `A-`, `O-`, `AB+`, `A+`, `O+`, `B-`. It effectively returns the intersection of the two sets, excluding elements unique to either.

---

## Versão em Português

# Qualidade de Dados: Categorias, Problemas, Soluções e Junções

Garantir alta qualidade de dados é primordial para análises confiáveis e aplicações robustas. Isso envolve a compreensão de tipos de dados comuns, a identificação de problemas potenciais decorrentes de entrada ou parsing de dados, a aplicação de estratégias de limpeza apropriadas e a combinação eficaz de conjuntos de dados usando várias operações de junção.

---

## Versão em Português

### 1. Categorias e Restrições de Membro

Dados categóricos envolvem valores que pertencem a um conjunto finito e predefinido de categorias. Essas categorias podem frequentemente ser representadas numericamente para facilitar o processamento, mantendo seu significado original.

| Tipo de dados           | Valores de exemplo            | Representação numérica |
| :---------------------- | :-------------------------- | :--------------------- |
| **Estado Civil** | `solteiro`, `casado`        | `0`, `1`               |
| **Categoria de Renda Familiar** | `0-20K`, `20-40K`, etc.     | `0`, `1`, etc.         |
| **Status do Empréstimo**| `inadimplente`, `pago`, `sem_emprestimo` | `0`, `1`, `2`          |

* **Explicação:** São exemplos onde categorias textuais são mapeadas para valores numéricos discretos. Essa prática é comum na preparação de dados, especialmente para modelos de aprendizado de máquina que preferem entradas numéricas. O ponto chave é que o conjunto de valores possíveis para essas categorias é finito e bem definido.

### 2. Por que Problemas de Qualidade de Dados Surgem

Problemas de qualidade de dados, particularmente em relação a dados categóricos, podem surgir de várias fontes:

* **Erros de Entrada de Dados:** Ocorrem quando a entrada humana é inconsistente ou incorreta.
    * **Texto livre:** Permite que os usuários digitem qualquer coisa, levando a erros de digitação, variações na grafia (ex: "RJ" vs. "Rio de Janeiro") ou entradas incorretas.
    * **Listas suspensas (Dropdowns):** Embora mais controladas, as listas suspensas ainda podem apresentar problemas se as opções predefinidas forem ambíguas, incompletas ou se os usuários selecionarem a opção errada.
* **Erros de Parsing (Análise Sintática):** Acontecem quando os dados são extraídos, transformados ou carregados, e o sistema falha em interpretar ou padronizar corretamente os dados. Isso pode ocorrer quando os dados são importados de diferentes fontes com formatos variados.

### 3. Como Tratar Esses Problemas (Categorias)

Abordar problemas em dados categóricos requer estratégias específicas para garantir consistência e usabilidade.

* **Remoção de Dados (Dropping Data):**
    * **Explicação:** Envolve a remoção de linhas ou registros que contêm valores categóricos errôneos ou incorrigíveis. Esta é uma medida drástica e deve ser usada com cautela para evitar a perda de informações valiosas, especialmente se o número de entradas problemáticas for alto.
* **Remapeamento de Categorias (Remapping Categories):**
    * **Explicação:** Essa estratégia envolve padronizar categorias inconsistentes, mapeando múltiplas variações de uma categoria para um único valor canônico (ex: mapear "RJ", "Rio", "Rio de J." tudo para "Rio de Janeiro"). Isso é crucial para a consistência.
* **Inferência de Categorias (Inferring Categories):**
    * **Explicação:** Quando os valores categóricos estão ausentes ou são pouco claros, pode ser possível inferir a categoria correta com base em outros pontos de dados disponíveis ou padrões no conjunto de dados. Isso frequentemente envolve o uso de métodos estatísticos ou modelos de aprendizado de máquina para prever a categoria mais provável.

### 4. Uma Nota sobre Junções (Joins)

Junções são operações fundamentais na manipulação de dados, particularmente ao combinar dados de diferentes fontes. Elas são essenciais para enriquecer conjuntos de dados e estabelecer relacionamentos.

* **Anti Joins (Anti Junções):**
    * **Explicação:** Uma Anti Junção identifica registros que estão presentes em um conjunto de dados, mas *não* em outro. É usada para encontrar incompatibilidades ou entradas únicas.
    * **Representação Visual:** Se você tem os conjuntos A e B, uma Anti Junção (A menos B) retorna "O que está em A e não em B".
* **Inner Joins (Junções Internas):**
    * **Explicação:** Uma Junção Interna combina linhas de dois conjuntos de dados onde há uma correspondência em coluna(s) comum(ns) especificada(s). Ela retorna apenas os registros que existem em *ambos* os conjuntos de dados com base na condição de correspondência.
    * **Representação Visual:** Se você tem os conjuntos A e B, uma Junção Interna retorna "O que está em A e em B".

### 5. Aplicando Junções: Exemplos com Tipos Sanguíneos

Vamos ilustrar os tipos de junção com um exemplo de tipos sanguíneos em conjuntos de dados `study_data` e `categories`.

#### Uma Junção Anti Esquerda (Left Anti Join) em Tipos Sanguíneos

* **Conceito:** "O que está *apenas* em `study_data`."
* **Exemplo:** Se `study_data` tem tipos sanguíneos `A-`, `O-`, `AB+`, `A+`, `O+`, `B-` e `Z+`, e `categories` tem `A-`, `O-`, `AB+`, `A+`, `O+`, `B-`, `B+` e `AB-`.
* **Resultado:** Uma junção anti esquerda em `study_data` retornaria apenas as linhas contendo `Z+`, pois `Z+` está presente em `study_data` mas não em `categories`.

#### Uma Junção Interna (Inner Join) em Tipos Sanguíneos

* **Conceito:** "O que está *tanto* em `study_data` *quanto* em `categories`."
* **Exemplo:** Usando os mesmos `study_data` e `categories` acima.
* **Resultado:** Uma junção interna retornaria todos os tipos sanguíneos que são comuns a ambos os conjuntos de dados: `A-`, `O-`, `AB+`, `A+`, `O+`, `B-`. Ela efetivamente retorna a interseção dos dois conjuntos, excluindo elementos únicos de um ou de outro.
