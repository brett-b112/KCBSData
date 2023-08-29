
# Information Below provided from Kaggle: 
#### [Kaggle Dataset and Information Here](https://www.kaggle.com/datasets/jaysobel/kansas-city-barbeque-society-competition-results)
# About Dataset
## Summary
### Access
This data set is also available as a public data set on Mode Analytics as raindata.table_name. Mode provides a PostgreSQL interface for querying and dashboard creation.

### Kansas City Barbeque Society
The Kansas City Barbeque Society hosts competitive BBQ events in the US and around the world. The KCBS trains and certifies barbeque judges to provide rigorous scoring at their contests. Millions of dollars in prizes are awarded annually to top teams.

This data set represents all of the competition results posted on the KCBS Events pages up to November of 2018.

### Data Overview
This dataset includes four tables: competitions, teams, results and competition web pages.

### Competitions
Each row is a KCBS competition with some dimensional data like the prize value, date and location

### Results
Each row is a team's score and place rank within a category at a competition. The category 'overall' reflects their overall score and place rank at the competition.

### Teams
Each row is a team uniquely identified by their lower-cased name string (name_key). Dimensional data is not broadly available for teams on the KCBS website but some can be derived from competition+result data (ie a guess at the team's 'home state').

### Competition Web Pages
Further competition meta-data from the KCBS events pages including the URL and year/month/country slugs of the containing search page.

## Competition Domain Knowledge
### Competition Format
A standard KCBS competition consists of four rounds/categories: chicken, pork ribs, pork, and brisket. Judges are divided into tables with six judges at each table. Efforts are made to evenly distribute judges based on their level of experience (competitions judged).

Judging proceeds with one round for each category. In a standard competition the rounds are ordered: chicken, pork ribs, pork and brisket. Within a round, each table of judges receives entries from six teams. Efforts are made to have each team judged by a different table of judges in each category. Judging is blind.

Non-standard competitions may include additional categories or exclude main categories and may not calculate the overall score as a combination of the four main categories.

### Scoring System
An entry is scored on three dimensions: appearance, taste and texture. Nine is 'excellent', eight is 'very good', seven is 'above average', six is 'average', five is 'below-average' and the list goes on. A one is a penalty, and can only be given after consulting a KCBS representative.

Judges are inclined to avoid scoring below a six unless there was an obvious problem with an entry. Teams spend substantial sums on supplies and judges, while volunteers, are eating for free. Judges are encouraged to fill out comment cards for flawed entries.

A team's final score in a single category is calculated by a sum of weighted judge scores with the lowest score thrown away. A team's overall score is (typically) the sum of their four category scores. Unweighted judge scores can be used to break ties, and if there is still a tie, the lowest score is brought back into the equation.


## Scoring Breakdown
### Score Range:
* Appearance: 0 : 9
* Taste: 0 : 9
* Tenderness: 0 : 9

        Score Weighting

        (appearance × .56) + (taste × 2.2972) + (tenderness × 1.1428)

        Maximum Single Judge Score:

        (9 × .56) + (9 × 2.2972) + (9 × 1.1428) = 36

        Maximum Category Score:

        (6 - 1) judges × 36 points = 180
        
        Maximum Standard Overall Score:

        4 categories × 180 points = 720

# All Data is from 2007-2018 KCBS competitions.

## Personal Background 

> Growing up my dad did the American Royal a KCBS competition in my hometown. I always loved watching him and others cook some of the best BBQ in the United States at one of the biggest competitions. I was always curious about the geographic and statistical underlying of the competition and this project helped me to understand the competition and learn more about python and its associated data science libraries.

## KC BBQ Heatmap

> This takes all of the information based on state frequency and generates a heatmap that shows number of KCBS competitions states with associated color scale.

## Average KCBS Competition Location
> This takes all of the cities given in the dataset and converts them into coordinates and then reads through the list of latitude and longitude coordinates taking an average to find the average location of KCBS coordinates and plotting that on a map with Plotly

## Kansas KCBS Competition Months Bar Chart
> My dad would always compete in late september and early october and I would remember eating barbeque on chilly nights nad enjoyed watching him compete. I Wanted to see when a majority of Kansas' KCBS competitions were and used matplotlib to chart the data

## Meat Scores Bar Chart Comparison
> My father would always cook sausage and I wanted to see how other meats scored. This uses matplotlib and pandas to analyze the dataset and generate a bar chart to compare outputs.


