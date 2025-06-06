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
