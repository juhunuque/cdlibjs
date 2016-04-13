## Introduction

Time ago, I had the requirement of create a calculator for Certificates of Deposit (Financial stuff), so, I went throught the internet looking for
a JavaScript library that makes the process simpler, but for my surprise, I was not able to find anyone.

Whom does not know about Certificate of Deposit, in the simplest words we can say is a promissory note issued by the bank. If you want to know
a little more about so, you only need to google.

## About formulas

There are 4 main factors in a Certificate of deposit, they're:
- Interest
- Capital
- Rate
- Term

If we have 3 of the 4 factors, we would get the result, this is the main goal of the library.

The formulas are:
- Interest = (Capital * rate * term)/ 365 (Natural Days) 
- Term = (Interest * 365) / (Capital * rate)
- Rate = (Interest * 365) / (Capital * term)
- Capital = (Interest * 365) / (Rate * Term)  

## Code Example

Firstable, you must include the library in your JavaScript declarations:
```javascript
<script src="js/others/cdLib.js"></script>
```

Then you can normally use it. Let's suppose we want to obtain the interest earned, we would obtain it in this way:

```javascript
var capital = 5000; 
var term = 90; // Number of days
var rate = 15; // In percentage

var interest = cdLib.calculatingInterestDates(capital,rate,term);
```

Also, you can pass a start and a end date instead of number of days;

```javascript
var capital = 5000; 
var rate = 15; // In percentage
var startDate = new Date('2016-3-27');
var endDate = new Date('2016-6-27');

var interest = cdLib.calculatingInterestDates(capital,rate,startDate,endDate);
```

If you want to check an example, click on the following [link] (www.desarrollosnunez.net/cdCalculator/index.html)

## Installation

Download the library and import it within your project:

```javascript
<script src="js/others/cdLib.js"></script>
```

## API Reference

- cdLib.calculatingInterest( capital, rate, term )
- cdLib.calculatingInterestDates( capital, rate, startDate, endDate )
- cdLib.calculatingTerm( interest, capital, rate )
- cdLib.calculatingRate( interest, capital, term )
- cdLib.calculatingRateDates( interest, capital, startDate, endDate )
- cdLib.calculatingCapital( interest, rate, term )
- cdLib.calculatingCapitalDates( interest, rate, startDate, endDate )
- cdLib.annualisedYield( inverstment, performance, days )
- cdLib.annualisedYieldDates( inverstment, performance, startDate, endDate )
- cdLib.daysBetweenDates( start, end )


## Contributors

So far, only Julio Núñez is working on this.

## License

MIT License

## Links

- Github: [certificateDeposit-calculator] (https://github.com/juhunuque/certificateDeposit-calculator)
- Sample: [http://www.desarrollosnunez.net/cdCalculator/index.html] (http://www.desarrollosnunez.net/cdCalculator/index.html)
