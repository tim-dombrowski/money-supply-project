# Money Supply Project

### Overview

This demonstration is focused on analyzing the expansion of the U.S. Dollar Money Supply. In this project demo, the R Notebook will retrieve three different measurements of the USD money supply (M2, M1, and the Currency component of M1) from FRED. Then we examine each of the three time series for trends and introduce the concept of autocorrelation (a.k.a. serial dependence). These time series will be transformed into annualized growth rates, which reduces the autocorrelation present in the time series. Then we will examine the distribution of the growth rates and fit a normal distribution to the data. Finally, we will use the normal distribution to calculate the probability of observing the growth rates that we have seen in the data.

### Additional Context Around the Data

On April 24, 2020, the Fed decided to remove a rule distinguishing "transaction accounts" and "savings deposits". The previous rule limited convenient transfers from savings deposit accounts to six-per-month. Deleting this rule eliminated any limit to the liquidity of these accounts. The idea behind this was to allow more access to liquidity from longer-term savings due to the pandemic ([Fed. Press Release](https://www.federalreserve.gov/newsevents/pressreleases/bcreg20200424a.htm)).

This rule change had a pronounced effect on the [M1 Money Stock](https://fred.stlouisfed.org/series/M1SL) beginning in May 2020. Under the previous rule, the limited access to savings deposits did not qualify them as part of the "money stock" under the M1 definition. However, after the rule change, these accounts are now "readily accessible for spending" since there is no transaction limit. Thus, the chart for M1 exhibits a more than a 200% increase from April to May 2020 (from under \$5T to over \$16T). Although the rule change took place in April 2020, this change to the data series occurred in February 2021 and was applied retroactively in the FRED data series going back to May 2020.

Regarding the [M2 Money Stock](https://fred.stlouisfed.org/series/M2SL), this is a broader definition of the money supply compared to the M1. Thus, the savings deposits are included both before and after May 2020.

Then the [Currency Component of M1](https://fred.stlouisfed.org/series/CURRSL) is a narrower definition compared to the M1, as it only considers currency in circulation outside the U.S. Treasury and Federal Reserve Banks. Thus, savings accounts do not fit into this definition either before or after May 2020.

Lastly, another change from around this same time is that the FRED is no longer publishing weekly, seasonally adjusted values for the money supply measurements. There is still a weekly, non-seasonally-adjusted series and a monthly series that is seasonally adjusted. We will use the latter in this version of the project. This also enables us to go back all the way to 1959 with the data.

### Repository Structure

The data work for this project demo is contained in the R Notebook directory of this repository. On GitHub, the webpage should display the README.md file, which contains the compiled output of the R Notebook. If you wish to explore the source code locally, then you can open the moneysupply.Rmd file in RStudio and execute the code chunks to replicate the data work. Note the `output: html_notebook` line in the header of that file, which indicates that the R Markdown document is an R Notebook. 

After exploring the R Notebook and making any desired changes, you can then create a copy that will appear on GitHub. To do this, save a copy of the R Notebook and name it README.Rmd. Then, change the header line to `output: github_document`, which will switch the file from being an R Notebook to an R Markdown file that will compile into a generic [Markdown](https://www.markdownguide.org/) file (.md). This format (along with the README name) will automatically be recognized by GitHub and displayed in-browser. This will also replace the Preview button with an option to Knit the Markdown file. This knitting process will re-run all the code chunks and generate a new README.md file inside of the R Notebook folder, which will display on GitHub.
