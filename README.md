
## Introduction

More Alaska voters than ever are voting by mail or in early voting this year. This page tracks the numbers as reported by the state.

The data come from the [Alaska Division of Elections website](https://www.elections.alaska.gov/results/20GENR/data/sovc/CombinedBallotCountReport_Server.pdf) It's a 10-page pdf, so I ran a script using tabula-py to extract the data. Additional summary information is available [here](https://www.elections.alaska.gov/doc/info/statstable.php).

I have republished the data [here](https://github.com/benmatheson/alaska_2020_early_absentee_vote/tree/master/data/output), where you can download the reports from each day.  I had a google sheet that was updating automatically, but that kept breaking. 

If you see any errors, contact [Ben Matheson](https://twitter.com/benmatheson). *Disclaimer - this may not be fully accurate or up to date. It also may break at any time.* This is not official or affiliated with anything...enjoy!




The Alaska Division of Elections data is originally is published in a 10-page PDF that I parsed to extract the data. This uses a combination of R and Python. The Python uses Tabula to pull out the data. After that, an R script cleans out extra spaces, gaps, and labels the rows by house district and adds descriptions. I wanted to do everything in R, but I couldn't get rJava loaded for the Tabulizer, so the tabula-py library ended up being more expedient.

This page is an RMarkdown document that calculates some summary stats, like percent rejected and then displays the data in several ggplot2 plots. The PDF parsing in particular may be brittle and this could definitely break at anytime.
