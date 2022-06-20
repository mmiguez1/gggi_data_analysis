---
jupyter:
  colab:
    name: DataScience.ipynb
  kernelspec:
    display_name: Python 3
    name: python3
  language_info:
    name: python
  nbformat: 4
  nbformat_minor: 0
---

::: {.cell .markdown id="ePEU4f2ULkCq"}
# The Impact of Religion on The Gender Gap Index

**Maygan Miguez and Jaclyn Wilson**\
Data Science Tutorial

[Link to our GitHub
webpage](https://datasciencegendergapindex.github.io)
:::

::: {.cell .markdown id="ww7qbnqMp6mf"}
\#**I. Introduction**
:::

::: {.cell .markdown id="Aioh51fkrxzD"}
For centuries, religion has been an influential factor in the
development of human beliefs, social interactions, and cultural
differences. As politics, social issues, economic climates, and human
health conditions evolve, one notable aspect of life that remains the
same is religion.

Undoubtedly, religion is the strongest belief system that exists in the
world. Religion has the power to influence cultural beliefs of an entire
city, nation, or continent. Every religion plays an important role in
the development of self-identity and morals on the individual level,
which expands into social norms, government policies, and community
ethics on the societial level.

Thus, a major religion can impact the social constructs of a country,
including attitudes towards different genders. A key metric of a
country\'s attitude towards the roles of men and women is the size of
its gender gap. A large gender gap may indicate that a country\'s
policies, societal norms, and opportunities are less advantageous for
women. A small gender gap may indicate that a country\'s policies,
societal norms, and opportunties are more equally advantageous to women
and men.
:::

::: {.cell .markdown id="GPvgTyR53bDw"}
## `<u>`{=html}`<b>`{=html}Project Goals`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="WVUC7EdIvrrE"}
The goal of this project is to investigate and determine how a
country\'s major religion(s) impact the size of its gender gap in terms
of health, education, economics, and politics.

`<u>`{=html}Three main questions that this project aims to answer
are:`</u>`{=html}\
**1. How does religion impact a country\'s gender gap subindex scores in
terms of health, education, economics, and politics?**

**2. Are particular major religions related to a lower overall gender
gap index score?**

**3. Can we predict how a country\'s gender gap index score will change
over time based on the prediction of its future major religion?**
:::

::: {.cell .markdown id="eoRTpYUF3f5a"}
## `<u>`{=html}`<b>`{=html}Project Datasets`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="f9T9sXqVMAZd"}
#### We are working with two datasets in this project:

1.  [The Global Gender Gap
    Index](https://www.weforum.org/reports/ab6795a1-960c-42b2-b3d5-587eccda6023)\
    The Global Gender Gap Index benchmarks the evolution of gender-based
    gaps among four key dimensions (Economic Participation and
    Opportunity, Educational Attainment, Health and Survival, and
    Political Empowerment) and tracks progress towards closing these
    gaps over time.

2.  [The Religious Composition By
    Country](https://www.pewforum.org/2015/04/02/religious-projection-table/2010/number/all/)\
    The Religious Composition By Country dataset from Pew Research
    Center details the estimated religious composition of 198 countries
    and territories from 2010 to 2050. The dataset also divides the
    world into six major regions and looks at how each region's
    religious composition is likely to change from 2010 to 2050,
    assuming that current patterns in migration and other demographic
    trends continue.
:::

::: {.cell .markdown id="yISmiJDV3jXU"}
## `<u>`{=html}`<b>`{=html}Measuring The Global Gender Gap`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="T7eFcmu5hDEg"}
The Global Gender Gap Index is a score ranging from 0 to 1 with 0 being
the lowest score and 1 being the highest score (indicating the gender
gap is closed). Each country\'s index score is measured on four
subindexes. Below is a description of how each of the four subindexes
(Economic Participation and Opportunity, Educational Attainment, Health
and Survival, and Political Empowerment) are measured by the World
Economic Forum to create the Global Gender Gap Index. More information
can be found at the [World Economic Forum\'s
website](https://reports.weforum.org/global-gender-gap-report-2018/measuring-the-global-gender-gap/).

\#\#\#\#`<u>`{=html}Economic Participation and Opportunity`</u>`{=html}\
This subindex contains three concepts: the participation gap, the
remuneration gap and the advancement gap.

1.  `<b>`{=html}Participation Gap`</b>`{=html}\
    This metric is captured using the difference between women and men
    in labour force participation rates.
2.  `<b>`{=html}Remuneration Gap`</b>`{=html}\
    This metric is captured through a hard data indicator (ratio of
    estimated female-to-male earned income) and a qualitative indicator
    gathered through the World Economic Forum's annual Executive Opinion
    Survey (wage equality for similar work).\
3.  `<b>`{=html}Gap Between Advancement of Women and Men`</b>`{=html}\
    This metric is captured through two hard data statistics (the ratio
    of women to men among legislators, senior officials and managers,
    and the ratio of women to men among technical and professional
    workers).

\#\#\#\#`<u>`{=html}Educational Attainment`</u>`{=html}\
This subindex captures the gap between women's and men's current access
to education through ratios of women to men in primary-, secondary- and
tertiary-level education. A longer-term view of the country's ability to
educate women and men in equal numbers is captured through the ratio of
the female literacy rate to the male literacy rate.

\#\#\#\#`<u>`{=html}Health and Survival`</u>`{=html} This subindex
provides an overview of the differences between women's and men's health
through the use of two indicators.

1.  `<b>`{=html}Sex Ratio at Birth`</b>`{=html}\
    This metric aims to capture the phenomenon of "missing women",
    prevalent in many countries with a strong son preference.\
2.  `<b>`{=html}Gap Between Women's and Men's Healthy Life
    Expectancy`</b>`{=html}\
    This measure provides an estimate of the number of years that women
    and men can expect to live in good health by taking into account the
    years lost to violence, disease, malnutrition and other relevant
    factors.

\#\#\#\#`<u>`{=html}Political Empowerment`</u>`{=html}\
This subindex measures the gap between men and women at the highest
level of political decision-making through the ratio of women to men in
ministerial positions and the ratio of women to men in parliamentary
positions. In addition, the World Economic Forum included the ratio of
women to men in terms of years in executive office (prime minister or
president) for the last 50 years. A clear drawback in this category is
the absence of any indicators capturing differences between the
participation of women and men at local levels of government. Should
such data become available at a globally comparative level in future
years, it will be considered for inclusion in the Index.
:::

::: {.cell .markdown id="E_CzVulOW81l"}
`<a id='external_factors'>`{=html}`</a>`{=html}

## `<u>`{=html}`<b>`{=html}External Factors That May Impact Our Model\'s Accuracy`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="guF0e2x2XeeR"}
While the Global Gender Gap Index computes a country\'s overall gender
gap score using the GGGI subindexes (economic, education, health and
political), our model does not explore additional factors that may
impact these subindexes other than religious groups. These additional
factors could include a country\'s GDP, population density, access to
natural resources, political freedom, level of corruption, development
of technology, etc. It is important that we recognize our model\'s
inability to account for these factors because we cannot make the
assumption that a country\'s religion is the sole cause of a higher or
lower GGGI score. In computing our model, we are making the assumption
that these additional factors other than religion do not exist.
:::

::: {.cell .markdown id="Wd1Dw9Yf3m8G"}
## `<u>`{=html}`<b>`{=html}Collaboration Plan`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="WNTBCcuY4K1p"}
For our collaboration plan, we met on zoom once a week to work on the
final project. We set up a google colab to work on our code together and
made updates through this shared google colab. From November 18 to
December 9, we developed our insights, visualizations, and presentation
for the final project and presentation.
:::

::: {.cell .markdown id="7fAfBRqVNYkQ"}
\#**II. ETL (Extraction, Transform, and Load)**
:::

::: {.cell .markdown id="X-WCn4HorkqJ"}
## `<u>`{=html}`<b>`{=html}Extraction`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="apY_UunO3CPk"}
#### `<u>`{=html}Extracting & Loading The Religious Composition By Country Data`</u>`{=html} {#extracting--loading-the-religious-composition-by-country-data}
:::

::: {.cell .markdown id="Yft4yNao3Hgo"}
We extracted the dataset .xlsx file from [Pew Research
Center](https://assets.pewresearch.org/wp-content/uploads/sites/11/2015/04/Religious_Composition_by_Country_2010-2050.xlsx)
and loaded it as a Pandas dataframe. This dataset includes the level of
specificity (1 = country, 2 = region, 3 = world), region ID number, year
(in 10-year increments from 2010-2050), region, country, and estimated
number of Christians, Muslims, Unaffiliated, Hindus, Buddhists, Folk
Religions, Other Religions, Jews, and all religions for each country.
:::

::: {.cell .code id="oYyORcbXx4og"}
``` {.python}
import pandas as pd
import re
import numpy as np
```
:::

::: {.cell .code id="78sZShOpuji8"}
``` {.python}
religion_df = pd.read_excel('https://assets.pewresearch.org/wp-content/uploads/sites/11/2015/04/Religious_Composition_by_Country_2010-2050.xlsx')
```
:::

::: {.cell .markdown id="Ee7EHukns_Yt"}
#### `<u>`{=html}Extracting & Loading The Global Gender Gap Index Data`</u>`{=html} {#extracting--loading-the-global-gender-gap-index-data}
:::

::: {.cell .markdown id="PuVhVQz33LIx"}
For the years 2010-2018, we extracted The Global Gender Gap Index data
.tsv file from Yongqiang Xiong\'s [Analysis of the Global Gender Gap
Index](https://github.com/yongqiangxiong/gggr_analysis) and loaded it as
a Pandas dataframe. For the years 2020-2021, we extracted The Global
Gender Gap Index data by converting the .pdf reports to .txt files. The
dataset includes the year, each country\'s Gender Gap Index rank and
score economic rank and score, education rank and score, health rank and
score, and political rank and score.

`<b>`{=html}NOTE:`</b>`{=html} We were unable to extract data for the
year 2019 because the World Economic Forum did not release a Global
Gender Gap Index Report for 2019.

\[All of the Global Gender Gap Index reports can be found
here\](<https://github.com/mmiguez1/mmiguez1.github.io/tree/main/The%20Global%20Gender%20Gap%20Index%20Reports%20(2019-2021)>.\
\[All Global Gender Gap Index text data can be found
here\](<https://github.com/mmiguez1/mmiguez1.github.io/tree/main/The%20Global%20Gender%20Gap%20Index%20Text%20(2019-2021)>.
:::

::: {.cell .code id="jRVm_qPA7acd"}
``` {.python}
# Extract 2010-2018 data from Yongqiang Xiong's Analysis of the Global Gender Gap Index and load as a Pandas dataframe
gggi_df = pd.read_csv('https://raw.githubusercontent.com/yongqiangxiong/gggr_analysis/b52f40026241444255d32483394f02913ab465b7/gggi-by-year.tsv', sep='\t')
gggi_df

# Extract 2020 data from txt files and load as a Pandas dataframe
gggi_econ_edu_2020_df = pd.read_csv('https://raw.githubusercontent.com/mmiguez1/mmiguez1.github.io/main/The%20Global%20Gender%20Gap%20Index%20Text%20(2019-2021)/WEF_GGGR_Economic_Education_2020.txt', delimiter=r"\s+", header=0, decimal=",")
gggi_health_pol_2020_df = pd.read_csv('https://raw.githubusercontent.com/mmiguez1/mmiguez1.github.io/main/The%20Global%20Gender%20Gap%20Index%20Text%20(2019-2021)/WEF_GGGR_Health_Political_2020.txt', delimiter=r"\s+", header=0, decimal=",")
gggi_overall_rank_2020_df = pd.read_csv('https://raw.githubusercontent.com/mmiguez1/mmiguez1.github.io/main/The%20Global%20Gender%20Gap%20Index%20Text%20(2019-2021)/WEF_GGGR_Overall_Rank_2020.txt', delimiter=r"\s+", header=0, decimal=",")

# Extract 2021 data from txt files and load as a Pandas dataframe
gggi_econ_edu_2021_df = pd.read_csv('https://raw.githubusercontent.com/mmiguez1/mmiguez1.github.io/main/The%20Global%20Gender%20Gap%20Index%20Text%20(2019-2021)/WEF_GGGR_Economic_Education_2021.txt', delimiter=r"\s+", header=0, decimal=",")
gggi_health_pol_2021_df = pd.read_csv('https://raw.githubusercontent.com/mmiguez1/mmiguez1.github.io/main/The%20Global%20Gender%20Gap%20Index%20Text%20(2019-2021)/WEF_GGGR_Health_Political_2021.txt', delimiter=r"\s+", header=0, decimal=",")
gggi_overall_rank_2021_df = pd.read_csv('https://raw.githubusercontent.com/mmiguez1/mmiguez1.github.io/main/The%20Global%20Gender%20Gap%20Index%20Text%20(2019-2021)/WEF_GGGR_Overall_Rank_2021.txt', delimiter=r"\s+", header=0, decimal=",")
```
:::

::: {.cell .markdown id="JzgfN_ppxnpB"}
## `<u>`{=html}`<b>`{=html}Transformation & Tidying`</b>`{=html}`</u>`{=html} {#transformation--tidying}
:::

::: {.cell .markdown id="8T_gh-S52oWo"}
#### `<u>`{=html}Tidying The Religious Composition Data`</u>`{=html}
:::

::: {.cell .markdown id="AaC7r5NgcWl1"}
First, we tidy the Religious Composition data. Since the \"row number\"
column is redundant, we use the .drop function to remove that column
from the Religious Composition data. We also convert each column\'s data
to its correct type.
:::

::: {.cell .code colab="{\"height\":684,\"base_uri\":\"https://localhost:8080/\"}" id="Y4e97kDw2jfi" outputId="479bcbc6-63b1-4f58-806b-7a9a0508517c"}
``` {.python}
# Tidy Religious Composition data
religion_df = religion_df.drop(['row_number'], axis=1)

dtype_cols = ['Christians', 'Muslims', 'Unaffiliated', 'Hindus', 'Buddhists', 'Folk Religions', 'Other Religions', 'Jews', 'All Religions']

# Remove spaces, commas, and non-numeric signs
religion_df[dtype_cols] = religion_df[dtype_cols].stack().str.replace(',','').unstack()
religion_df[dtype_cols] = religion_df[dtype_cols].stack().str.replace(' ','').unstack()
religion_df[dtype_cols] = religion_df[dtype_cols].stack().str.replace('<','').unstack()

# Convert columns to correct datatypes
religion_df[dtype_cols] = religion_df[dtype_cols].apply(lambda x: pd.to_numeric(x, downcast="integer", errors='coerce'))
religion_df["Christians"] = religion_df["Christians"].fillna(0)
religion_df = religion_df.astype({'Christians': 'int64'})

display(religion_df)
display(religion_df.dtypes)
```

::: {.output .display_data}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>level</th>
      <th>Nation_fk</th>
      <th>Year</th>
      <th>Region</th>
      <th>Country</th>
      <th>Christians</th>
      <th>Muslims</th>
      <th>Unaffiliated</th>
      <th>Hindus</th>
      <th>Buddhists</th>
      <th>Folk Religions</th>
      <th>Other Religions</th>
      <th>Jews</th>
      <th>All Religions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>3</td>
      <td>10000</td>
      <td>2010</td>
      <td>World</td>
      <td>All Countries</td>
      <td>2168330000</td>
      <td>1599700000</td>
      <td>1131150000</td>
      <td>1032210000</td>
      <td>487760000</td>
      <td>404690000</td>
      <td>58150000</td>
      <td>13860000</td>
      <td>6895850000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1001</td>
      <td>2010</td>
      <td>North America</td>
      <td>All Countries</td>
      <td>266630000</td>
      <td>3480000</td>
      <td>59040000</td>
      <td>2250000</td>
      <td>3860000</td>
      <td>1020000</td>
      <td>2200000</td>
      <td>6040000</td>
      <td>344530000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>1002</td>
      <td>2010</td>
      <td>Latin America-Caribbean</td>
      <td>All Countries</td>
      <td>531280000</td>
      <td>840000</td>
      <td>45390000</td>
      <td>660000</td>
      <td>410000</td>
      <td>10040000</td>
      <td>990000</td>
      <td>470000</td>
      <td>590080000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>1003</td>
      <td>2010</td>
      <td>Europe</td>
      <td>All Countries</td>
      <td>553280000</td>
      <td>43470000</td>
      <td>139890000</td>
      <td>1380000</td>
      <td>1350000</td>
      <td>870000</td>
      <td>890000</td>
      <td>1420000</td>
      <td>742550000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>1004</td>
      <td>2010</td>
      <td>Middle East-North Africa</td>
      <td>All Countries</td>
      <td>12710000</td>
      <td>317070000</td>
      <td>2100000</td>
      <td>1720000</td>
      <td>500000</td>
      <td>1060000</td>
      <td>230000</td>
      <td>5630000</td>
      <td>341020000</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1200</th>
      <td>1</td>
      <td>232</td>
      <td>2050</td>
      <td>Sub-Saharan Africa</td>
      <td>Zimbabwe</td>
      <td>16230000</td>
      <td>200000</td>
      <td>1430000</td>
      <td>10000</td>
      <td>10000</td>
      <td>930000</td>
      <td>50000</td>
      <td>10000</td>
      <td>18850000</td>
    </tr>
    <tr>
      <th>1201</th>
      <td>1</td>
      <td>237</td>
      <td>2050</td>
      <td>Sub-Saharan Africa</td>
      <td>South Sudan</td>
      <td>12750000</td>
      <td>1300000</td>
      <td>100000</td>
      <td>10000</td>
      <td>10000</td>
      <td>6930000</td>
      <td>10000</td>
      <td>10000</td>
      <td>21080000</td>
    </tr>
    <tr>
      <th>1202</th>
      <td>1</td>
      <td>238</td>
      <td>2050</td>
      <td>Latin America-Caribbean</td>
      <td>Curacao</td>
      <td>170000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>180000</td>
    </tr>
    <tr>
      <th>1203</th>
      <td>1</td>
      <td>239</td>
      <td>2050</td>
      <td>Latin America-Caribbean</td>
      <td>Sint Maarten</td>
      <td>60000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>60000</td>
    </tr>
    <tr>
      <th>1204</th>
      <td>1</td>
      <td>240</td>
      <td>2050</td>
      <td>Latin America-Caribbean</td>
      <td>Caribbean Netherlands</td>
      <td>20000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>10000</td>
      <td>20000</td>
    </tr>
  </tbody>
</table>
<p>1205 rows × 14 columns</p>
</div>
```
:::

::: {.output .display_data}
    level               int64
    Nation_fk           int64
    Year                int64
    Region             object
    Country            object
    Christians          int64
    Muslims             int64
    Unaffiliated        int32
    Hindus              int32
    Buddhists           int32
    Folk Religions      int32
    Other Religions     int32
    Jews                int32
    All Religions       int64
    dtype: object
:::
:::

::: {.cell .markdown id="g00WE9FE22Dg"}
#### `<u>`{=html}Tidying The Global Gender Gap Index Data`</u>`{=html}
:::

::: {.cell .markdown id="9ZpLjeUGckaH"}
To tidy the Global Gender Gap Index data for 2010-2018, we drop columns
of data we will not be using. Next, we rename column names to standard
names we will use moving forward and drop data for the years before 2010
since our Religious Composition data starts at 2010.
:::

::: {.cell .code id="k7yITvOdd5WX"}
``` {.python}
# Tidy GGGI data for 2010-2018
tidy_gggi_df = gggi_df.filter(["#year", "country", "ggi_rank", "ggi_score", "eco_rank", "eco_score", "edu_rank", "edu_score", "health_rank", "health_score", "pol_rank", "pol_score"], axis=1)
tidy_gggi_df.rename(columns={"country":'Country', '#year': 'Year', 'ggi_rank':'Rank', 'ggi_score':'Score', 'eco_rank':'Economic_Rank', 'eco_score':'Economic_Score', \
                             'edu_rank':'Education_Rank', 'edu_score':'Education_Score', 'health_rank':'Health_Rank', 'health_score':'Health_Score', \
                             'pol_rank':'Political_Rank', 'pol_score':"Political_Score"}, inplace=True)

tidy_ggi_df= tidy_gggi_df[~tidy_gggi_df['Year'].isin(['2006', '2007', '2008', '2009'])]
```
:::

::: {.cell .markdown id="zJa0xkG0d-QN"}
In the previous section, we loaded six different .txt files for the
2020-2021 Global Gender Gap Index data. Each .txt file contains economic
and education data, health and political data, or overall ranking and
scores per year. Each .txt file resulted in a dataframe that contains
two different columns for the two category rankings, scores, and
countries. Therefore, we must break each one into two dataframes, rename
columns to standard names, and concatenate the data to itself.
:::

::: {.cell .markdown id="_1K_LSzmhL_E"}
First, we separate our 2020 economic, education, health, and political
data into two dataframes and rename the columns to standard names.
:::

::: {.cell .code id="bqwgkZ-Bg6Qn"}
``` {.python}
# Separate 2020 Economic data into two dataframes & standardize column names
econ1_2020_df = gggi_econ_edu_2020_df.filter(['Country', 'Economic_Rank', 'Economic_Score_(0-1)'], axis = 1)
econ2_2020_df = gggi_econ_edu_2020_df.filter(['Country.1', 'Economic_Rank.1', 'Economic_Score_(0-1).1'], axis = 1)
econ2_2020_df = econ2_2020_df.rename(columns={'Country.1':'Country', 'Economic_Score_(0-1).1':'Economic_Score_(0-1)', 'Economic_Rank.1':'Economic_Rank'})

# Separate 2020 Education data into two dataframes & standardize column names
edu1_2020_df = gggi_econ_edu_2020_df.filter(['Country.2', 'Education_Rank', 'Education_Score_(0-1)'], axis=1)
edu1_2020_df = edu1_2020_df.rename(columns={'Country.2':'Country'})
edu2_2020_df = gggi_econ_edu_2020_df.filter(['Country.3', 'Education_Rank.1', 'Education_Score_(0-1).1'], axis=1)
edu2_2020_df = edu2_2020_df.rename(columns={'Country.3':'Country', 'Education_Score_(0-1).1':'Education_Score_(0-1)', 'Education_Rank.1':'Education_Rank'})

# Separate 2020 Health data into two dataframes & standardize column names
health1_2020_df = gggi_health_pol_2020_df.filter(['Country', 'Health/Survival_Rank', 'Health/Survival_Score_(0-1)'], axis = 1)
health2_2020_df = gggi_health_pol_2020_df.filter(['Country.1', 'Health/Survival_Rank.1', 'Health/Survival_Score_(0-1).1'], axis = 1)
health2_2020_df = health2_2020_df.rename(columns={'Country.1':'Country', 'Health/Survival_Score_(0-1).1':'Health/Survival_Score_(0-1)', 'Health/Survival_Rank.1':'Health/Survival_Rank'})

# Separate 2020 Political data into two dataframes & standardize column names
political1_2020_df = gggi_health_pol_2020_df.filter(['Country.2', 'Political_Rank', 'Political_Score_(0-1)'], axis=1)
political1_2020_df = political1_2020_df.rename(columns={'Country.2':'Country'})
political2_2020_df = gggi_health_pol_2020_df.filter(['Country.3', 'Political_Rank.1', 'Political_Score_(0-1).1'], axis=1)
political2_2020_df = political2_2020_df.rename(columns={'Country.3':'Country', 'Political_Score_(0-1).1':'Political_Score_(0-1)', 'Political_Rank.1':'Political_Rank'})
```
:::

::: {.cell .markdown id="pt-CSziDhRkR"}
We must add a year column to the new dataframes so we can merge based on
year later on.
:::

::: {.cell .code id="AsD7TVf3hl_5"}
``` {.python}
econ1_2020_df["Year"] = 2020
econ2_2020_df["Year"] = 2020
edu1_2020_df["Year"] = 2020
edu2_2020_df["Year"] = 2020
health1_2020_df["Year"] = 2020
health2_2020_df["Year"] = 2020
political1_2020_df["Year"] = 2020
political2_2020_df["Year"] = 2020
```
:::

::: {.cell .markdown id="g9p1slA4i6gV"}
Next, we separate our 2021 economic, education, health, and political
data into two dataframes and rename the columns to standard names.
:::

::: {.cell .code id="agryF7MNyA08"}
``` {.python}
# Separate 2021 Economic data into two dataframes & standardize column names
econ1_2021_df = gggi_econ_edu_2021_df.filter(['Country', 'Economic_Rank', 'Economic_Score_(0-1)'], axis=1)
econ2_2021_df = gggi_econ_edu_2021_df.filter(['Country.1', 'Economic_Rank.1', 'Economic_Score_(0-1).1'], axis=1)
econ2_2021_df = econ2_2021_df.rename(columns={'Country.1':'Country', 'Economic_Score_(0-1).1':'Economic_Score_(0-1)', 'Economic_Rank.1':'Economic_Rank'})

# Separate 2021 Education data into two dataframes & standardize column names
edu1_2021_df = gggi_econ_edu_2021_df.filter(['Country.2', 'Education_Rank', 'Education_Score_(0-1)'], axis=1)
edu1_2021_df = edu1_2021_df.rename(columns={'Country.2':'Country'})
edu2_2021_df = gggi_econ_edu_2021_df.filter(['Country.3', 'Education_Rank.1', 'Education_Score_(0-1).1'], axis=1)
edu2_2021_df = edu2_2021_df.rename(columns={'Country.3':'Country', 'Education_Score_(0-1).1':'Education_Score_(0-1)', 'Education_Rank.1':'Education_Rank'})

# Separate 2021 Health data into two dataframes & standardize column names
health1_2021_df = gggi_health_pol_2021_df.filter(['Country', 'Health/Survival_Rank', 'Health/Survival_Score_(0-1)'], axis = 1)
health2_2021_df = gggi_health_pol_2021_df.filter(['Country.1', 'Health/Survival_Rank.1', 'Health/Survival_Score_(0-1).1'], axis = 1)
health2_2021_df = health2_2021_df.rename(columns={'Country.1':'Country', 'Health/Survival_Score_(0-1).1':'Health/Survival_Score_(0-1)', 'Health/Survival_Rank.1':'Health/Survival_Rank'})

# Separate 2021 Political data into two dataframes & standardize column names
political1_2021_df = gggi_health_pol_2021_df.filter(['Country.2', 'Political_Rank', 'Political_Score_(0-1)'], axis=1)
political1_2021_df = political1_2021_df.rename(columns={'Country.2':'Country'})
political2_2021_df = gggi_health_pol_2021_df.filter(['Country.3', 'Political_Rank.1', 'Political_Score_(0-1).1'], axis=1)
political2_2021_df = political2_2021_df.rename(columns={'Country.3':'Country', 'Political_Score_(0-1).1':'Political_Score_(0-1)', 'Political_Rank.1':'Political_Rank'})
```
:::

::: {.cell .markdown id="-utmF3vEjqs3"}
Again, we add a year column to the new dataframes so we can merge based
on year later on.
:::

::: {.cell .code id="_8uPVc3qjLVL"}
``` {.python}
econ1_2021_df["Year"] = 2021
econ2_2021_df["Year"] = 2021
edu1_2021_df["Year"] = 2021
edu2_2021_df["Year"] = 2021
health1_2021_df["Year"] = 2021
health2_2021_df["Year"] = 2021
political1_2021_df["Year"] = 2021
political2_2021_df["Year"] = 2021
```
:::

::: {.cell .markdown id="F-aKWMpJj5lc"}
Next, we tidy the overall score and rankings data for 2020 and 2021 by
dropping columns with data we don\'t need. We then separate the data
into two dataframes and rename columns.
:::

::: {.cell .code id="a3sA2AxTkw_V"}
``` {.python}
# Separate Overall data for 2020 into two dataframes & standardize column names
gggi_overall_rank_2020_df = gggi_overall_rank_2020_df.drop(['Rank_change_(2018)', 'Score_change_(2018)', 'Score_change_(2006)', 'Rank_change_(2018).1', 'Score_change_(2018).1', 'Score_change_(2006).1'], axis=1)
overall1_2020_df = gggi_overall_rank_2020_df.filter(['Rank', 'Country', 'Score'], axis=1)
overall2_2020_df = gggi_overall_rank_2020_df.filter(['Rank.1', 'Country.1', 'Score.1'], axis=1)
overall2_2020_df = overall2_2020_df.rename(columns={'Rank.1':'Rank', 'Country.1':'Country', 'Score.1':'Score'})

# Separate Overall data for 2020 into two dataframes & standardize column names
gggi_overall_rank_2021_df = gggi_overall_rank_2021_df.drop(['Rank_change_(2020)', 'Score_change_(2020)', 'Score_Change_(2006)', 'Rank_Change_(2020)', 'Score_Change_(2020)', 'Score_Change_(2006).1', 'Score.1', 'Score.3'], axis=1)
overall1_2021_df = gggi_overall_rank_2021_df.filter(['Rank', 'Country', 'Score'], axis=1)
overall2_2021_df = gggi_overall_rank_2021_df.filter(['Rank.1', 'Country.1', 'Score.2'], axis=1)
overall2_2021_df = overall2_2021_df.rename(columns={'Rank.1':'Rank', 'Country.1':'Country', 'Score.2':'Score'})
```
:::

::: {.cell .markdown id="6VwdXAGhk2og"}
Again, we add a year column so we can merge based on year later on.
:::

::: {.cell .code id="E6hTITvxkp86"}
``` {.python}
overall1_2020_df["Year"] = 2020
overall2_2020_df["Year"] = 2020
overall1_2021_df["Year"] = 2021
overall2_2021_df["Year"] = 2021
```
:::

::: {.cell .markdown id="lhbnGmiZlAM5"}
After splitting up the data by category for each year (2020 and 2021),
we can concatenate the data for both years together into
category-specific dataframes.
:::

::: {.cell .code id="mr5efYxjgw03"}
``` {.python}
# Combine Economic, Education, Health, Political, and General data into one Dataframe per category
edu_df = pd.concat([edu1_2020_df, edu2_2020_df, edu1_2021_df, edu2_2021_df])
econ_df = pd.concat([econ1_2020_df, econ2_2020_df, econ1_2021_df, econ2_2021_df])
health_df = pd.concat([health1_2020_df, health2_2020_df, health1_2021_df, health2_2021_df])
political_df = pd.concat([political1_2020_df, political2_2020_df, political1_2021_df, political2_2021_df])
overall_df = pd.concat([overall1_2020_df, overall2_2020_df, overall1_2021_df, overall2_2021_df])
```
:::

::: {.cell .markdown id="Sxw38Z8Wladw"}
Now we can merge our new dataframes into one dataframe containing all
ranks and scores for 2020 and 2021.
:::

::: {.cell .code id="8-kFL2sKlZn2"}
``` {.python}
# Merge Dataframes for both years into one
econ_edu_df = edu_df.merge(econ_df)
health_pol_df = health_df.merge(political_df)
eehp_df = econ_edu_df.merge(health_pol_df)
gggi_20_21_df = eehp_df.merge(overall_df, on=["Year", "Country"])
```
:::

::: {.cell .markdown id="Vo-qsMbUmgIi"}
We can tidy our new dataframe containing all ranks and scores for
2020-2021 by renaming the columns to more concise names and making the
format of values consistent.
:::

::: {.cell .code id="UC-9aQ19lxPq"}
``` {.python}
# Rename columns to more concise names
gggi_20_21_df = gggi_20_21_df.rename(columns={"Economic_Score_(0-1)":"Economic_Score",'Education_Score_(0-1)':"Education_Score", 'Health/Survival_Score_(0-1)':"Health_Score", \
                                          'Health/Survival_Rank':'Health_Rank', 'Political_Score_(0-1)':"Political_Score"})

# Clean up data inconsistencies
gggi_20_21_df = gggi_20_21_df.replace({'-': np.nan, 'n/a': np.nan})
```
:::

::: {.cell .markdown id="x2wHDTrZtjJE"}
Now, we can merge the 2010-2018 data with the 2020-2021 to create our
final dataframe for the Global Gender Gap Index data and convert our
combined columns to their correct datatypes.
:::

::: {.cell .code colab="{\"height\":649,\"base_uri\":\"https://localhost:8080/\"}" id="1F3G8dEyonLp" outputId="4d87744d-1c5f-4fb2-801d-f5e285964089"}
``` {.python}
# Merge data for 2020-2021 with data for 2010-2018
all_gggi_df = pd.concat([tidy_gggi_df, gggi_20_21_df])

# Convert columns to correct datatypes
float_cols = ['Score', 'Economic_Score', 'Education_Score', 'Health_Score', 'Political_Score']
all_gggi_df[float_cols] = all_gggi_df[float_cols].apply(pd.to_numeric, axis=1)
all_gggi_df = all_gggi_df.astype({'Rank':'int64', 'Education_Rank':'int64', 'Health_Rank':'int64', 'Political_Rank':'int64'})

display(all_gggi_df)
display(all_gggi_df.dtypes)
```

::: {.output .display_data}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Year</th>
      <th>Country</th>
      <th>Rank</th>
      <th>Score</th>
      <th>Economic_Rank</th>
      <th>Economic_Score</th>
      <th>Education_Rank</th>
      <th>Education_Score</th>
      <th>Health_Rank</th>
      <th>Health_Score</th>
      <th>Political_Rank</th>
      <th>Political_Score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2006</td>
      <td>Albania</td>
      <td>61</td>
      <td>0.661</td>
      <td>38</td>
      <td>0.661</td>
      <td>58</td>
      <td>0.989</td>
      <td>110</td>
      <td>0.955</td>
      <td>105</td>
      <td>0.038</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2006</td>
      <td>Algeria</td>
      <td>97</td>
      <td>0.602</td>
      <td>103</td>
      <td>0.443</td>
      <td>84</td>
      <td>0.944</td>
      <td>78</td>
      <td>0.971</td>
      <td>98</td>
      <td>0.049</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2006</td>
      <td>Angola</td>
      <td>96</td>
      <td>0.604</td>
      <td>69</td>
      <td>0.587</td>
      <td>107</td>
      <td>0.779</td>
      <td>1</td>
      <td>0.980</td>
      <td>81</td>
      <td>0.070</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2006</td>
      <td>Argentina</td>
      <td>41</td>
      <td>0.683</td>
      <td>82</td>
      <td>0.551</td>
      <td>29</td>
      <td>0.997</td>
      <td>1</td>
      <td>0.980</td>
      <td>23</td>
      <td>0.204</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2006</td>
      <td>Australia</td>
      <td>15</td>
      <td>0.716</td>
      <td>12</td>
      <td>0.726</td>
      <td>1</td>
      <td>1.000</td>
      <td>57</td>
      <td>0.976</td>
      <td>32</td>
      <td>0.163</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>287</th>
      <td>2021</td>
      <td>Benin</td>
      <td>123</td>
      <td>0.653</td>
      <td>9</td>
      <td>0.814</td>
      <td>150</td>
      <td>0.733</td>
      <td>70</td>
      <td>0.973</td>
      <td>131</td>
      <td>0.093</td>
    </tr>
    <tr>
      <th>288</th>
      <td>2021</td>
      <td>Niger*</td>
      <td>138</td>
      <td>0.629</td>
      <td>82</td>
      <td>0.673</td>
      <td>151</td>
      <td>0.726</td>
      <td>124</td>
      <td>0.964</td>
      <td>97</td>
      <td>0.155</td>
    </tr>
    <tr>
      <th>289</th>
      <td>2021</td>
      <td>Yemen</td>
      <td>155</td>
      <td>0.492</td>
      <td>154</td>
      <td>0.282</td>
      <td>152</td>
      <td>0.717</td>
      <td>95</td>
      <td>0.968</td>
      <td>154</td>
      <td>0.001</td>
    </tr>
    <tr>
      <th>290</th>
      <td>2021</td>
      <td>Guinea</td>
      <td>118</td>
      <td>0.660</td>
      <td>6</td>
      <td>0.839</td>
      <td>153</td>
      <td>0.680</td>
      <td>109</td>
      <td>0.966</td>
      <td>96</td>
      <td>0.157</td>
    </tr>
    <tr>
      <th>291</th>
      <td>2021</td>
      <td>Chad</td>
      <td>148</td>
      <td>0.593</td>
      <td>73</td>
      <td>0.693</td>
      <td>155</td>
      <td>0.589</td>
      <td>81</td>
      <td>0.970</td>
      <td>119</td>
      <td>0.118</td>
    </tr>
  </tbody>
</table>
<p>2063 rows × 12 columns</p>
</div>
```
:::

::: {.output .display_data}
    Year                 int64
    Country             object
    Rank                 int64
    Score              float64
    Economic_Rank        int64
    Economic_Score     float64
    Education_Rank       int64
    Education_Score    float64
    Health_Rank          int64
    Health_Score       float64
    Political_Rank       int64
    Political_Score    float64
    dtype: object
:::
:::

::: {.cell .markdown id="K1u11C1iEj3p"}
#### `<u>`{=html}Checking Country Name Consistency`</u>`{=html}
:::

::: {.cell .markdown id="X9bkn0DXEvU_"}
In order to accurately combine the values from the Religous Composition
data with the Global Gender Gap Index data, we must correct any
inconsistent spelling or punctuation of country names. We can do this by
left joining our two datasets and creating a new dataframe with only the
left values to see which country names are different. Once we determine
which names need to be changed, we can replace them with their correct
spelling and punctuation.
:::

::: {.cell .code id="tECwxWmVEkfN"}
``` {.python}
#checks which rows were not merged from the all_gggi_df so that we can see which country names are different and need to be renamed
rename_df=pd.merge(all_gggi_df,religion_df[['Country']],on=['Country'],how="outer",indicator=True)
rename_df=rename_df[rename_df['_merge']=='left_only']
rename_df = rename_df.drop_duplicates(subset='Country', keep='first')

#Renaming some of the country
all_gggi_df = all_gggi_df.replace("Russian_Federation", "Russia")
all_gggi_df = all_gggi_df.replace(r'\_+', ' ', regex=True)
all_gggi_df = all_gggi_df.replace({'*':'', 'Korea Rep.':'South Korea', 'Kyrgyz Republic': 'Kyrgyzstan', 'Macedonia':'Republic of Macedonia', 'Russian Federation':'Russia', \
                                   'Slovak Republic':'Slovakia', 'Macedonia,FYR':'Republic of Macedonia', 'Brunei Darussalam':'Brunei', 'Lao PDR':'Laos', \
                                   'Bosnia and Herzegovina':'Bosnia-Herzegovina', 'Myanmar':'Burma (Myanmar)', 'Congo, Dem. Rep.':'Democratic Republic of the Congo', \
                                   'Zambia*': 'Zambia', 'Guyana*': 'Guyana', 'North Macedonia': 'Republic of Macedonia', 'United States of America':'United States', \
                                   'W. Sahara':'Western Sahara'})
```
:::

::: {.cell .markdown id="mOHHghALuBZq"}
\#**III. Exploratory Data Analysis (EDA)**
:::

::: {.cell .markdown id="8KXFIPTz1__X"}
For our exploratory data analysis of The Global Gender Gap Index and
Religious Composition data, we first get familiar with the summary
statistics of our data. Next, we analyze both datasets to gain general
answers to two of our project questions.
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\"}" id="JVPY8n2OapRQ" outputId="a84a7b0a-2f6c-483a-de3a-a3e0a08c5923"}
``` {.python}
%%time 
!apt install gdal-bin python-gdal python3-gdal   # Important library for many geopython libraries
!apt install python3-rtree   # Install rtree - Geopandas requirment
!pip install git+git://github.com/geopandas/geopandas.git   # Install Geopandas
!pip install descartes   # Install descartes - Geopandas requirment
!pip install folium   # Install Folium for Geographic data visualization
!pip install plotly_express   # Install plotlyExpress
```

::: {.output .stream .stdout}
    Reading package lists... Done
    Building dependency tree       
    Reading state information... Done
    gdal-bin is already the newest version (2.2.3+dfsg-2).
    python-gdal is already the newest version (2.2.3+dfsg-2).
    The following additional packages will be installed:
      python3-numpy
    Suggested packages:
      python-numpy-doc python3-nose python3-numpy-dbg
    The following NEW packages will be installed:
      python3-gdal python3-numpy
    0 upgraded, 2 newly installed, 0 to remove and 37 not upgraded.
    Need to get 2,288 kB of archives.
    After this operation, 13.2 MB of additional disk space will be used.
    Get:1 http://archive.ubuntu.com/ubuntu bionic/main amd64 python3-numpy amd64 1:1.13.3-2ubuntu1 [1,943 kB]
    Get:2 http://archive.ubuntu.com/ubuntu bionic/universe amd64 python3-gdal amd64 2.2.3+dfsg-2 [346 kB]
    Fetched 2,288 kB in 1s (1,599 kB/s)
    Selecting previously unselected package python3-numpy.
    (Reading database ... 155222 files and directories currently installed.)
    Preparing to unpack .../python3-numpy_1%3a1.13.3-2ubuntu1_amd64.deb ...
    Unpacking python3-numpy (1:1.13.3-2ubuntu1) ...
    Selecting previously unselected package python3-gdal.
    Preparing to unpack .../python3-gdal_2.2.3+dfsg-2_amd64.deb ...
    Unpacking python3-gdal (2.2.3+dfsg-2) ...
    Setting up python3-numpy (1:1.13.3-2ubuntu1) ...
    Setting up python3-gdal (2.2.3+dfsg-2) ...
    Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
    Reading package lists... Done
    Building dependency tree       
    Reading state information... Done
    The following additional packages will be installed:
      libspatialindex-c4v5 libspatialindex-dev libspatialindex4v5
      python3-pkg-resources
    Suggested packages:
      python3-setuptools
    The following NEW packages will be installed:
      libspatialindex-c4v5 libspatialindex-dev libspatialindex4v5
      python3-pkg-resources python3-rtree
    0 upgraded, 5 newly installed, 0 to remove and 37 not upgraded.
    Need to get 671 kB of archives.
    After this operation, 3,948 kB of additional disk space will be used.
    Get:1 http://archive.ubuntu.com/ubuntu bionic/universe amd64 libspatialindex4v5 amd64 1.8.5-5 [219 kB]
    Get:2 http://archive.ubuntu.com/ubuntu bionic/universe amd64 libspatialindex-c4v5 amd64 1.8.5-5 [51.7 kB]
    Get:3 http://archive.ubuntu.com/ubuntu bionic/main amd64 python3-pkg-resources all 39.0.1-2 [98.8 kB]
    Get:4 http://archive.ubuntu.com/ubuntu bionic/universe amd64 libspatialindex-dev amd64 1.8.5-5 [285 kB]
    Get:5 http://archive.ubuntu.com/ubuntu bionic/universe amd64 python3-rtree all 0.8.3+ds-1 [16.9 kB]
    Fetched 671 kB in 1s (551 kB/s)
    Selecting previously unselected package libspatialindex4v5:amd64.
    (Reading database ... 155632 files and directories currently installed.)
    Preparing to unpack .../libspatialindex4v5_1.8.5-5_amd64.deb ...
    Unpacking libspatialindex4v5:amd64 (1.8.5-5) ...
    Selecting previously unselected package libspatialindex-c4v5:amd64.
    Preparing to unpack .../libspatialindex-c4v5_1.8.5-5_amd64.deb ...
    Unpacking libspatialindex-c4v5:amd64 (1.8.5-5) ...
    Selecting previously unselected package python3-pkg-resources.
    Preparing to unpack .../python3-pkg-resources_39.0.1-2_all.deb ...
    Unpacking python3-pkg-resources (39.0.1-2) ...
    Selecting previously unselected package libspatialindex-dev:amd64.
    Preparing to unpack .../libspatialindex-dev_1.8.5-5_amd64.deb ...
    Unpacking libspatialindex-dev:amd64 (1.8.5-5) ...
    Selecting previously unselected package python3-rtree.
    Preparing to unpack .../python3-rtree_0.8.3+ds-1_all.deb ...
    Unpacking python3-rtree (0.8.3+ds-1) ...
    Setting up libspatialindex4v5:amd64 (1.8.5-5) ...
    Setting up python3-pkg-resources (39.0.1-2) ...
    Setting up libspatialindex-c4v5:amd64 (1.8.5-5) ...
    Setting up libspatialindex-dev:amd64 (1.8.5-5) ...
    Setting up python3-rtree (0.8.3+ds-1) ...
    Processing triggers for libc-bin (2.27-3ubuntu1.3) ...
    /sbin/ldconfig.real: /usr/local/lib/python3.7/dist-packages/ideep4py/lib/libmkldnn.so.0 is not a symbolic link

    Collecting git+git://github.com/geopandas/geopandas.git
      Cloning git://github.com/geopandas/geopandas.git to /tmp/pip-req-build-55t_je7a
      Running command git clone -q git://github.com/geopandas/geopandas.git /tmp/pip-req-build-55t_je7a
    Requirement already satisfied: pandas>=0.25.0 in /usr/local/lib/python3.7/dist-packages (from geopandas==0.10.2+16.gee8adfb) (1.1.5)
    Requirement already satisfied: shapely>=1.6 in /usr/local/lib/python3.7/dist-packages (from geopandas==0.10.2+16.gee8adfb) (1.8.0)
    Collecting fiona>=1.8
      Downloading Fiona-1.8.20-cp37-cp37m-manylinux1_x86_64.whl (15.4 MB)
    -manylinux2010_x86_64.whl (6.3 MB)
    ent already satisfied: setuptools in /usr/local/lib/python3.7/dist-packages (from fiona>=1.8->geopandas==0.10.2+16.gee8adfb) (57.4.0)
    Requirement already satisfied: six>=1.7 in /usr/local/lib/python3.7/dist-packages (from fiona>=1.8->geopandas==0.10.2+16.gee8adfb) (1.15.0)
    Requirement already satisfied: click>=4.0 in /usr/local/lib/python3.7/dist-packages (from fiona>=1.8->geopandas==0.10.2+16.gee8adfb) (7.1.2)
    Collecting munch
      Downloading munch-2.5.0-py2.py3-none-any.whl (10 kB)
    Collecting click-plugins>=1.0
      Downloading click_plugins-1.1.1-py2.py3-none-any.whl (7.5 kB)
    Requirement already satisfied: certifi in /usr/local/lib/python3.7/dist-packages (from fiona>=1.8->geopandas==0.10.2+16.gee8adfb) (2021.10.8)
    Requirement already satisfied: attrs>=17 in /usr/local/lib/python3.7/dist-packages (from fiona>=1.8->geopandas==0.10.2+16.gee8adfb) (21.2.0)
    Collecting cligj>=0.5
      Downloading cligj-0.7.2-py3-none-any.whl (7.1 kB)
    Requirement already satisfied: numpy>=1.15.4 in /usr/local/lib/python3.7/dist-packages (from pandas>=0.25.0->geopandas==0.10.2+16.gee8adfb) (1.19.5)
    Requirement already satisfied: python-dateutil>=2.7.3 in /usr/local/lib/python3.7/dist-packages (from pandas>=0.25.0->geopandas==0.10.2+16.gee8adfb) (2.8.2)
    Requirement already satisfied: pytz>=2017.2 in /usr/local/lib/python3.7/dist-packages (from pandas>=0.25.0->geopandas==0.10.2+16.gee8adfb) (2018.9)
    Building wheels for collected packages: geopandas
      Building wheel for geopandas (setup.py) ... e=geopandas-0.10.2+16.gee8adfb-py2.py3-none-any.whl size=1031775 sha256=88f139f05aad40a78065970f863373e107931c1dc0e785ceae5f04b8789a747c
      Stored in directory: /tmp/pip-ephem-wheel-cache-lds8b2b_/wheels/cf/3e/0b/6475054094c2b1ea054158ac1fdcf749fb92f5b512377e4cf8
    Successfully built geopandas
    Installing collected packages: munch, cligj, click-plugins, pyproj, fiona, geopandas
    Successfully installed click-plugins-1.1.1 cligj-0.7.2 fiona-1.8.20 geopandas-0.10.2+16.gee8adfb munch-2.5.0 pyproj-3.2.1
    Requirement already satisfied: descartes in /usr/local/lib/python3.7/dist-packages (1.1.0)
    Requirement already satisfied: matplotlib in /usr/local/lib/python3.7/dist-packages (from descartes) (3.2.2)
    Requirement already satisfied: numpy>=1.11 in /usr/local/lib/python3.7/dist-packages (from matplotlib->descartes) (1.19.5)
    Requirement already satisfied: kiwisolver>=1.0.1 in /usr/local/lib/python3.7/dist-packages (from matplotlib->descartes) (1.3.2)
    Requirement already satisfied: python-dateutil>=2.1 in /usr/local/lib/python3.7/dist-packages (from matplotlib->descartes) (2.8.2)
    Requirement already satisfied: cycler>=0.10 in /usr/local/lib/python3.7/dist-packages (from matplotlib->descartes) (0.11.0)
    Requirement already satisfied: pyparsing!=2.0.4,!=2.1.2,!=2.1.6,>=2.0.1 in /usr/local/lib/python3.7/dist-packages (from matplotlib->descartes) (3.0.6)
    Requirement already satisfied: six>=1.5 in /usr/local/lib/python3.7/dist-packages (from python-dateutil>=2.1->matplotlib->descartes) (1.15.0)
    Requirement already satisfied: folium in /usr/local/lib/python3.7/dist-packages (0.8.3)
    Requirement already satisfied: six in /usr/local/lib/python3.7/dist-packages (from folium) (1.15.0)
    Requirement already satisfied: jinja2 in /usr/local/lib/python3.7/dist-packages (from folium) (2.11.3)
    Requirement already satisfied: requests in /usr/local/lib/python3.7/dist-packages (from folium) (2.23.0)
    Requirement already satisfied: branca>=0.3.0 in /usr/local/lib/python3.7/dist-packages (from folium) (0.4.2)
    Requirement already satisfied: numpy in /usr/local/lib/python3.7/dist-packages (from folium) (1.19.5)
    Requirement already satisfied: MarkupSafe>=0.23 in /usr/local/lib/python3.7/dist-packages (from jinja2->folium) (2.0.1)
    Requirement already satisfied: chardet<4,>=3.0.2 in /usr/local/lib/python3.7/dist-packages (from requests->folium) (3.0.4)
    Requirement already satisfied: idna<3,>=2.5 in /usr/local/lib/python3.7/dist-packages (from requests->folium) (2.10)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in /usr/local/lib/python3.7/dist-packages (from requests->folium) (1.24.3)
    Requirement already satisfied: certifi>=2017.4.17 in /usr/local/lib/python3.7/dist-packages (from requests->folium) (2021.10.8)
    Collecting plotly_express
      Downloading plotly_express-0.4.1-py2.py3-none-any.whl (2.9 kB)
    Requirement already satisfied: scipy>=0.18 in /usr/local/lib/python3.7/dist-packages (from plotly_express) (1.4.1)
    Requirement already satisfied: statsmodels>=0.9.0 in /usr/local/lib/python3.7/dist-packages (from plotly_express) (0.10.2)
    Requirement already satisfied: plotly>=4.1.0 in /usr/local/lib/python3.7/dist-packages (from plotly_express) (4.4.1)
    Requirement already satisfied: patsy>=0.5 in /usr/local/lib/python3.7/dist-packages (from plotly_express) (0.5.2)
    Requirement already satisfied: numpy>=1.11 in /usr/local/lib/python3.7/dist-packages (from plotly_express) (1.19.5)
    Requirement already satisfied: pandas>=0.20.0 in /usr/local/lib/python3.7/dist-packages (from plotly_express) (1.1.5)
    Requirement already satisfied: pytz>=2017.2 in /usr/local/lib/python3.7/dist-packages (from pandas>=0.20.0->plotly_express) (2018.9)
    Requirement already satisfied: python-dateutil>=2.7.3 in /usr/local/lib/python3.7/dist-packages (from pandas>=0.20.0->plotly_express) (2.8.2)
    Requirement already satisfied: six in /usr/local/lib/python3.7/dist-packages (from patsy>=0.5->plotly_express) (1.15.0)
    Requirement already satisfied: retrying>=1.3.3 in /usr/local/lib/python3.7/dist-packages (from plotly>=4.1.0->plotly_express) (1.3.3)
    Installing collected packages: plotly-express
    Successfully installed plotly-express-0.4.1
    CPU times: user 455 ms, sys: 108 ms, total: 564 ms
    Wall time: 42.2 s
:::
:::

::: {.cell .code id="yEXXAL_stvxl"}
``` {.python}
import seaborn as sns
import matplotlib.pyplot as plt
import geopandas as geo
from shapely.geometry import Point
import matplotlib
import matplotlib.pyplot as plt 
import folium
import plotly_express as px
import altair as alt 
```
:::

::: {.cell .markdown id="R7wnI4QP4emr"}
## `<u>`{=html}`<b>`{=html}Summary Statistics`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="d6vxbgOyNNuJ"}
#### `<u>`{=html}The Gender Gap Index Summary Statistics`</u>`{=html}
:::

::: {.cell .markdown id="fj3RDMXzss2e"}
Below, we look at the summary statistics for the Global Gender Gap Index
data. Here we see that the mean score is 0.687736 and median is 0.691.
We can also see the mean and median for each of the various metrics
above. We find it interesting that the maximum score is 0.892 and
minimum is 0.451. The fact that no country has received a perfect score
of 1 gives insight that the gender gap index has not yet completely
closed in any country.
:::

::: {.cell .code colab="{\"height\":300,\"base_uri\":\"https://localhost:8080/\"}" id="P9dxWiqDfsn_" outputId="77570c06-001c-497b-e281-34fd31089099"}
``` {.python}
all_gggi_df.describe()
```

::: {.output .execute_result execution_count="24"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Year</th>
      <th>Rank</th>
      <th>Score</th>
      <th>Economic_Rank</th>
      <th>Economic_Score</th>
      <th>Education_Rank</th>
      <th>Education_Score</th>
      <th>Health_Rank</th>
      <th>Health_Score</th>
      <th>Political_Rank</th>
      <th>Political_Score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
      <td>2063.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2013.394086</td>
      <td>69.907416</td>
      <td>0.686941</td>
      <td>69.931653</td>
      <td>0.640637</td>
      <td>67.963645</td>
      <td>0.953069</td>
      <td>64.898206</td>
      <td>0.971943</td>
      <td>69.959767</td>
      <td>0.182244</td>
    </tr>
    <tr>
      <th>std</th>
      <td>4.502538</td>
      <td>40.509553</td>
      <td>0.060744</td>
      <td>40.583770</td>
      <td>0.121293</td>
      <td>43.228748</td>
      <td>0.082809</td>
      <td>46.397121</td>
      <td>0.010015</td>
      <td>40.529914</td>
      <td>0.132888</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2006.000000</td>
      <td>1.000000</td>
      <td>0.451000</td>
      <td>1.000000</td>
      <td>0.195000</td>
      <td>1.000000</td>
      <td>0.468000</td>
      <td>1.000000</td>
      <td>0.915000</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2010.000000</td>
      <td>35.000000</td>
      <td>0.651000</td>
      <td>35.000000</td>
      <td>0.584000</td>
      <td>35.000000</td>
      <td>0.951000</td>
      <td>1.000000</td>
      <td>0.969000</td>
      <td>35.000000</td>
      <td>0.087000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>2013.000000</td>
      <td>70.000000</td>
      <td>0.690000</td>
      <td>70.000000</td>
      <td>0.659000</td>
      <td>69.000000</td>
      <td>0.991000</td>
      <td>69.000000</td>
      <td>0.974000</td>
      <td>70.000000</td>
      <td>0.145000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2017.000000</td>
      <td>104.000000</td>
      <td>0.722000</td>
      <td>104.000000</td>
      <td>0.726000</td>
      <td>104.000000</td>
      <td>0.999000</td>
      <td>104.000000</td>
      <td>0.980000</td>
      <td>104.000000</td>
      <td>0.248000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2021.000000</td>
      <td>155.000000</td>
      <td>0.892000</td>
      <td>155.000000</td>
      <td>0.915000</td>
      <td>155.000000</td>
      <td>1.000000</td>
      <td>156.000000</td>
      <td>0.980000</td>
      <td>155.000000</td>
      <td>0.760000</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .markdown id="KXKhGYXXNZ2C"}
#### `<u>`{=html}Religious Composition Summary Statistics`</u>`{=html}
:::

::: {.cell .markdown id="G4cBISgm5fU4"}
Here we look at the summary statistics for the Religious Composition
data. We can see that on average, countries have more Christians and
Muslims than other religions. However, we must take into account that
the dominating religion of larger countries may have a greater impact on
the data averages.
:::

::: {.cell .code colab="{\"height\":300,\"base_uri\":\"https://localhost:8080/\"}" id="XX2vqYA_5brl" outputId="bd2b3dea-e629-4346-bb14-87b3da3f6e62"}
``` {.python}
religion_df.describe()
```

::: {.output .execute_result execution_count="25"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>level</th>
      <th>Nation_fk</th>
      <th>Year</th>
      <th>Christians</th>
      <th>Muslims</th>
      <th>Unaffiliated</th>
      <th>Hindus</th>
      <th>Buddhists</th>
      <th>Folk Religions</th>
      <th>Other Religions</th>
      <th>Jews</th>
      <th>All Religions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>1205.000000</td>
      <td>1205.000000</td>
      <td>1205.000000</td>
      <td>1.205000e+03</td>
      <td>1.205000e+03</td>
      <td>1.205000e+03</td>
      <td>1.205000e+03</td>
      <td>1.205000e+03</td>
      <td>1.205000e+03</td>
      <td>1.205000e+03</td>
      <td>1.205000e+03</td>
      <td>1.205000e+03</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>1.033195</td>
      <td>181.286307</td>
      <td>2030.000000</td>
      <td>3.187832e+07</td>
      <td>2.732775e+07</td>
      <td>1.502062e+07</td>
      <td>1.541210e+07</td>
      <td>6.220664e+06</td>
      <td>5.433477e+06</td>
      <td>7.657759e+05</td>
      <td>1.958672e+05</td>
      <td>1.022204e+08</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.201061</td>
      <td>652.395920</td>
      <td>14.148007</td>
      <td>1.836824e+08</td>
      <td>1.715920e+08</td>
      <td>1.060028e+08</td>
      <td>1.348549e+08</td>
      <td>4.787220e+07</td>
      <td>4.166840e+07</td>
      <td>5.476515e+06</td>
      <td>1.270617e+06</td>
      <td>6.281590e+08</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>2010.000000</td>
      <td>0.000000e+00</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>1.000000</td>
      <td>61.000000</td>
      <td>2020.000000</td>
      <td>1.300000e+05</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>5.100000e+05</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>1.000000</td>
      <td>121.000000</td>
      <td>2030.000000</td>
      <td>1.210000e+06</td>
      <td>1.600000e+05</td>
      <td>8.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>1.000000e+04</td>
      <td>6.330000e+06</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>1.000000</td>
      <td>183.000000</td>
      <td>2040.000000</td>
      <td>8.100000e+06</td>
      <td>3.740000e+06</td>
      <td>1.000000e+06</td>
      <td>2.000000e+04</td>
      <td>2.000000e+04</td>
      <td>1.800000e+05</td>
      <td>3.000000e+04</td>
      <td>1.000000e+04</td>
      <td>2.871000e+07</td>
    </tr>
    <tr>
      <th>max</th>
      <td>3.000000</td>
      <td>10000.000000</td>
      <td>2050.000000</td>
      <td>2.918070e+09</td>
      <td>2.761480e+09</td>
      <td>1.244190e+09</td>
      <td>1.384360e+09</td>
      <td>5.113000e+08</td>
      <td>4.519100e+08</td>
      <td>6.255000e+07</td>
      <td>1.609000e+07</td>
      <td>9.307190e+09</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .markdown id="EdC7t_r1Npdp"}
## `<u>`{=html}`<b>`{=html}Distributions`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="ZZdgtySAN1TJ"}
#### `<u>`{=html}The Gender Gap Index Distributions`</u>`{=html}
:::

::: {.cell .markdown id="FhraWDruasH9"}
To plot the distributions of the Gender Gap Index we can plot a
histogram and box plot. The histogram shows the overall distribution of
the scores. The box plot represents the median and IQR of the
distribution. We choose to mainly focus on a country\'s GGI score rather
than rank because countries are ranked based on comparision to other
countries for a specific year. We see in the histogram the distribution
is symmetric and unimodal, only slightly skewed to the right. This is
interesting because it shows us that the majority of countries have a
gender gap index score close to 0.7.
:::

::: {.cell .code colab="{\"height\":336,\"base_uri\":\"https://localhost:8080/\"}" id="apnUzUzhLBGY" outputId="7e72764b-ecf7-426c-d5bc-2578ae2570e6"}
``` {.python}
fig, ax = plt.subplots(1, 2, figsize=(20,5))
fig1 = all_gggi_df['Score'].plot.box(ax=ax[0], title="Box Plot of the World's GGGI Score", color='mediumseagreen')
fig2 = all_gggi_df['Score'].plot.hist(bins = 50, ax = ax[1], title="Distribution of Overall GGGI Scores", color='mediumseagreen')
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/4019e803b02b21b17a2cb64d556c5545f4f700ab.png)
:::
:::

::: {.cell .markdown id="pGDvxjnevb3M"}
Here, we look at the average of the GGI subindexes over the past 15
years. This graph informs us that on average, political and economic
scores worldwide are the lowest.
:::

::: {.cell .code colab="{\"height\":344,\"base_uri\":\"https://localhost:8080/\"}" id="HzYfeGlCn-En" outputId="c452a7b7-29ff-4228-b210-c7f7864fec0d"}
``` {.python}
new_all_gggi_df = all_gggi_df[['Year','Country', 'Economic_Score', 'Education_Score', 'Health_Score', 'Political_Score']]
new_all_gggi_df = new_all_gggi_df.set_index('Year')
new_all_gggi_df.mean().plot(kind="bar", label='World Average', title='Average Worldwide GGI Subindex Scores', figsize=(10,5), color='darksalmon', rot=360)
plt.legend(loc="lower left",bbox_to_anchor=(0.9,1.0))
plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/e2ab4f68163a01312db9dcb0407fc1162450bb20.png)
:::
:::

::: {.cell .markdown id="HWIy0XD7OJSR"}
:::

::: {.cell .code colab="{\"height\":343,\"base_uri\":\"https://localhost:8080/\"}" id="fbpC7Q1zOJfe" outputId="697ce881-eeb7-4f12-de2a-9c665adfea08"}
``` {.python}
spec_religion_df = religion_df[(religion_df['Year'] == 2020)].copy()
spec_religion_df = spec_religion_df[['Christians', 'Muslims', 'Unaffiliated', 'Hindus', 'Buddhists', 'Folk Religions', 'Other Religions', 'Jews']]
spec_religion_df.mean().plot(kind="bar", label='Average Religion Population', title='Average Worldwide Religion Populations', figsize=(10,5), color='seagreen', rot=360)
plt.legend(loc="lower left",bbox_to_anchor=(0.75,1.0))
plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/f3f3a35f19a29eed9913ba7715f30b1ed36030b0.png)
:::
:::

::: {.cell .markdown id="SuvJjxgTZgH6"}
## `<u>`{=html}`<b>`{=html}Relationship Strength`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="PYhWXWuybKiZ"}
Next, we explore the strengths of the relationship between the different
metrics including economic, political, health, education, and overall
rank. Both the correlation matrix and heatmap show that the political
and economic metrics have the strongest correlations with the overall
score. This means that a lot of the political policies, political
opportunities, and economic opportunities strongly affect the gender gap
index.

This is interesting because politics can play a huge role in gender
equality. Throughout history, politics have often played roles in
granting equal rights and opportunities for women.
:::

::: {.cell .code colab="{\"height\":654,\"base_uri\":\"https://localhost:8080/\"}" id="1hxhltBbBSOv" outputId="492b41be-a011-4de6-c672-1a642c639f53"}
``` {.python}
#Drop columns corresponding with rank to only look at the scores
all_gggi_score = all_gggi_df
all_gggi_score = all_gggi_score.drop(columns = ["Year", "Rank", "Economic_Rank", "Education_Rank", "Health_Rank", "Political_Rank"])
corr_score = all_gggi_score.corr()

# Plot correlation matrix and heatmap
f, ax = plt.subplots(figsize=(10,7))
f.suptitle("Correlation Matrix of Global Gender Gap Index Score and Subindex Scores", fontsize=16, y=0.95)
sns.heatmap(corr_score, annot = True)
plt.show()
corr_score
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/22ebc08f4d69363e9ba80ddbcb4b1681570f26b6.png)
:::

::: {.output .execute_result execution_count="29"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Score</th>
      <th>Economic_Score</th>
      <th>Education_Score</th>
      <th>Health_Score</th>
      <th>Political_Score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Score</th>
      <td>1.000000</td>
      <td>0.751156</td>
      <td>0.565653</td>
      <td>0.240833</td>
      <td>0.772235</td>
    </tr>
    <tr>
      <th>Economic_Score</th>
      <td>0.751156</td>
      <td>1.000000</td>
      <td>0.223157</td>
      <td>0.164396</td>
      <td>0.309088</td>
    </tr>
    <tr>
      <th>Education_Score</th>
      <td>0.565653</td>
      <td>0.223157</td>
      <td>1.000000</td>
      <td>0.166027</td>
      <td>0.195063</td>
    </tr>
    <tr>
      <th>Health_Score</th>
      <td>0.240833</td>
      <td>0.164396</td>
      <td>0.166027</td>
      <td>1.000000</td>
      <td>0.112411</td>
    </tr>
    <tr>
      <th>Political_Score</th>
      <td>0.772235</td>
      <td>0.309088</td>
      <td>0.195063</td>
      <td>0.112411</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .markdown id="xeEpGTrsbj61"}
## `<u>`{=html}`<b>`{=html}Geographic Visualization`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="CDnqfBS0bxAn"}
Here, we visualize the data in terms of its geographic location. This
enables us to better understand religion and gender gap scores in
broader regional terms which will help us determine if a specific
religion impacts countries\' gender gap score.
:::

::: {.cell .markdown id="i4H6aBmCdjHJ"}
We can plot our data by geographic location using the Geopandas library.
:::

::: {.cell .markdown id="EyjqYX5xdstQ"}
#### `<u>`{=html}The Gender Gap Index Geographic Visualization`</u>`{=html}
:::

::: {.cell .markdown id="_koqE4Z-edGd"}
In the Choropleth map of the Gender Gap Index scores by country, we see
that countries in eastern areas tend to have a lower gender gap score.
This tells us that gender gap scores tend to be similar among countries
in the same geographic region.
:::

::: {.cell .code colab="{\"height\":683,\"base_uri\":\"https://localhost:8080/\"}" id="T3x_PoSbB-vn" outputId="2f49aa97-3cd3-432e-9314-4e30a35152db"}
``` {.python}
#Join the two tables based on the country
table_new = religion_df.join(all_gggi_df.set_index(["Country"])["Rank"].to_frame("Rank"), on=["Country"])
table_new = table_new.join(all_gggi_df.set_index(["Country"])["Score"].to_frame("Score"), on=["Country"])

#Find the proportions of all religions
table_new["Christians_porp"] = table_new["Christians"]/table_new["All Religions"]
table_new["Muslims_porp"] = table_new["Muslims"]/table_new["All Religions"]
table_new["Unaffiliated_porp"] = table_new["Unaffiliated"]/table_new["All Religions"]
table_new["Hindus_porp"] = table_new["Hindus"]/table_new["All Religions"]
table_new["Buddhists_porp"] = table_new["Buddhists"]/table_new["All Religions"]
table_new["Folk Religions porp"] = table_new["Folk Religions"]/table_new["All Religions"]
table_new["Other_porp"] = table_new["Other Religions"]/table_new["All Religions"]
table_new["Jews_porp"] = table_new["Jews"]/table_new["All Religions"]

#world contains the information for each country and its shape
world = geo.read_file(geo.datasets.get_path("naturalearth_lowres"))

f1 = table_new.merge(world, left_on="Country", right_on="name", how="outer", indicator=True)
f1=f1[f1['_merge']=='left_only']
f1 = f1.drop_duplicates(subset='Country', keep='first')

#Combine the dataframes to use for plot
world_score = world.merge(table_new, left_on="name", right_on="Country")
world_score = world_score.drop(columns = ["Christians",	"Muslims",	"Unaffiliated",	"Hindus",	"Buddhists",	"Folk Religions",	"Other Religions",	"Jews"])
world_score = world_score.dropna(0)
#set the range for the choropleth
vmin, vmax = 120, 220
# create figure and axes for Matplotlib
fig, ax = plt.subplots(1, figsize=(20, 15))

world_score.plot(column='Score', cmap='YlGnBu', linewidth=0.8, ax=ax, edgecolor = '0.8', legend=True, legend_kwds = {'label': "Score by Country", 'orientation': "horizontal"})
ax.set_axis_off()
plt.show()

## NOTE: I will later fix the names of each country too
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/627c8369346ae66ebb88f84fee32f272b954f6db.png)
:::
:::

::: {.cell .markdown id="8vJaQ-srfVoZ"}
#### `<u>`{=html}Religious Composition Geographic Visualization`</u>`{=html}
:::

::: {.cell .markdown id="Gbgh3oQJfkgI"}
In the choropleth map of the religious composition data, we can see that
countries in the same geographic region tend to have the same major
religion. We can also see the geographic spread of each religion. In
particular, Christianity appears to be the most geographically spread
out religion.
:::

::: {.cell .code colab="{\"height\":476,\"base_uri\":\"https://localhost:8080/\"}" id="4zNz90pTGBEp" outputId="e446a14b-8752-4c5d-813b-c864066fbe95"}
``` {.python}
# Create a seperate column Max that has which of the religious populations is largest in that country
for_religion = religion_df
for_religion['Max'] = for_religion[["Christians",	"Muslims",	"Unaffiliated",	"Hindus",	"Buddhists",	"Folk Religions",	"Other Religions",	"Jews"]].idxmax(axis=1)
world_religion = world.merge(for_religion, left_on="name", right_on="Country")

# Set the range for the choropleth
vmin, vmax = 120, 220

# Create figure and axes for Matplotlib
fig, ax = plt.subplots(1, figsize=(20, 15))
world_religion.plot(column='Max', cmap='YlGnBu', linewidth=0.8, ax=ax, edgecolor = '0.8', legend=True)
ax.set_axis_off()
plt.show()

## NOTE: I will later fix the names of each country too
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/368e5f90616bb4529910e99aed3c14c756d9a6e3.png)
:::
:::

::: {.cell .markdown id="tAXb3zGp52fP"}
## `<u>`{=html}`<b>`{=html}Model Hypothesis`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="utGM_TNr6uw4"}
From our exploratory data analysis, we determined that we can create a
model to accomplish two things:
:::

::: {.cell .markdown id="k_Fnh-jG6A53"}
1.  We can evaluate how religion impacts overall scores and subindex
    scores by determining the correlations between overall score and
    religion as well as subindex score and religion
:::

::: {.cell .markdown id="F_b5tdLx6WDq"}
1.  We can predict a country\'s GGGI score from its predicted major
    religion or proportion of religions.
:::

::: {.cell .markdown id="szxL2TUVhWLm"}
\#**IV. Evaluating How Religion Impacts Subindex Scores**
:::

::: {.cell .markdown id="Hs8pXyKJiaO9"}
## `<u>`{=html}`<b>`{=html}Determining How Religion Impacts a Country\'s Gender Gap Subindex Scores & Overall Score`</b>`{=html}`</u>`{=html} {#determining-how-religion-impacts-a-countrys-gender-gap-subindex-scores--overall-score}
:::

::: {.cell .markdown id="2g9u829Wd2W-"}
As mentioned in our [External Factors That May Impact Our Model\'s
Accuracy section](#external_factors), we must remember that there are
additional factors that may impact a country\'s subindex scores other
than religion and that our model assumes these factors do not exist.
:::

::: {.cell .markdown id="xJmoCUB_eScV"}
In order to visualize how each religion correlates to each subindex
score, we graph scatter plots of each subindex score with each religion
and fit the data with a regression line to better visualize correlation.
Each point on the scatter plots represents the proportion of a
particular religion in a country and that country\'s particular subindex
score.
:::

::: {.cell .markdown id="tYEiQ02H7O58"}
To plot the religion data, we must first compute the proportions of
religious groups of each country in our dataset. To compute this, we
divide the number of members of each religious group by the total number
of members of all religious groups combined. It is important for us to
use these proportions instead of the number of members for each
religious group in each country because countries with larger
populations or more religious citizens will have a greater weight than
those with smaller populations or less religious citizens. By taking the
proportions of each group, we can standardize all of the religious group
variables to be measured on the same scale.
:::

::: {.cell .code id="UDF1sJ9cdlqz"}
``` {.python}
# Create dataframe for subindexes and religions
subindex_rel_df = all_gggi_df.merge(religion_df, how='inner', on=['Country', 'Year'], sort=True)

# Create lists of columns
religion_list = ['Muslims', 'Unaffiliated', 'Christians', 'Hindus', 'Buddhists', 'Folk Religions', 'Other Religions', 'Jews']
prop_religion_list = ['Muslims Proportion', 'Unaffiliated Proportion', 'Christians Proportion', 'Hindus Proportion', 'Buddhists Proportion', 'Folk Religions Proportion', 'Other Religions Proportion', 'Jews Proportion']
subindex_list = ['Economic_Score', 'Education_Score', 'Health_Score', 'Political_Score']
    
# Loop through list of columns and compute religion proportions for each column
for (i,j) in zip(religion_list, prop_religion_list):
    subindex_rel_df[j] = subindex_rel_df[i]/subindex_rel_df["All Religions"]

# Drop unnecessary columns   
subindex_rel_df_2020 = subindex_rel_df.loc[subindex_rel_df['Year'] > 2019].copy()   
subindex_rel_df_2020 = subindex_rel_df_2020.drop(columns=['All Religions', 'Year', 'level', 'Rank', 'Score', 'Economic_Rank', 'Education_Rank', 'Health_Rank', 'Political_Rank', 'Nation_fk', \
                                        'Muslims', 'Unaffiliated', 'Christians', 'Hindus', 'Buddhists', 'Folk Religions', 'Other Religions', 'Jews'])

# Create individual subindex/religion dataframes for plotting
df1,df2,df3,df4 = subindex_rel_df_2020[['Muslims Proportion', 'Economic_Score']], subindex_rel_df_2020[['Muslims Proportion', 'Education_Score']], subindex_rel_df_2020[['Muslims Proportion', 'Health_Score']], subindex_rel_df_2020[['Muslims Proportion', 'Political_Score']]
df5,df6,df7,df8 = subindex_rel_df_2020[['Unaffiliated Proportion', 'Economic_Score']], subindex_rel_df_2020[['Unaffiliated Proportion', 'Education_Score']], subindex_rel_df_2020[['Unaffiliated Proportion', 'Health_Score']], subindex_rel_df_2020[['Unaffiliated Proportion', 'Political_Score']]
df9,df10,df11,df12 = subindex_rel_df_2020[['Christians Proportion', 'Economic_Score']], subindex_rel_df_2020[['Christians Proportion', 'Education_Score']], subindex_rel_df_2020[['Christians Proportion', 'Health_Score']], subindex_rel_df_2020[['Christians Proportion', 'Political_Score']]
df13,df14,df15,df16 = subindex_rel_df_2020[['Hindus Proportion', 'Economic_Score']], subindex_rel_df_2020[['Hindus Proportion', 'Education_Score']], subindex_rel_df_2020[['Hindus Proportion', 'Health_Score']], subindex_rel_df_2020[['Hindus Proportion', 'Political_Score']]
df17,df18,df19,df20 = subindex_rel_df_2020[['Buddhists Proportion', 'Economic_Score']], subindex_rel_df_2020[['Buddhists Proportion', 'Education_Score']], subindex_rel_df_2020[['Buddhists Proportion', 'Health_Score']], subindex_rel_df_2020[['Buddhists Proportion', 'Political_Score']]
df21,df22,df23,df24 = subindex_rel_df_2020[['Folk Religions Proportion', 'Economic_Score']], subindex_rel_df_2020[['Folk Religions Proportion', 'Education_Score']], subindex_rel_df_2020[['Folk Religions Proportion', 'Health_Score']], subindex_rel_df_2020[['Folk Religions Proportion', 'Political_Score']]
df25,df26,df27,df28 = subindex_rel_df_2020[['Other Religions Proportion', 'Economic_Score']], subindex_rel_df_2020[['Other Religions Proportion', 'Education_Score']], subindex_rel_df_2020[['Other Religions Proportion', 'Health_Score']], subindex_rel_df_2020[['Other Religions Proportion', 'Political_Score']]
df29,df30,df31,df32 = subindex_rel_df_2020[['Jews Proportion', 'Economic_Score']], subindex_rel_df_2020[['Jews Proportion', 'Education_Score']], subindex_rel_df_2020[['Jews Proportion', 'Health_Score']], subindex_rel_df_2020[['Jews Proportion', 'Political_Score']]
```
:::

::: {.cell .markdown id="QQmshFTviHMJ"}
#### `<u>`{=html}Economic Score vs. Religion Proportion Visualization`</u>`{=html} {#economic-score-vs-religion-proportion-visualization}
:::

::: {.cell .markdown id="qn02xrI8fkam"}
First, we plot each country\'s economic score with its proportions for
each religion in our dataset. In the plots below, we can see that
Christianity and Unaffiliated have a positive correlation with economic
score. Islam has a negative correlation with economic score, and
Hinduism has a slightly negative correlation with economic score.
Buddhism, Folk Religions, Other, and Judaism have almost no correlation
with economic score.
:::

::: {.cell .code colab="{\"height\":657,\"base_uri\":\"https://localhost:8080/\"}" id="2sjtDCcJfyxq" outputId="8c45deb6-71ca-4c88-af82-99869ca2fcbd"}
``` {.python}
# Create list of dataframe containing economic subindex scores and religion proportions
economic_list = [df1,df5,df9,df13,df17,df21,df25,df29]

# Create subplots
fig, axes = plt.subplots(2,4,  figsize=(20, 10))
axes = axes.flatten()
fig.suptitle("Economic Score vs. Religion Proportion", fontsize=18, y=0.95)

# Loop through list of dataframes and plot scatter points in row of 4 subplots
count=0
for c in prop_religion_list[:4]:
    df = economic_list[count]
    ax = sns.regplot(data=df, x='Economic_Score', y=c,ax=axes[prop_religion_list.index(c)], color='cornflowerblue')   
    count+=1
    
for c in prop_religion_list[4:]:
    df = economic_list[count]
    ax = sns.regplot(data=df, x='Economic_Score', y=c,ax=axes[prop_religion_list.index(c)], color='cornflowerblue')
    count+=1

plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/89ebf338ba597012f59ec9de8e3ab02c3058e1ab.png)
:::
:::

::: {.cell .markdown id="12rtP5ZHhz7d"}
#### `<u>`{=html}Education Score vs. Religion Proportion Visualization`</u>`{=html} {#education-score-vs-religion-proportion-visualization}
:::

::: {.cell .markdown id="t66qiboihveq"}
Next, we plot each country\'s education score with its proportions for
each religion in our dataset. In the plots below, we can see that
Christianity and Unaffiliated have a positive correlation with education
score, and Other has a slightly positive correlation with education
score. Islam has a negative correlation with education score, and Folk
religions have a slightly negative correlation with education score.
Hinduism, Buddhism, and Judaism have almost no correlation with
education score.
:::

::: {.cell .code colab="{\"height\":657,\"base_uri\":\"https://localhost:8080/\"}" id="0R7_meozi5V6" outputId="8aa2acb2-a067-4c58-ddf6-c85d514294ef"}
``` {.python}
# Create list of dataframe containing education subindex scores and religion proportions
education_list = [df2, df6, df10, df14, df18, df22, df26, df30]

# Create subplots
fig, axes = plt.subplots(2,4,  figsize=(20, 10))
axes = axes.flatten()
fig.suptitle("Education Score vs. Religion Proportion", fontsize=18, y=0.95)

# Loop through list of dataframes and plot scatter points in row of 4 subplots
count=0
for c in prop_religion_list[:4]:
    df = education_list[count]
    ax = sns.regplot(data=df, x='Education_Score', y=c,ax=axes[prop_religion_list.index(c)], color='tomato')   
    count+=1
    
for c in prop_religion_list[4:]:
    df = education_list[count]
    ax = sns.regplot(data=df, x='Education_Score', y=c,ax=axes[prop_religion_list.index(c)], color='tomato')   
    count+=1

plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/2ba3fc5550794e5829b800657b9593224afd27d3.png)
:::
:::

::: {.cell .markdown id="lyuARauUjQ23"}
#### `<u>`{=html}Health Score vs. Religion Proportion Visualization`</u>`{=html} {#health-score-vs-religion-proportion-visualization}
:::

::: {.cell .markdown id="sEz6_BD7jKTQ"}
We then plot each country\'s health score with its proportions for each
religion in our dataset. In the plots below, we can see that
Christianity has a positive correlation with health score. Islam,
Hinduism, and Folk religions have a negative correlation with health
score. Unaffiliated religions, Buddhism, Other religions, and Judaism
have almost no correlation with health score.
:::

::: {.cell .code colab="{\"height\":657,\"base_uri\":\"https://localhost:8080/\"}" id="opg30SkOjbfy" outputId="8d1525b1-9102-4c88-fdb1-d07c1ddfeb4b"}
``` {.python}
# Create list of dataframe containing health subindex scores and religion proportions
health_list = [df3,df7,df11,df15,df19,df23,df27,df31]

# Create subplots
fig, axes = plt.subplots(2,4,  figsize=(20, 10))
axes = axes.flatten()
fig.suptitle("Health Score vs. Religion Proportion", fontsize=18, y=0.95)

# Loop through list of dataframes and plot scatter points in row of 4 subplots
count=0
for c in prop_religion_list[:4]:
    df = health_list[count]
    ax = sns.regplot(data=df, x='Health_Score', y=c,ax=axes[prop_religion_list.index(c)], color='mediumseagreen')   
    count+=1
    
for c in prop_religion_list[4:]:
    df = health_list[count]
    ax = sns.regplot(data=df, x='Health_Score', y=c,ax=axes[prop_religion_list.index(c)], color='mediumseagreen')   
    count+=1

plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/784951f99b76e50b43f4147a039b54d98a17cb99.png)
:::
:::

::: {.cell .markdown id="o-ShIaJDjsjv"}
#### `<u>`{=html}Political Score vs. Religion Proportion Visualization`</u>`{=html} {#political-score-vs-religion-proportion-visualization}
:::

::: {.cell .markdown id="qyWonjAAjuvU"}
Finally, we plot each country\'s political score with its proportions
for each religion in our dataset. In the plots below, we can see that
Christianity and Unaffiliated have a positive correlation with political
score. Islam and Buddhism have a negative correlation with political
score, and Folk religions have a slightly negative correlation with
political score. Hinduism, Other, and Judaism have almost no correlation
with political score.
:::

::: {.cell .code colab="{\"height\":657,\"base_uri\":\"https://localhost:8080/\"}" id="6uq5_7atkFTy" outputId="f9d8e198-e702-42bd-d629-aead4b70f161"}
``` {.python}
# Create list of dataframe containing health subindex scores and religion proportions
political_list = [df4,df8,df12,df16,df20,df24,df28,df32]

# Create subplots
fig, axes = plt.subplots(2,4,  figsize=(20, 10))
axes = axes.flatten()
fig.suptitle("Political Score vs. Religion Proportion", fontsize=18, y=0.95)

# Loop through list of dataframes and plot scatter points in row of 4 subplots
count=0
for c in prop_religion_list[:4]:
    df = political_list[count]
    ax = sns.regplot(data=df, x='Political_Score', y=c,ax=axes[prop_religion_list.index(c)], color='coral')   
    count+=1
    
for c in prop_religion_list[4:]:
    df = political_list[count]
    ax = sns.regplot(data=df, x='Political_Score', y=c,ax=axes[prop_religion_list.index(c)], color='coral')   
    count+=1

plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/e37e79b292ad05d3180985e064e5a115af5b0e0f.png)
:::
:::

::: {.cell .markdown id="2CBTx5sCiM3f"}
## `<u>`{=html}`<b>`{=html}Determining Which Subindex Score is Impacted the Most by Religion`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="t6MF6Pon0y09"}
To determine which subindex score is most impacted by a particular
religion(s), we plot a correlation matrix of the Global Gender Gap
subindexes and the religion proportions in our dataset.
:::

::: {.cell .markdown id="2Ta2L3nkPhyd"}
#### `<u>`{=html}Strongest Positive Correlation Between Religion and Subindex Scores`</u>`{=html}
:::

::: {.cell .markdown id="W6-wjhYzOO_Z"}
In the correlation matrix below, we can see that economic, health, and
political scores have the highest positive correlation with Christianity
with correlation values of 0.5, 0.5, 0.4, respectively. Education score
has the highest positive correlation with Unaffiliated and Christianity
with both religious groups sharing correlation values of 0.3.
:::

::: {.cell .markdown id="4jh1spVsPp75"}
#### `<u>`{=html}Strongest Negative Correlation Between Religion and Subindex Scores`</u>`{=html}
:::

::: {.cell .markdown id="CX3SHpXZSJpb"}
Economic, education, and political scores have the highest negative
correlation with Islam with correlation values of -0.6, -0.4, -0.3,
respectively. Health score has the strongest negative correlation with
Islam and Folk Religions which share a correlation value of -0.3.
:::

::: {.cell .code colab="{\"height\":600,\"base_uri\":\"https://localhost:8080/\"}" id="V-yaO5g-0zQ9" outputId="73f1f168-693e-4dfe-b72b-fc08c3e8f40c"}
``` {.python}
# Draw heatmap with numeric values in each cell
f, ax = plt.subplots(figsize=(12, 7))
f.suptitle('Correlation Matrix of Subindexes vs. Religion Proportions', fontsize=15)
cmap = sns.diverging_palette(15, 120, as_cmap=True, sep=60)
sns.heatmap(subindex_rel_df_2020.corr(), annot=True, fmt=".1f", linewidths=0.5, linecolor='w', ax=ax, cmap=cmap)
plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/c9cc9a81ae4377d461c16e7e889e56e46e967f95.png)
:::
:::

::: {.cell .markdown id="DmmHL3zSekbJ"}
## `<u>`{=html}`<b>`{=html}Determining Which Religion Impacts Overall GGGI Score the Most`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="PIQ_wi3nhrwI"}
To determine which religion impacts overall GGGI score the most, we plot
another heatmap of the correlation matrix for overall GGGI score and the
religion proportions in our dataset. In the heatmap below, we can see
that overall score has the strongest positive correlation with
Christianity and the strongest negative correlation with Islam which
have correlation values of 0.5 and -0.6, respectively.
:::

::: {.cell .code colab="{\"height\":600,\"base_uri\":\"https://localhost:8080/\"}" id="kJjrO-Mzekwh" outputId="cc9f3407-37ef-4917-f0cd-31f582bc1466"}
``` {.python}
# Create dataframe of overall score and religious proportions
score_rel_df = subindex_rel_df.copy()
score_rel_df = score_rel_df.drop(columns=['All Religions', 'Year', 'level', 'Rank', 'Economic_Rank', 'Education_Rank', 'Health_Rank', 'Political_Rank', 'Nation_fk', \
                                        'Muslims', 'Unaffiliated', 'Christians', 'Hindus', 'Buddhists', 'Folk Religions', 'Other Religions', 'Jews', 'Economic_Score', 'Education_Score', 'Health_Score', 'Political_Score'])

# Draw heatmap with numeric values in each cell
f, ax = plt.subplots(figsize=(12, 7))
f.suptitle('Correlation Matrix of Overall Score vs. Religion Proportions', fontsize=15)
cmap = sns.diverging_palette(200, 1, as_cmap=True, sep=60)
sns.heatmap(score_rel_df.corr(), annot=True, fmt=".1f", linewidths=0.5, linecolor='w', ax=ax, cmap=cmap)
plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/9abb18ef55f156ad11f14ca404155c733fb7f16a.png)
:::
:::

::: {.cell .markdown id="BM3HLwG_h9tx"}
\#**V. Predicting Gender Gap Index Scores Based on Predicted Religions**
:::

::: {.cell .markdown id="cyq9_wznHQnL"}
## `<u>`{=html}`<b>`{=html}Building a Prediction Model Using Religion Proportions`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="psTnU9o5k8CO"}
Using our findings from our first model question, we use the Gender Gap
Index Score and Religion proportion variables for each country to
predict a country\'s subindex and/or index scores.
:::

::: {.cell .markdown id="FPa_wLs0HyUt"}
#### `<u>`{=html}Building a Linear Regression Model`</u>`{=html}
:::

::: {.cell .markdown id="G9e9dUDopwrC"}
First we build and examine a linear regression model on the proportions
of each religion to predict the score.
:::

::: {.cell .code id="67NOk7BHksb3"}
``` {.python}
from sklearn.ensemble import RandomForestRegressor
from numpy import mean
from numpy import std
from sklearn.datasets import make_regression
from sklearn.model_selection import cross_val_score
from sklearn.model_selection import RepeatedKFold
from sklearn.ensemble import RandomForestRegressor
from sklearn import datasets, linear_model, metrics
```
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\"}" id="9urxgfvUuCBm" outputId="1c45817a-a1c9-4b0c-968c-eb8128d2abbb"}
``` {.python}
#Build and train model based on religious features
X = world_score[["Christians_porp",	"Muslims_porp",	"Unaffiliated_porp",	"Hindus_porp",	"Buddhists_porp",	"Folk Religions porp",	"Other_porp", "Jews_porp"]]
y = world_score.Score
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=1)
reg = linear_model.LinearRegression()
reg.fit(X_train.values, y_train.values)
print('Coefficients: ', reg.coef_)
print('Variance score: {}'.format(reg.score(X_test.values, y_test.values)))#as you can see our score is very low
print('Intercept:', reg.intercept_)
```

::: {.output .stream .stdout}
    Coefficients:  [ 0.52719229  0.43099553  0.60547662  0.46863548  0.49597554  0.40167294
     -0.74000635  0.55008101]
    Variance score: 0.436354188479781
    Intercept: 0.1837439499190786
:::
:::

::: {.cell .markdown id="QQ10RUeZ56bD"}
Based on the model above we can get the equation:

$y = x_{1}0.52719229 + x_{2}0.43099553 + x_{3}0.60547662 + x_{4}0.46863548 + x_{5}0.49597554 + x_{6}0.40167294 + x_{7}-0.74000635 + x_{8}0.55008101 + 0.1837439499190786$

We also see that the variance score is not good at 0.436, ideally we
would want a score closer to 1.0.
:::

::: {.cell .markdown id="4GW28RgXH-G2"}
#### `<u>`{=html}Building a Random Forest Regression Model`</u>`{=html}
:::

::: {.cell .markdown id="zylxb8Gblxly"}
To improve the variance score, we can use a random forest regressor
since there are no signs of linearity. Overall, this method of
regression yields a much better result with a variance score of 0.88 and
a very good MAE value of -0.016.
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\"}" id="DzR7DkAejlC7" outputId="85393ca6-d57a-4514-e4f9-7a7fb578f983"}
``` {.python}
reg = RandomForestRegressor(n_estimators=10, max_features=8)
reg.fit(X_train.values, y_train.values)
print('Variance score: {}'.format(reg.score(X_test.values, y_test.values)))
```

::: {.output .stream .stdout}
    Variance score: 0.8814052005914517
:::
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\"}" id="0f7Eo078uRWP" outputId="fa3fc163-e0a3-4903-b34d-427847bdd689"}
``` {.python}
cv = RepeatedKFold(n_splits=10, n_repeats=3, random_state=1)
n_scores = cross_val_score(reg, X, y, scoring='neg_mean_absolute_error', cv=cv, n_jobs=-1, error_score='raise')
# report performance
print('MAE: %.3f (%.3f)' % (mean(n_scores), std(n_scores)))
```

::: {.output .stream .stdout}
    MAE: -0.016 (0.000)
:::
:::

::: {.cell .markdown id="nT9QVa-USeBK"}
We then examine the model based on the known proportions from Fiji
below. The actual score is 0.626 but the predicted score is 0.6417.
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\"}" id="5sGM1LZjxMRI" outputId="aae8f5b9-ffea-47d8-f222-cf757dd5883b"}
``` {.python}
#predicting off of the data from Fiji and it should return about 0.626 as the score
predicted = reg.predict([[0.639535,	0.05814,	0.011628,	0.27907,	0.011628,	0.011628,	0.011628,	0.011628]])
print(predicted)
```

::: {.output .stream .stdout}
    [0.64258217]
:::
:::

::: {.cell .markdown id="x8GluEIy99Cf"}
This model is based off of the features of proportions. Using a Random
Forest Regression, we find that you can use religion to predict the
scores. The results are all pretty close to the actual scores.
:::

::: {.cell .markdown id="PwXWcZSHULbP"}
#### `<u>`{=html}Understanding Our Random Forest Regression Model`</u>`{=html}

We then compare the data from the actual score and the predicted score
to compare the linearity assumption. In the graph below, we can see that
the relationship between actual and predicted score is linear and that
there is a relatively strong correlation between the actual and
predicted score.
:::

::: {.cell .code colab="{\"height\":618,\"base_uri\":\"https://localhost:8080/\"}" id="Opi5kAq37UsO" outputId="b9b3514a-f07e-40f1-e58c-e4fac613ad4b"}
``` {.python}
world_score['score_pred'] = reg.predict(X)
world_score['residual'] = world_score["Score"]-world_score["score_pred"]

plt.figure(figsize=(10,5))
sns.lmplot(x='Score', y='score_pred', data=world_score, fit_reg=False, height=5)
    
# Plotting the diagonal line
line_coords = np.arange(world_score[['Score', 'score_pred']].min().min()- 0.3, 
                        world_score[['Score', 'score_pred']].max().max()+0.3)
plt.plot(line_coords, line_coords,  # X and y points
         color='darkorange', linestyle='--')

plt.ylabel('Predicted Scores', fontsize=14)
plt.xlabel('Actual Scores', fontsize=14)
plt.title('Actual vs. Predicted Scores From Random Forest Regression Model', fontsize=14)
plt.show()
```

::: {.output .stream .stderr}
    /usr/local/lib/python3.7/dist-packages/sklearn/base.py:439: UserWarning:

    X has feature names, but RandomForestRegressor was fitted without feature names
:::

::: {.output .display_data}
    <Figure size 1000x500 with 0 Axes>
:::

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/e737a07354e9ac11b97376fe82db0d06a05f66a4.png)
:::
:::

::: {.cell .markdown id="YvL2BU7qK6Lh"}
Next, we graph the predicted scores and the residuals to analyze how
accurate our predicted scores are. We can see that the graph below is a
good residual plot because it has a high density of points close to the
origin and is symmetric about the origin. Thus, our random forest
regression model does a good job at predicting scores.
:::

::: {.cell .code colab="{\"height\":493,\"base_uri\":\"https://localhost:8080/\"}" id="_nJ34nPPdzNl" outputId="8d6d1f12-32b3-42e5-feb2-0e0b6d48858d"}
``` {.python}
plt.figure(figsize=(10,5))
plt.scatter(world_score["score_pred"], world_score["residual"], color = 'mediumseagreen')
plt.axhline(y=0.0, color='r', linestyle='-')
plt.title('Predicted Score vs. Residual', fontsize=14)
plt.xlabel('Predicted Score', fontsize=14)
plt.ylabel('Residual', fontsize=14)
plt.show()
```

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/e8bbd583a52418e0e243f1107c7d554cbfc07c8d.png)
:::
:::

::: {.cell .markdown id="7dwaKcPvjKcz"}
## `<u>`{=html}`<b>`{=html}Building a Prediction Model Based Off of Major Religion`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="h9_ZquKgqPrn"}
Next we examined a model using countrys\' predicted dominant religion,
instead of proportions of all religions in each country. This model
however, is not very useful and yields a variance of 0.377.
:::

::: {.cell .code id="AC6P5Ypch7OE"}
``` {.python}
world_score['Max'] = world_score[["Christians_porp",	"Muslims_porp",	"Unaffiliated_porp",	"Hindus_porp",	"Buddhists_porp",	"Folk Religions porp",	"Other_porp",	"Jews_porp"]].idxmax(axis=1)
```
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\"}" id="huMwRKkviHy1" outputId="d4124c0f-ad7e-4d31-cab8-c57a5454649d"}
``` {.python}
#Build and train model based on religious features
X = world_score[["Max"]]
X=pd.get_dummies(X)
y = world_score.Score
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=1)
reg = RandomForestRegressor(n_estimators=10, max_features=1)
reg.fit(X_train.values, y_train.values)
print('Variance score: {}'.format(reg.score(X_test.values, y_test.values)))
```

::: {.output .stream .stdout}
    Variance score: 0.3775745311959273
:::
:::

::: {.cell .markdown id="odm-jp7PZPIC"}
## `<u>`{=html}`<b>`{=html}Building a Prediction Model with Muslim Proportions`</b>`{=html}`</u>`{=html}

Below we build the same random forest regression model but only having
the Muslim proportions as features. We decided to try this model with
this feature since looking at the correlation matrix, Muslim proportions
had a higher correlation value with the score. As we can see below, the
variance score is still pretty high at 0.86. The $R^{2}$ value is also
very high which is a positive sign.
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\"}" id="JvO47q2j-BCy" outputId="3d42eca6-3f7b-4591-b722-da7d48640509"}
``` {.python}
#Build and train model based on religious features
X = world_score[["Muslims_porp"]]
y = world_score.Score
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=1)
#reg = linear_model.LinearRegression()
#reg.fit(X_train.values, y_train.values)
reg = RandomForestRegressor(n_estimators=10, max_features=1)
reg.fit(X_train.values, y_train.values)
print('Variance score: {}'.format(reg.score(X_test.values, y_test.values)))
```

::: {.output .stream .stdout}
    Variance score: 0.8641835721718514
:::
:::

::: {.cell .code colab="{\"height\":639,\"base_uri\":\"https://localhost:8080/\"}" id="7O3Z2DLZ2XDO" outputId="9c9cf6a4-a99f-4405-c813-0078e9bed3bb"}
``` {.python}
#Looking how than Islamic proportions effects overall score
response = reg.predict(X)
r2 = reg.score(X, y)

plt.style.use('default')
plt.style.use('ggplot')
fig, ax = plt.subplots(figsize=(10, 5))
ax.scatter(X, response, color='k', label='Regression model')
ax.scatter(X, y, edgecolor='k', facecolor='grey', alpha=0.7, label='Sample data')

ax.set_ylabel('Islamic Proportion', fontsize=14)
ax.set_xlabel('Score', fontsize=14)
ax.legend(facecolor='white', fontsize=11)
ax.set_title('$R^2= %.2f$' % r2, fontsize=18)
plt.show()
```

::: {.output .stream .stderr}
    /usr/local/lib/python3.7/dist-packages/sklearn/base.py:439: UserWarning:

    X has feature names, but RandomForestRegressor was fitted without feature names

    /usr/local/lib/python3.7/dist-packages/sklearn/base.py:439: UserWarning:

    X has feature names, but RandomForestRegressor was fitted without feature names
:::

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/50ea10ba679250a7142e9eeda07b989cb8d0e177.png)
:::
:::

::: {.cell .markdown id="9thAtoykeXLc"}
## `<u>`{=html}`<b>`{=html}Building a Prediction Model with Christianity Proportions`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="sUOsKHcYe8-Z"}
Below we built the same random forest regression model but only having
the Christianity proportions as features. We decided to try this model
with this feature since looking at the correlation matrix, Christianity
proportions had a higher correlation value with the score. This model is
a pretty good model since the $R^{2}$ value is 0.88 and the variance
score is still also pretty high.
:::

::: {.cell .code colab="{\"base_uri\":\"https://localhost:8080/\"}" id="edIRjgnId1vv" outputId="0d2c1497-5943-4e56-eb91-cbf8bf5bf6b9"}
``` {.python}
#Build and train model based on religious features
X = world_score[["Christians_porp"]]
y = world_score.Score
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=1)
#reg = linear_model.LinearRegression()
#reg.fit(X_train.values, y_train.values)
reg = RandomForestRegressor(n_estimators=10, max_features=1)
reg.fit(X_train.values, y_train.values)
print('Variance score: {}'.format(reg.score(X_test.values, y_test.values)))
```

::: {.output .stream .stdout}
    Variance score: 0.8797764959833853
:::
:::

::: {.cell .code colab="{\"height\":656,\"base_uri\":\"https://localhost:8080/\"}" id="_1nheaLxd_SO" outputId="96da5947-1250-412c-e419-ebc9651a27ff"}
``` {.python}
#Looking how the Christianity proportions effects overall score
response = reg.predict(X)
r2 = reg.score(X, y)

plt.style.use('default')
plt.style.use('ggplot')
fig, ax = plt.subplots(figsize=(10, 5))
ax.scatter(X, response, color='k', label='Regression model')
ax.scatter(X, y, edgecolor='k', facecolor='grey', alpha=0.7, label='Sample data')

ax.set_ylabel('Christian Proportion', fontsize=14)
ax.set_xlabel('Score', fontsize=14)
ax.legend(facecolor='white', fontsize=11)
ax.set_title('$R^2= %.2f$' % r2, fontsize=18)
```

::: {.output .stream .stderr}
    /usr/local/lib/python3.7/dist-packages/sklearn/base.py:439: UserWarning:

    X has feature names, but RandomForestRegressor was fitted without feature names

    /usr/local/lib/python3.7/dist-packages/sklearn/base.py:439: UserWarning:

    X has feature names, but RandomForestRegressor was fitted without feature names
:::

::: {.output .execute_result execution_count="80"}
    Text(0.5, 1.0, '$R^2= 0.87$')
:::

::: {.output .display_data}
![](vertopal_1269b5fc497e40f7bacf0eda94063a15/a5793f4e7814698b1362ecf18d107d9f7c3b1be7.png)
:::
:::

::: {.cell .markdown id="YhhDwE8TibEY"}
\#**VI. Conclusion**
:::

::: {.cell .markdown id="onXbX-ZptJIz"}
## `<u>`{=html}`<b>`{=html}Answering Our Initial Questions`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="8qfxviuai5wV"}
Through the completion of this final tutorial, we have gained several
insights relating to our initial questions:
:::

::: {.cell .markdown id="b7daRgv5jpIH"}
**1. How does religion impact a country\'s gender gap subindex scores in
terms of health, education, economics, and politics?**\
Our analysis shows that countries with a higher number of members of
Christianity tend to have a higher economic, education, health, and
political score. Moreover, countries with a higher number of members of
Islam tend to have a lower economic, education, health, and political
score. Other religious groups that we evaluated including Unaffiliated,
Hinduism, Buddhism, Folk religions, Judaism, and other religions, do not
appear to have a strong impact on a country\'s subindex scores. While
our analysis resulted in the above conclusions about countries with a
more concentrated number of Christianity and Islam, the positive
correlation values did not exceed 0.5 and negative correlation values
did not exceed -0.6. Thus, there is not a perfect positive or negative
correlation between these religions and the GGGI subindexes. We can
conclude that there are most likely additional country characteristics
having a greater impact on subindex scores than religion. More research
should be done to evaluate these additional country characteristics that
may impact its subindex scores.
:::

::: {.cell .markdown id="aGQa2smgj-ZM"}
**2. Are particular major religions related to a lower overall gender
gap index score?**\
Similar to our findings in the question above, our analysis shows that
the number of members of Christianity and Islam impact the overall GGGI
score of a country. Countries with a higher number of members of
Christianity tend to have a higher overall score, and countries with a
higher number of members of Islam tend to have a lower overall score.
Other religious groups that we evaluated including Unaffiliated,
Hinduism, Buddhism, Folk religions, Judaism, and other religions, do not
appear to have a strong impact on a country\'s overall score. Again,
more research should be done to account for the additional factors that
could also impact a country\'s overall score.
:::

::: {.cell .markdown id="vyigjFpzj-hd"}
**3. Can we predict how a country\'s gender gap index score will change
over time based on the prediction of its future major religion?**

We examined linear regression models with the religious proportions as
the features. Our first linear regression model was not ideal with a low
variance score and it did not fit the assumptions. However, using a
random forest regression model, we can use the religious proportions to
successfully predict the score. When using only the major religion of
countries, both methods do not yield a successful way to predict future
score. We then built models using just the proportions of members of
Islam and Christianity, since we found that they had more of an impact
on the overall GGGI score of a country. Still, both models showed very
high variance scores and $R^{2}$ values. Thus, our findings show that
while we cannot use each country\'s major religion to predict gender gap
index scores, we can use the proportions of religions in each country to
accurately predict gender gap index scores in a random forest regression
model. However, this model could be improved with other features that
help impact the gender gap index score.
:::

::: {.cell .markdown id="IMuuEdf3tRn3"}
## `<u>`{=html}`<b>`{=html}More Resources on the Gender Gap`</b>`{=html}`</u>`{=html}
:::

::: {.cell .markdown id="eJK1w02Atfv2"}
Thank you for taking the time to learn more about our Exploratory
Analysis on the Global Gender Gap Index and Religion! We hope that you
found it interesting and gained some knowledge about the global gender
gap. In case you\'re interested in learning more about the gender gap,
we\'ve listed a few readings to further your learning:
:::

::: {.cell .markdown id="yMHRxPJrxtmN"}
[TIME: The Global Gender Gap Will Take an Extra 36 Years to Close After
the COVID-19 Pandemic, Report
Finds](https://time.com/5951101/global-gender-gap-135-years/)
:::

::: {.cell .markdown id="hUy4NvZIx70w"}
[United Nations: Women and Girls -- Closing the Gender
Gap](https://www.un.org/en/un75/women_girls_closing_gender_gap)
:::

::: {.cell .markdown id="5JS7_d8l0_1V"}
[U.S. News: Around the World, the Greatest Gender Disparities Are in
Politics](https://www.usnews.com/news/best-countries/articles/2021-04-13/the-greatest-gender-inequality-in-the-world-is-in-politics)
:::

::: {.cell .markdown id="2JT7VGTIyVBL"}
[*Dear Ijeawele, or A Feminist Manifesto in Fifteen
Suggestions*](https://www.amazon.com/Ijeawele-Feminist-Manifesto-Fifteen-Suggestions/dp/0525434801/ref=asc_df_0525434801/?tag=hyprod-20&linkCode=df0&hvadid=312736202848&hvpos=&hvnetw=g&hvrand=724739099013568940&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9025150&hvtargid=pla-466543736783&psc=1&tag=&ref=&adgrpid=62017409437&hvpone=&hvptwo=&hvadid=312736202848&hvpos=&hvnetw=g&hvrand=724739099013568940&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9025150&hvtargid=pla-466543736783)
by Chimamanda Ngozi Adichie
:::
