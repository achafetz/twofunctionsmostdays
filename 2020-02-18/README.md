2020-02-18
================

# `scales::dollar()` - i know this one\!

``` r
library(scales)

money <- c(1.50, 100, 1000, 40000)

# Give nice dollar formatting to some money!
dollar(money)
```

    ## [1] "$1.50"      "$100.00"    "$1,000.00"  "$40,000.00"

``` r
# You can change the prefix (or suffix!), the thousand separator, and decimal mark, too:
dollar(money, prefix = "\u20ac", big.mark = " ", decimal.mark = ",")
```

    ## [1] "€1,50"      "€100,00"    "€1 000,00"  "€40 000,00"

# `tidyr::full_seq()` - new to me\!

``` r
library(tidyr)

# A sequence, by 5, but missing 15:
x <- c(0, 5, 10, 20)

# Create the full sequence by specifying the gap between observations
full_seq(x, period = 5)
```

    ## [1]  0  5 10 15 20

``` r
# Works with dates, too!
y <- as.Date(c("2020-01-01", "2020-01-03"))

full_seq(y, period = 1)
```

    ## [1] "2020-01-01" "2020-01-02" "2020-01-03"
