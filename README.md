# US Election Analysis (1976 to 2020)

An exploratory data analysis of U.S. Presidential and Senate election results from 1976 to 2020. The goal was to see how voting patterns changed over time, how competitive elections have been, and how often states voted for different parties for President and Senate.

## Dataset

The data comes from the MIT Election Data and Science Lab and contains state level results for:

* Presidential elections, 1976 to 2020 (4,287 rows)
* Senate elections, 1976 to 2020 (3,629 rows)

## Data Cleaning

* Made column names lowercase and removed extra spaces from text
* Converted writein to True/False
* Dropped the empty notes column
* Filled missing party_detailed values from party_simplified and missing writein values with False
* Kept rows with no candidate name (grouped "other" votes) and flagged them in the presidential data so they are never picked as winners
* Checked for duplicates, negative votes and vote totals that did not add up (none found)
* For Georgia races decided by a runoff (1992, 2008 and 2020), kept only the runoff result
* Counted the January 2021 Georgia runoffs as part of 2020
* Fixed the swapped party labels in the Wyoming 2020 Senate race

No rows were dropped because of missing values.

## Analysis

1. National presidential vote share by party
2. Split ticket voting (states that voted for different parties for President and Senate)
3. Median winning margin in presidential elections
4. Senate seat share by party

## Key Findings

* Republicans had their highest vote share in 1984 (58.5%) and Democrats in 2008 (52.8%). Third parties made a real impact mainly in 1980, 1992 and 1996.
* Split ticket voting fell from 54.5% in 1984 to 0% in 2016. States now almost always pick the same party for both offices.
* The median presidential winning margin roughly doubled from 8.2% in 1992 to 17.1% in 2016, so fewer states are close contests.
* The closest race in the data was Florida in 2000, decided by less than 0.01%.
* Senate results swing a lot between cycles, for example Democrats won 23 of 33 races in 2012 and Republicans won 24 of 36 in 2014.

## Tools

Python, Pandas, Matplotlib, Jupyter Notebook

## How to Run

1. Clone this repository
2. Download the dataset and update the file path in the first code cell
3. Open the notebook in Jupyter or Kaggle and run all cells
