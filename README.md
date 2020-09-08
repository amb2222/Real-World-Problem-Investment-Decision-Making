# Real-World-Problem-Investment-Decision-Making

## Objective
A company 'X' wants to make investments in a few companies. The CEO of 'X' wants to understand the global trends in investments so that he can take the investment decisions effectively.
'X' has two minor constraints for investments: 
1. It wants to invest between 5 to 15 million USD per round of investment 
2. It wants to invest only in English-speaking countries because of the ease of communication with the companies it would invest in 
(List of English-speakig countries: https://www.lingoda.com/en/content/english-speaking-countries/)

'X' wants to invest where most other investors are investing. This pattern is often observed among early stage startup investors.

## Dataset
I have taken real investment data from crunchbase.com.
We have three data files:
### companies.txt
A table with basic data of companies 
### mapping.csv
This file maps the numerous category names in the companies table (such 3D printing, aerospace, agriculture, etc.) to eight broad sector names. The purpose is to simplify the analysis into eight sector buckets, rather than trying to analyse hundreds of them. 
### round2.csv

## Sub-Goals
1.Investment type analysis: Comparing the typical investment amounts in the venture, seed, angel, private equity etc. so that 'X' can choose the type that is best suited for their strategy. 
2.Country analysis: Identifying the countries which have been the most heavily invested in the past. These will be 'X'’s favourites as well. 
3.Sector analysis: Understanding the distribution of investments across the eight main sectors. (Note that we are interested in the eight 'main sectors' provided in the mapping file. The two files — companies and rounds2 — have numerous sub-sector names; hence, we will need to map each sub-sector to its main sector.)

## Problem1: Data Processing
Load the companies and rounds data into two data frames and name them companies and rounds2 respectively.Merge the two data frames so that all variables (columns) in the companies frame are added to the rounds2 data frame. Name the merged frame master_frame. How many observations are present in master_frame?
## Problem2: Investment/Funding Type Analysis
The funding types such as seed, venture, angel, etc. depend on the type of the company (startup, corporate, etc.), its stage (early stage startup, funded startup, etc.), the amount of funding (a few million USD to a billion USD), and so on. For example, seed, angel and venture are three common stages of startup funding.
## Problem3: Country Analysis
'X' wants to invest in countries with the highest amount of funding for the chosen investment type. This is a part of its broader strategy to invest where most investments are occurring. 'X' wants to see the top nine countries which have received the highest total funding (across ALL sectors for the chosen investment type). Identify the top three English-speaking countries from top nine.
## Problem4: Sector Analysis
When we say sector analysis, we refer to one of the eight main sectors listed in the mapping file (note that ‘Other’ is one of the eight main sectors; also, there are eight 
sectors if you consider the category 'Blanks' as a missing value). This is to simplify the analysis by grouping the numerous category lists (named ‘category_list’) in the mapping file.Also, for some companies, the category list is a list of multiple sub-sectors separated by a pipe (vertical bar |). For example, one of the companies’ category_list is Application Platforms|Real Time|Social Network Media.
You discuss with the CEO and come up with the business rule that the first string before the vertical bar will be considered the primary sector. In the example above, ‘Application Platforms’ will be considered the primary sector. 

## Expected Result
A plot showing top 3 countries against the total amount of investments of specific funding type in different sectors
