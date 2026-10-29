# Data

The dataset is **not included** in this repository.

## Source

The notebook uses a version of the Coupon Recommendation dataset provided by the module (Business Data Mining and Visual Analytics, COMP1943, University of Greenwich). It appears to derive from the public **In-Vehicle Coupon Recommendation** dataset:

- UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation
- DOI: https://doi.org/10.24432/C5GS4P
- Licence: Creative Commons Attribution 4.0 International (CC BY 4.0)
- Citation: In-Vehicle Coupon Recommendation [Dataset]. (2017). UCI Machine Learning Repository. https://doi.org/10.24432/C5GS4P
- Introductory paper: Wang, T., Rudin, C., Doshi-Velez, F., Liu, Y., Klampfl, E. and MacNeille, P. (2017) 'A Bayesian framework for learning rule sets for interpretable classification', *Journal of Machine Learning Research*, 18(70), pp. 1-37.

The module version differs from the UCI original: it has 12,079 rows and 25 columns with no missing values, whereas the UCI original has 12,684 rows and contains missing values. Because the module copy cannot be confirmed as a straight redistribution of the public file, it is not published here. Running the notebook on the UCI original will need extra cleaning and will not reproduce the exact figures.

## Expected File

Place the file at `data/Coupon_Recommendation.csv` (comma-separated, header row). The notebook reads it from `../data/Coupon_Recommendation.csv`.

## Columns

Each row is one survey scenario: a driver is shown a coupon in a given driving context and says whether they would accept it.

| Column | Type | Description |
|---|---|---|
| destination | string | Trip destination (Home, Work, No Urgent Place) |
| passanger | string | Passenger type (Alone, Friend(s), Kid(s), Partner); spelling as in the source |
| weather | string | Weather (Sunny, Rainy, Snowy) |
| temperature | integer | Temperature level (30, 55, 80) |
| time | string | Time of day (7AM, 10AM, 2PM, 6PM, 10PM) |
| coupon | string | Coupon type (Bar, Coffee House, Carry out & Take away, Restaurant(<20), Restaurant(20-50)) |
| expiration | string | Coupon expiry window (2h, 1d) |
| gender | string | Gender of the driver |
| age | string | Age group |
| maritalStatus | string | Marital status |
| has_children | integer | 1 = has children, 0 = no |
| education | string | Highest education level |
| occupation | string | Occupational category (read but not used in the rules) |
| income | string | Income band |
| Bar | string | Bar visits per month (never, less1, 1~3, 4~8, gt8) |
| CoffeeHouse | string | Coffee house visits per month (same bands) |
| CarryAway | string | Take-away purchases per month (same bands) |
| RestaurantLessThan20 | string | Visits to restaurants under $20 per person per month (same bands) |
| Restaurant20To50 | string | Visits to restaurants at $20-$50 per person per month (same bands) |
| toCoupon_GEQ5min | integer | 1 = venue at least 5 minutes away (constant, dropped in the notebook) |
| toCoupon_GEQ15min | integer | 1 = venue at least 15 minutes away |
| toCoupon_GEQ25min | integer | 1 = venue at least 25 minutes away |
| direction_same | integer | 1 = venue in the same direction as the destination |
| direction_opp | integer | 1 = venue in the opposite direction |
| Y | integer | Target: 1 = coupon accepted, 0 = rejected |
