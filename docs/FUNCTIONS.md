# Built-in Functions

The Trading Journal workbook has a number of functions built into it that are always available. They are listed here in alphabetical order.

**Built-in Functions**
|                           |                     |       |       |       |
| -------------             |:-------------------:| -----:| -----:| -----:|
| [getOptionType()](#getOptionType()) | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) |
| [exampleFunction()](#exampleFunction())  | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) |
| [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) | [exampleFunction()](#exampleFunction()) |

<a name="getOptionType()"></a>
### getOptionType(string)
Returns a string representing the type of option contract input by the user. Arguments may be a string copied from the thinkorswim platform.

``` excel
=getOptionType("SOLD -3 IRON CONDOR SPY 100 21 APR 17 240.5/241.5/228.5/227.5 CALL/PUT @.37")
```

Supported option strategies currently include:

| Option Type       | Example String |
|-------------------|:--------------|
|Long Call          |BOT +1 FAST 100 16 FEB 18 55 CALL @1.75 LMT|
|Short Call         |SOLD -1 FAST 100 16 FEB 18 55 CALL @1.60 LMT|
|Long Put           |BOT +1 FAST 100 16 FEB 18 52.5 PUT @1.70 LMT|
|Short Put          |SOLD -1 FAST 100 16 FEB 18 52.5 PUT @1.55 LMT|
|Long Call Vertical |BOT +1 VERTICAL MRK 100 20 OCT 17 65/67.5 CALL @1.13|
|Short Put Vertical |SOLD -1 VERTICAL ADBE 100 19 JAN 18 170/175 CALL @2.80|
|Iron Condor        |SOLD -1 IRON CONDOR QCOM 100 16 FEB 18 65/67.5/60/57.5 CALL/PUT @1.44|
|Butterfly          |BOT +1 BUTTERFLY SINA 100 19 MAY 17 65/70/75 CALL @.80|
|Calendar           |BOT +5 CALENDAR FSLR 100 16 JUN 17/19 MAY 17 25 CALL @.31|
|Diagonal           |BOT +1 DIAGONAL CRM 100 18 AUG 17/21 JUL 17 87.5/82.5 PUT @2.57|
|Synthetic          |SOLD -1 COMBO CVX 100 18 AUG 17 105 CALL/PUT @-2.06 LMT [TO OPEN/TO OPEN]|