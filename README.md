# quantr

R package for fetching financials and stock market data.

## Usage

### Euronext tickers

```r
euronext_tickers("XBRU")

# A tibble: 144 x 12
   name     isin    symbol market    currency    open   high     low   last last_datetime       volume turnover
   <chr>    <chr>   <chr>  <chr>     <chr>      <dbl>  <dbl>   <dbl>  <dbl> <dttm>               <dbl>    <dbl>
 1 AB INBEV BE0974… ABI    Euronext… EUR      5.23e+1  52.9  5.22e+1  52.6  2021-02-12 17:35:00 1.17e6   6.18e7
 2 ABO GRO… BE0974… ABO    Euronext… EUR      3.80e+0   3.8  3.70e+0   3.7  2021-02-12 16:30:00 2.20e1   8.16e1
 3 ACACIA … GB00BY… ACPH   Euronext… EUR      3.11e+0   3.17 3.10e+0   3.15 2021-02-12 17:35:00 1.32e5   4.15e5
 4 ACCENTIS BE0003… ACCB   Euronext… EUR      4.95e-2   0.05 4.95e-2   0.05 2021-02-12 15:52:00 2.62e4   1.31e3
 5 ACKERMA… BE0003… ACKB   Euronext… EUR      1.30e+2 130    1.28e+2 129.   2021-02-12 17:35:00 1.83e4   2.36e6
 6 ADVICEN… FR0013… ADVIC  Euronext… EUR      1.27e+1  13.8  1.26e+1  13.7  2021-02-12 17:38:00 9.39e4   1.22e6
 7 AEDIFICA BE0003… AED    Euronext… EUR      1.01e+2 102    1.00e+2 100.   2021-02-12 17:35:00 3.09e4   3.10e6
 8 AGEAS    BE0974… AGS    Euronext… EUR      4.56e+1  45.7  4.50e+1  45.4  2021-02-12 17:35:00 2.18e5   9.88e6
 9 AGFA-GE… BE0003… AGFB   Euronext… EUR      3.82e+0   3.82 3.78e+0   3.81 2021-02-12 17:35:00 5.73e4   2.18e5
10 AHOLD D… NL0011… AD     Euronext… EUR      2.31e+1  23.6  2.31e+1  23.5  2021-02-12 17:37:00 4.38e6   1.03e8
# … with 134 more rows
```

### Xetra tickers

```r
xetra_tickers()

# A tibble: 3,073 x 9
   name                      isin        symbol mic   mic_primary mic_reporting currency instrument_type market
   <chr>                     <chr>       <chr>  <chr> <chr>       <chr>         <chr>    <chr>           <chr> 
 1 FACC AG INH.AKT.          AT00000FAC… 1FC    XETR  XWBO        XETB          EUR      CS              Xetra 
 2 RAIFFEISEN BK INTL INH.   AT00006063… RAW    XETR  XWBO        XETB          EUR      CS              Xetra 
 3 PORR AG                   AT00006096… ABS2   XETR  XWBO        XETB          EUR      CS              Xetra 
 4 LENZING AG                AT00006445… LEN    XETR  XWBO        XETB          EUR      CS              Xetra 
 5 ERSTE GROUP BNK INH. O.N. AT00006520… EBO    XETR  XWBO        XETB          EUR      CS              Xetra 
 6 S IMMO AG                 AT00006522… T1L    XETR  XWBO        XETB          EUR      CS              Xetra 
 7 TELEKOM AUSTRIA AG        AT00007200… TA1    XETR  XWBO        XETB          EUR      CS              Xetra 
 8 ANDRITZ AG                AT00007300… AZ2    XETR  XWBO        XETB          EUR      CS              Xetra 
 9 OMV AG                    AT00007430… OMV    XETR  XWBO        XETB          EUR      CS              Xetra 
10 VERBUND AG       INH. A   AT00007464… OEWA   XETR  XWBO        XETB          EUR      CS              Xetra 
# … with 3,063 more rows
```

### Nasdaq and NYSE tickers

```r
nasdaq_tickers()

# A tibble: 3,735 x 10
   symbol name                   last  change volume   market_cap country   industry         sector    ipo_year
   <chr>  <chr>                 <dbl>   <dbl> <chr>         <dbl> <chr>     <chr>            <chr>        <int>
 1 AACG   "ATA Creativity Glo…   5.72  0.1    1610099     1.79e 8 China     Other Consumer … Consumer…       NA
 2 AACQ   "Artius Acquisition…  11.3   0.01   1427755     1.02e 9 United S… Business Servic… Finance       2020
 3 AACQU  "Artius Acquisition…  12.1   0.16   134919      0.      United S… Business Servic… Finance       2020
 4 AACQW  "Artius Acquisition…   2.5  -0.0416 300867      0.      United S… Business Servic… Finance       2020
 5 AAL    "American Airlines …  17.3   0.28   274118…     1.07e10 United S… Air Freight/Del… Transpor…       NA
 6 AAME   "Atlantic American …   5.71  0.45   2251125     1.17e 8 United S… Life Insurance   Finance         NA
 7 AAOI   "Applied Optoelectr…  12.2  -0.11   455336      2.81e 8 United S… Semiconductors   Technolo…     2013
 8 AAON   "AAON Inc. Common S…  79.2  -0.15   126212      4.14e 9 United S… Industrial Mach… Capital …       NA
 9 AAPL   "Apple Inc. Common … 135.    0.24   600273…     2.35e12 United S… Computer Manufa… Technolo…     1980
10 AAWW   "Atlas Air Worldwid…  56.1   1.82   920836      1.54e 9 United S… Transportation … Transpor…       NA
# … with 3,725 more rows
```

```r
nyse_tickers()

# A tibble: 3,037 x 10
   symbol name                        last change volume  market_cap country  industry        sector   ipo_year
   <chr>  <chr>                      <dbl>  <dbl> <chr>        <dbl> <chr>    <chr>           <chr>       <int>
 1 A      "Agilent Technologies In… 128.     1.02 1277628    3.91e10 "United… "Biotechnology… "Capita…     1999
 2 AA     "Alcoa Corporation Commo…  21.7    0.27 3304816    4.03e 9 ""       "Aluminum"      "Basic …     2016
 3 AAIC   "Arlington Asset Investm…   3.89   0.17 243716     1.30e 8 "United… "Real Estate I… "Consum…       NA
 4 AAIC^B "Arlington Asset Investm…  22.4    0.15 500       NA       "United… ""              ""             NA
 5 AAIC^C "Arlington Asset Investm…  22.4   -0.07 2395      NA       "United… ""              ""             NA
 6 AAN    "Aarons Holdings Company…  20.0    0.03 250189     6.75e 8 "United… "Diversified C… "Techno…     2020
 7 AAP    "Advance Auto Parts Inc … 153.    -1.65 846631     1.04e10 "United… "Other Special… "Consum…       NA
 8 AAT    "American Assets Trust I…  30.1   -0.22 414638     1.82e 9 "United… "Real Estate I… "Consum…     2011
 9 AB     "AllianceBernstein Holdi…  37.7   -1.04 596647     3.62e 9 "United… "Investment Ma… "Financ…       NA
10 ABB    "ABB Ltd Common Stock"     29.5    0.26 1050056    6.00e10 "Switze… "Electrical Pr… "Consum…       NA
# … with 3,027 more rows
```

### Yahoo Finance summary data

```r
yahoo_summary(c("AAPL", "MSFT", "AMZN"))

# A tibble: 3 x 131
  priceHint previousClose  open dayLow dayHigh regularMarketPr… regularMarketOp… regularMarketDa…
      <int>         <dbl> <dbl>  <dbl>   <dbl>            <dbl>            <dbl>            <dbl>
1         2          135.  134.   134.    136.             135.             134.             134.
2         2          244.  244.   243.    245.             244.             244.             243.
3         2         3262. 3250   3233.   3280.            3262.            3250             3233.
# … with 123 more variables: regularMarketDayHigh <dbl>, dividendRate <dbl>, dividendYield <dbl>,
#   exDividendDate <int>, payoutRatio <dbl>, fiveYearAvgDividendYield <dbl>, beta <dbl>, trailingPE <dbl>,
#   forwardPE <dbl>, volume <int>, regularMarketVolume <int>, averageVolume <int>, averageVolume10days <int>,
#   averageDailyVolume10Day <int>, bid <dbl>, ask <dbl>, bidSize <int>, askSize <int>, marketCap <dbl>,
#   fiftyTwoWeekLow <dbl>, fiftyTwoWeekHigh <dbl>, priceToSalesTrailing12Months <dbl>, fiftyDayAverage <dbl>,
#   twoHundredDayAverage <dbl>, trailingAnnualDividendRate <dbl>, trailingAnnualDividendYield <dbl>,
#   currency <chr>, fromCurrency <lgl>, toCurrency <lgl>, lastMarket <lgl>, algorithm <lgl>, tradeable <lgl>,
#   enterpriseValue <dbl>, profitMargins <dbl>, floatShares <dbl>, sharesOutstanding <dbl>, sharesShort <int>,
#   sharesShortPriorMonth <int>, sharesShortPreviousMonthDate <int>, dateShortInterest <int>,
#   sharesPercentSharesOut <dbl>, heldPercentInsiders <dbl>, heldPercentInstitutions <dbl>, shortRatio <dbl>,
#   shortPercentOfFloat <dbl>, category <lgl>, bookValue <dbl>, priceToBook <dbl>, fundFamily <lgl>,
#   legalType <lgl>, lastFiscalYearEnd <int>, nextFiscalYearEnd <int>, mostRecentQuarter <int>,
#   earningsQuarterlyGrowth <dbl>, netIncomeToCommon <dbl>, trailingEps <dbl>, forwardEps <dbl>,
#   pegRatio <dbl>, lastSplitFactor <chr>, lastSplitDate <int>, enterpriseToRevenue <dbl>,
#   enterpriseToEbitda <dbl>, `52WeekChange` <dbl>, SandP52WeekChange <dbl>, lastDividendValue <dbl>,
#   lastDividendDate <int>, exchange <chr>, quoteType <chr>, symbol <chr>, underlyingSymbol <chr>,
#   shortName <chr>, longName <chr>, firstTradeDateEpochUtc <int>, timeZoneFullName <chr>,
#   timeZoneShortName <chr>, uuid <chr>, messageBoardId <chr>, gmtOffSetMilliseconds <int>,
#   preMarketSource <chr>, postMarketChangePercent <dbl>, postMarketChange <dbl>, postMarketTime <int>,
#   postMarketPrice <dbl>, postMarketSource <chr>, regularMarketChangePercent <dbl>,
#   regularMarketChange <dbl>, regularMarketTime <int>, regularMarketPrice <dbl>,
#   averageDailyVolume3Month <int>, regularMarketSource <chr>, exchangeName <chr>,
#   exchangeDataDelayedBy <int>, marketState <chr>, quoteSourceName <chr>, currencySymbol <chr>,
#   currentPrice <dbl>, targetHighPrice <dbl>, targetLowPrice <dbl>, targetMeanPrice <dbl>,
#   targetMedianPrice <dbl>, …
```
