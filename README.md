
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

# The rise of China in World University Rankings
## Rankings 2011 - 2023*. 
<sup>*Years 2020, 2017 and 2016 not available.</sup>

<p align="center">
    <img width="400" height="200" src="https://github.com/aleivaar94/University-World-Rankings-2023/blob/master/assets/times-higher-logo.png"/>
</p>

Although the US continues to dominate the world rankings overall, China has overtaken the US in terms of the volume of high quality academic research it produces. At this rate China could overtake the US in the coming years, adding another race between the two superpowers.

Canada has ranked consistently in the top 100, but has less universities than China in the top 100 since 2022.


## Demo 
![](https://github.com/aleivaar94/University-World-Rankings-2023/blob/master/assets/Bar-chart-race-gif.gif)

<sup>Bar chart race made using Flourish.</sup>

## Requirements

```
numpy==1.20.3
pandas==1.3.4
```

## Methodology

### Data Collection

Data was extracted from The Times Higher Education World University Rankings website from 2011 to 2023. Years 2020, 2017 and 2016 are missing at the time of webscraping.

It was not possible to reverse engineer The Times Higher Education website to make an automated data request using API and Python. However, the data for each year was complete in json format. 

![](https://github.com/aleivaar94/University-World-Rankings-2023/blob/master/assets/api-response.png)

<sup>Response can be accessed by going into developer tools in Chrome. The API response will be data in json format. It can be accessed inside the `Network` tab.</sup>

Postman was used to make a request to dump the data of each year into a json file. The rankings for each year were saved into a separate `.json` file and concatenated into a single file using the glob library.


![](https://github.com/aleivaar94/University-World-Rankings-2023/blob/master/assets/copy-link-response.png)

<sup>Right click the file containing the data and copy the link address.</sup>


![](https://github.com/aleivaar94/University-World-Rankings-2023/blob/master/assets/postman.png)

<sup>Make a request using Postman by pasting the link address and making an sending a request. Save the output of the request in a `.json` file.</sup>


### Data Analysis

Follow the jupyter notebook to see the methodology in detail:

```
world-university-rankings-2023-extraction.ipynb
```

The `flourish.csv` file contains the pivoted rankings for [Flourish](https://flourish.studio/) to properly render the bar chart race.

## Results

A beautiful and fun bar chart race made using [Flourish](https://flourish.studio/).
