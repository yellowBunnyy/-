# COVID vs INFLUENZA analisis

# Discription

Comparing two viruses based on number of infection and deaths in Poland.
The analisis covers the yars 2020 - 2021.


## Table of Contents

- [About](#about)
- [Conclusions](#conclusions)
- [Used technologies](#technologies)
- [Folder Structure](#structure)



## I. About <a name = "about"></a>

This project have three steaps.
I.1. In step one we decided to get data from two diffrent sources:
COVID:
https://covid19.who.int/WHO-COVID-19-global-data.csv
Influenza:
http://wwwold.pzh.gov.pl/oldpage/epimeld/grypa/index.htm

In frist case we download a .csv file so it was easy, but in second case for extract data we were forced to use external library `tabula` for obtain data which we needed because data was on .pdf.
So we decide create data scraper which is included in this project look at [Folder Structure](#structure)

I.2. In second step downloaded data had to be adapted to the needs of our project eg. data must be prepared for our analisis (data preprocessin). Afret preprocessing data we make a analisis includes standard statstical operation:
- mean,
- std,
- max
- min
- summary, and so on


I.3. Plots.


## II. Conclusions. <a name="conclusions"></a>
After analisist we see COVD is more agresive than Flu. More people have been critically infected with the COVID virus, resulting in the deaths of those infected.

<!-- ![Alt Text](https://github.com/yellowBunnyy/key_gen/blob/master/p.png) -->


## III. Used technologies and libraries <a name="technologies"></a>

Python:
- pandas==1.4.1
- numpy==1.22.3
- matplotlib==3.5.1
- python-dotenv==0.20.0
- plotly-express==0.4.1
- poetry

Firstly install `poetry` by using:
>$ pip install poetry

More information at link : https://pypi.org/project/poetry/1.1.13/

How to install all libraries and dependencies:

>$ poetry install --no-root

## IV. Folder structure <a name="structure"></a>
```.
├── data_scraper
│   ├── create_csv.ipynb
│   ├── download_urls.py
│   ├── extract_data.py
│   └── requirements.txt
├── data_sets
│   ├── cov.csv
│   ├── influenza.csv
│   ├── pickledf
│   │   ├── covid.pickle
│   │   ├── influenza.pickle
│   │   └── __init__.py
│   └── prepare_data.ipynb
├── poetry.lock
├── pyproject.toml
└── README.md
```