## English description

This is the repo of my solution to the *Medical Data Visualizer* project from the **Data Analysis with Python** course from freeCodeCamp. Portuguese description is down below.

### Assignment

In this project, you will visualize and make calculations from medical examination data using matplotlib, seaborn, and pandas. The dataset values were collected during medical examinations.

#### Data description

The rows in the dataset represent patients and the columns represent information like body measurements, results from various blood tests, and lifestyle choices. You will use the dataset to explore the relationship between cardiac disease, body measurements, blood markers, and lifestyle choices.

File name: medical_examination.csv

| Feature | Variable Type | Variable      | Value Type |
|:-------:|:------------:|:-------------:|:----------:|
| Age | Objective Feature | age | int (days) |
| Height | Objective Feature | height | int (cm) |
| Weight | Objective Feature | weight | float (kg) |
| Gender | Objective Feature | gender | categorical code |
| Systolic blood pressure | Examination Feature | ap_hi | int |
| Diastolic blood pressure | Examination Feature | ap_lo | int |
| Cholesterol | Examination Feature | cholesterol | 1: normal, 2: above normal, 3: well above normal |
| Glucose | Examination Feature | gluc | 1: normal, 2: above normal, 3: well above normal |
| Smoking | Subjective Feature | smoke | binary |
| Alcohol intake | Subjective Feature | alco | binary |
| Physical activity | Subjective Feature | active | binary |
| Presence or absence of cardiovascular disease | Target Variable | cardio | binary |

#### Tasks

Create a chart similar to `examples/Figure_1.png`, where we show the counts of good and bad outcomes for the `cholesterol`, `gluc`, `alco`, `active`, and `smoke` variables for patients with cardio=1 and cardio=0 in different panels.

Use the data to complete the following tasks in `medical_data_visualizer.py`:

* Add an `overweight` column to the data. To determine if a person is overweight, first calculate their BMI by dividing their weight in kilograms by the square of their height in meters. If that value is > 25 then the person is overweight. Use the value 0 for NOT overweight and the value 1 for overweight.
* Normalize the data by making 0 always good and 1 always bad. If the value of `cholesterol` or `gluc` is 1, make the value 0. If the value is more than 1, make the value 1.
* Convert the data into long format and create a chart that shows the value counts of the categorical features using seaborn's `catplot()`. The dataset should be split by 'Cardio' so there is one chart for each `cardio` value. The chart should look like `examples/Figure_1.png`.
* Clean the data. Filter out the following patient segments that represent incorrect data:
  - diastolic pressure is higher than systolic (Keep the correct data with `(df['ap_lo'] <= df['ap_hi'])`)
  - height is less than the 2.5th percentile (Keep the correct data with `(df['height'] >= df['height'].quantile(0.025))`)
  - height is more than the 97.5th percentile
  - weight is less than the 2.5th percentile
  - weight is more than the 97.5th percentile
* Create a correlation matrix using the dataset. Plot the correlation matrix using seaborn's `heatmap()`. Mask the upper triangle. The chart should look like `examples/Figure_2.png`.

Any time a variable is set to `None`, make sure to set it to the correct code.

Unit tests are written for you under `test_module.py`.

### Development

For development, you can use `main.py` to test your functions. Click the "run" button and `main.py` will run.

### Testing 

We imported the tests from `test_module.py` to `main.py` for your convenience. The tests will run automatically whenever you hit the "run" button.

### Submitting

Copy your project's URL and submit it to freeCodeCamp.

-------------------------------------------------------------------------------------------------------

## Descri????o em portugu??s

Esse ?? o reposit??rio com a minha solu????o para o projeto *Medical Data Visualizer* do curso **Data Analysis with Python** do freeCodeCamp. A tradu????o ?? livre e feita por mim.

### Tarefa

Nesse projeto, voc?? vai visualizar e realizar c??lculos a partir de dados de exames m??dicos usando matplotlib, seaborn and pandas. Os valores do dataset foram coletados durante exames m??dicos.

#### Descri????o dos dados

As linhas no dataset representam pacientes e as colunas representam informa????es como medidas corporais, resultados de exames de sangue e escolhas de estilo de vida. Voc?? usar?? o dataset para explorar a rela????o entre doen??a card??aca, medidas corporais, marcadores sangu??neos e escolhas de estilo de vida.

Nome do arquivo: medical_examination.csv

| Feature | Variable Type | Variable      | Value Type |
|:-------:|:------------:|:-------------:|:----------:|
| Age | Objective Feature | age | int (days) |
| Height | Objective Feature | height | int (cm) |
| Weight | Objective Feature | weight | float (kg) |
| Gender | Objective Feature | gender | categorical code |
| Systolic blood pressure | Examination Feature | ap_hi | int |
| Diastolic blood pressure | Examination Feature | ap_lo | int |
| Cholesterol | Examination Feature | cholesterol | 1: normal, 2: above normal, 3: well above normal |
| Glucose | Examination Feature | gluc | 1: normal, 2: above normal, 3: well above normal |
| Smoking | Subjective Feature | smoke | binary |
| Alcohol intake | Subjective Feature | alco | binary |
| Physical activity | Subjective Feature | active | binary |
| Presence or absence of cardiovascular disease | Target Variable | cardio | binary |

#### Tarefas

Crie um gr??fico similar a `examples/Figure_1.png`, onde mostramos a quantidade de resultados bons e ruins para as vari??veis `cholesterol`, `gluc`, `alco`, `active`, e `smoke` para pacientes com cardio=1 e cardio=0 em pain??is diferentes.

Use os dados para completar as seguintes tarefas em `medical_data_visualizer.py`:
* Acrescente uma coluna `overweight` aos dados. Para determinar se uma pessoa est?? acima do peso, primeiro calcule o seu IMC dividindo seu peso em quilogramas pelo quadrado de sua altura em metros. Se esse valor ?? > 25 ent??o a pessoa est?? acima do peso. Use 0 para quem n??o estiver acima do peso e 1 para quem estiver.
* Normalize os dados fazendo 0 sempre bom e 1 sempre ruim. Se o valor de `cholesterol` ou `gluc` ?? 1, torne-o 0. Se o valor ?? maior que 1, torne-o 1.
* Converat os dados em long format e crie um gr??fico que mostra a quantidade de features categ??ricas usando a fun????o `catplot()` do seaborn. O dataset deve ser dividido por 'Cardio', ent??o deve haver um gr??fico para cada valor de `cardio`. O gr??fico deve parecer com `examples/Figure_1.png`.
* Limpe os dados. Filtre os seguintes segmentos de pacientes, que representam dados incorretos:
  - press??o diast??lica maior que a sist??lica (mantenha os dados corretos com `(df['ap_lo'] <= df['ap_hi'])`)
  - altura menor que o 2.5th percentil (mantenha os dados corretos com `(df['height'] >= df['height'].quantile(0.025))`)
  - altura maior que o 97.5th percentil
  - peso menor que o 2.5th percentil
  - peso maior que o 97.5th percentil
* Crie uma matriz de correla????o usando o dataset. Plote a matriz usando `heatmap()` do seaborn. Mascare o tri??ngulo superior. O gr??fico deve parecer com `examples/Figure_2.png`.

Sempre que uma vari??vel for `None`, garante de atribuir a ela o c??digo correto.

Testes unit??rios foram escritos para voc?? em `test_module.py`.

### Desenvolvimento

Para desenvolvimento, voc?? pode usar `main.py` para testar suas fun????es. Clique em "run" e `main.py` rodar??.

### Testando 

Os testes unit??rios para este projeto est??o em `test_module.py`. Importamos os testes de `test_module.py` para `main.py` por conveni??ncia. Os teste v??o rodar automaticamente quando clicar em "run".

### Submiss??o

Copie a URL do projeto e submeta-a ao freeCodeCamp.
