# US Minimum Wage by State from 1968 to 2017

## Rationale for Project
While looking online for a clean dataset for minimum wage data by state, I was having trouble finding one. I decided to create one myself and provide it to the community.

## Files and Sources
This repository contains 3 primary items:
- [`Minimum Wage Data.csv`](Minimum%20Wage%20Data.csv): A cleaned dataset of US state and federal minimum wages from 1968 to 2017 (including 2018 equivalency values). The data was scraped from the [United States Department of Labor's table of minimum wage by state](https://www.dol.gov/whd/state/stateMinWageHis.htm). 
- [`1808 - Minimum Wage by State from 1968 to 2017 - R Code.Rmd`](1808%20-%20Minimum%20Wage%20by%20State%20from%201968%20to%202017%20-%20R%20Code.Rmd): The code used to clean the data
- [`CPI 1913 - 2018.csv`](CPI%201913%20-%202018.csv): A dataset containing the CPI values used to calculate 2018 equivalent wages. I kept the values in here so that other equivalent dollars could easily be calculated without needing to bring in a separate dataset.
 
## Description of Data
The values in the [dataset](Minimum%20Wage%20Data.csv) are as follows:
- Year: The year of the data.
- State: The state or territory of the data.
- Table_Data: The scraped value from the [source](https://www.dol.gov/whd/state/stateMinWageHis.htm).
- Footnote: The footnote associated with the Table_Data. [See more below](README.md#data-footnotes).
- High.Value: As there were some values in Table_Data that had multiple values (usually associated with footnotes), this is the higher of the two values in the table. It could be useful for viewing the proposed minimum wage, because in most cases, the higher value meant that all persons protected under minimum wage laws eventually had minimum wage set at that value.
- Low.Value: This is the same as High.Value, but has the lower of the two values. This could be useful for viewing the effective minimum wage at the year of setting the minimum wage, as peoples protected under such minimum wage laws made that value during that year (although, in most cases, they had a higher minimum wage after that year).
- CPI.Average: This is the [Consumer Price Index](https://www.investopedia.com/terms/c/consumerpriceindex.asp) associated with that year. It was used to calculate 2018-equivalent values.
- High.2018: This is the 2018-equivalent dollars for High.Value.
- Low.2018: This is the 2018-equivalent dollars for Low.Value.

### Data Footnotes
As laws differ a lot from territory to territory, especially relating to whom is protected by minimum wage laws, the following footnotes are located throughout the data in Footnote to add more context to the minimum wage. [The original footnotes can be found here.](https://www.dol.gov/whd/state/stateMinWageHis.htm)

(a) - under the Federal Fair Labor Standards Act (FLSA), the two rates shown in 1968, 1970, and 1976 reflect the former multiple-track minimum-wage system in effect from 1961 to 1978. The lower rate applied to newly covered persons brought under the act by amendments, whose rates were gradually phased in. A similar dual-track system was also in effect in certain years under the laws in Connecticut, Maryland, and Nevada.

(b) - For the years indicated, the laws in Arizona, Arkansas, California, Colorado, Kentucky, Minnesota, Ohio, Utah, and Wisconsin applied only to women and minors.

[c] - Rates applicable to employers of four or more.

(d) - Rates applicable to employers of six or more. In West Virginia, applicable to employers of six or more in one location.

(e) - Rates applicable to employers of two or more.

(f) - For the years 1988 to 1990, Minnesota had a two tier schedule with the higher rate applicable to employers covered by the FLSA and the lower rate to employers not covered by the FLSA.

(g) - Minnesota sets a lower rate for enterprises with annual receipts of less than $500,000 ($4.90, January 1, 1998-January 1, 2005). The dollar amount prior to September 1, 1997 was $362,500 ($4.00 - January 1, 1991-January 1, 1997); Montana sets a lower rate for businesses with gross annual sales of $110,000 or less ($4.00 - January 1, 1992-January 1, 2005); Ohio sets a lower rate for employers with gross annual sales from $150,000 to $500,000 ($3.35 - January 1, 1991-January 1, 2005) and for employers with gross annual sales under $150,000 ($2.50 - January 1, 1991-January 1, 2005); Oklahoma sets a lower rate for employers of fewer than 10 full-time employees at any one location and for those with annual gross sales of less than $100,000 ($2.00, January 1, 1991-January 1, 2005); and the U.S. Virgin Islands sets a lower rate for businesses with gross annual receipts of less than $150,000 ($4.30, January 1, 1991-January 1, 2005).

(h) - In the District of Columbia, wage orders were replaced by a statutory minimum wage on October 1, 1993. A $5.45 minimum rate remained in effect for the laundry and dry cleaning industry as the result of the grandfather clause.

(i) - In Puerto Rico, separate minimum rates are in effect for almost 350 non-farm occupations by industry Mandatory Decrees. Rates are higher than those in the range listed in effect in a few specific occupations. 
(i2) - The rate is 5.08/hour for those employees not covered by the Fair Labor Standards Act.

(j) - In the U.S. Virgin Islands, implementation of an indexed rate, which was to have started January 1, 1991, was delayed.
