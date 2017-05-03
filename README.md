# Predicting Google Search Trends

Final Project for CSCI 5466 - Chaotic Dynamics

## Introduction

The goals of this project were to see whether of not some Google search trends are predictable. Class presentation can be found in [`slides.pdf`](https://github.com/allisonmorgan/google_trends/blob/master/slides.pdf).

### Setup

This package requires `numpy`, `sklearn`, `matplotlib` and `pandas`. The Jupyter notebook, `parse_google_trends.ipynb`, contains code for downloading, and cleaning a given Google search trend. To learn more read Samantha Molnar's [blog post](http://samanthamolnar.me/personal/2017/05/02/hacking-google-trends.html).

To play with one of the trends already downloaded ("baseball", "influenza", and "full moon"), you may run:

```{bash}
python main.py "full moon"
``` 

This will generate a plot of the [time series](https://github.com/allisonmorgan/google_trends/blob/master/data/fullmoon_hourly.csv.trend.png). It will also create plots of [mutual information](https://github.com/allisonmorgan/google_trends/blob/master/data/fullmoon_hourly.csv.mi.png) and percentage of [false nearest neighbors](https://github.com/allisonmorgan/google_trends/blob/master/data/fullmoon_hourly.csv.fnn.png) - the steps required to [delay-coordinate embed](https://github.com/allisonmorgan/google_trends/blob/master/data/fullmoon_hourly.csv.embed.png) the time series. Finally, it will produce a [prediction](https://github.com/allisonmorgan/google_trends/blob/master/data/fullmoon_hourly.csv_prediction.png) of the last 20% trend.

<img src="https://github.com/allisonmorgan/google_trends/blob/master/data/fullmoon_hourly.csv_prediction.png?raw=true"/>

### Works Cited

The file [`embedding.py`](https://github.com/allisonmorgan/google_trends/blob/master/embedding.py) contains python wrappers for some functions from the time series analysis package, [TISEAN](https://www.mpipks-dresden.mpg.de/~tisean/Tisean_3.0.1/index.html). Binaries relevant to this project have been reproduced in the [`tisean`](https://github.com/allisonmorgan/google_trends/tree/master/tisean) folder.

```
R. Hegger, H. Kantz, and T. Schreiber, Practical implementation of nonlinear time series methods: The TISEAN package, CHAOS 9, 413 (1999)
```
