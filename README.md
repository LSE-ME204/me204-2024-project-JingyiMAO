[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/VaFOWmpj)

# 🛠 Team

- LEGEQI Guillaume (Engineer Manager in Data and Finance🖥)
- Jingyi MAO (Bachelor of Mathematics with Appiled Mathematics in UNUK📊)

## ⚙️ How to replicate
1. Install Python and a conda dsitribution (either Anaconda or Miniconda)
2. Create a new conda environment for this project and activate it

```bash
conda create -name crime --python=3.11
conda activate crime
```

3. Installl the required packages:

```bash
pip install -r requirements.
pip install kaggle
pip install numpy pandas numerize lets_plot
pip install python-dotenv
pip install plotnine
pip install pandas numpy lets-plot numerize tqdm sqlalchemy jupysql
```

4. If running on VSCode, clone this repository and activate the correct environment every time you are running a notebook.

5. Go to the [Kaggle](https://www.kaggle.com/), create an account and get your credentials. Create a .env file in the folder where all the files from this repository are stored and save your username and key in the following format:
{
    'KAGGLE_USERNAME=<your user name>'
    'KAGGLE_KEY=<your key>'
}

6. Everything is ready! Go through each of the notebooks under the 'notebooks/' folder, read and run.


 
## 🤖 GenAI acknowledgement
ChatGPT is used in this project, primarily to help with data type cleaning and to visualize the spatial distribution of crime data.