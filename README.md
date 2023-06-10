# COVID vs INFLUENZA analisis

# Discription

Comparing two viruses based on number of infection and deaths in Poland.
The analisis covers the yars 2020 - 2021.


## Table of Contents

- [About](#about)
- [Used technologies](#technologies)
- [How to run API](#api)
- [Folder Structure](#structure)


## About <a name = "about"></a>

This project have three steaps.
I. In step one we decided to get data from two diffrent sources:
COVID:
https://covid19.who.int/WHO-COVID-19-global-data.csv
Influenza:
http://wwwold.pzh.gov.pl/oldpage/epimeld/grypa/index.htm

In frist case we download a .csv file so it was easy, but in second case for extract data we were forced to use external library `tabula` for obtain data which we needed because data was on .pdf.
So we decide create data scraper which is included in this project look at [Folder Structure](#structure)

II. In second step downloaded data had to be adapted to the needs of our project and we make preprocessing our data.
This preprocessing include:
- fill n/a data
- change data types
- obtain the necessary data from downloaded data

At the end of the preprocessing we pilcke DataFrames for low usage memory.

III. Data analisis.



## Used technologies and libraries <a name="technologies"></a>

Python:
- pandas==1.4.1
- numpy==1.22.3
- matplotlib==3.5.1
- python-dotenv==0.20.0
- plotly-express==0.4.1

