# Certified B-Corporation Investment Index

## For my job @KeeneAdvisors, we wanted to create a bespoke stock index of Certified B-Corporations.
### The index will appeal to investors who are interested in global leaders in sustainable business practices

Becoming a Certified B-Corporation status is facilitated by the nonprofit [B-Lab]([url](https://usca.bcorporation.net/)). Many Certified B-Corporations are private companies, but there are over 50 public Certified B-Corporations globally as of the beginning of 2024.

I researched and built a trackable index of the Top 20 public B-Corporations. We looked at several iterations of the methodology, including a price-weighted index as well as a market-cap weighted index and backtested the performance of both standalone B-Corps as well as larger organizations that had B-Corp subsidiaries.

- The initial dataset includes companies from 28 global stock exchanges, so each stock had to be mapped to the correct exchange to be able to access Yahoo Finance price history.

- Each stock's price history and market capitalization is reported in local currency. Our challenge included mapping each currency correctly then converting local currency into USD every day to allow for standardized currency.

- We considered many iterations of inclusion criteria, which is present in this code

## Methodology
1. At initiation, a stock had to be publicly traded and be an active Certified B-Corporation. No large companies with B-Corp subsidiaries
2. The price and market cap was then calculated in US Dollars
3. The top 20 companies by market-cap were included
4. We constructed a price-weighted index. If an investor chose to buy 1 share of each of the 20 stocks, they would track the index.
5. The index is reconstituted annually with stocks below the Top 20 market cap falling out and stocks within the Top 20 market cap being added.
6. The divisor is adjusted annually and whenever there are corporate actions so those events do not impact the value of the index.
