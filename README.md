# Pine Script for Inside Bar Detection
This repository contains a Pine Script for detecting inside bars on TradingView charts. An inside bar is a candlestick pattern where the current bar's high is lower than the previous bar's high, and the current bar's low is higher than the previous bar's low. In other words, the current bar is inside the range of the previous bar.
## Usage
To use this script, you first need to add it to your TradingView chart. You can do this by clicking on the "Indicators" button at the top of the chart and searching for the "Inside Bar Detection" script under the "Scripts" tab. Once you find it, you can add it to your chart by clicking on the "Add to Chart" button.
Once the script is added to the chart, you can see the inside bars plotted as green triangles below the bars. Traders can use this information to identify potential price reversals or consolidation periods and adjust their trading strategies accordingly. For example, traders may look for inside bars near key support or resistance levels or use inside bars as a confirmation for other technical indicators or trading signals.
## Code Explanation
The Pine Script used to detect inside bars is as follows:
```pine
//@version=4
study("Inside Bar Detection", overlay=true)

// Determine inside bar
isInsideBar = low > low[1] and high < high[1]

// Plot inside bar
plotshape(isInsideBar, style=shape.triangleup, location=location.belowbar, color=color.green, size=size.small, transp=0)
```
