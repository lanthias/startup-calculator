[![Run on Datapane !](https://img.shields.io/badge/Datapane-Run%20script-1abc9c.svg)](https://datapane.com/leo/scripts/startup_calculator/)
[![View on Datapane !](https://img.shields.io/badge/Datapane-View%20sample%20report-ff69b4.svg)](https://datapane.com/leo/reports/startup_finance_report_0e7760f2/)

# Startup calculator
This script forecasts your future finances based on current cash position, growth rate, revenue, and costs.

Using pandas, it tries to answer two questions:

1. The most conservative scenario: if you fail to grow at all from this point, when you will run out of money and die? 
2. If you continue to grow at your current rate, when you will run out of money and die?

"Running out of money" is actually defined as having less than 25,000 in the bank, as this is presumed to be the minimum amount to wind down the company in a suitable fashion. 

It also uses Altair to plot [Default alive / Default dead](http://paulgraham.com/aord.html): the growth rate you will need to achieve to never die. This plot is inspired by a [similar one](http://growth.tlb.org/#) by Trevor Blackwell.

<img alt="image" src="https://user-images.githubusercontent.com/3541695/81616582-a6931780-93db-11ea-818a-752ef5642e8b.png">

>Warning: because calculating any kind of growth rate won't work if the starting revenue is 0, it uses 100 as a minimum start, which may throw off your calculations.

## Parameters
[<img width="1054" alt="image" src="https://user-images.githubusercontent.com/3541695/82499853-56f2d100-9aea-11ea-8f51-5970a02dc1d9.png">](https://datapane.com/scripts/MA1pRkK/)


## Usage
Run the Jupyter Notebook to generate reports using `datapane`, or deploy it to Datapane.com if you want to let other people run it through their browser (make sure you're logged in first).

```
~/> datapane script deploy
```

## More information
Check the datapane.yaml for full input parameter descriptions.

## Requirements

- pandas
- altair
- datapane
