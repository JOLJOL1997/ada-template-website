# The biases behind rating: Uncovering the hidden influences in beer ratings

Introduction
The world of beer reviews is rich with data, offering insights into consumer preferences and biases. The main goal of any rating app is to provide objective scores, helping users navigate a world of choices. However, ratings are inherently subjective, shaped by the biases and perceptions of reviewers. In this data story, we explore the various biases that influence beer ratings, ranging from time-related trends to cultural and naming biases. By identifying these influences, we aim to propose adjustments that can enhance the objectivity and accuracy of ratings.

The Key Questions
Our analysis focuses on the following critical questions:

Temporal Trends: How do ratings change over time? Are there seasonal variations or spikes linked to events or holidays?
Anchoring Effects: Do early ratings significantly impact subsequent ones? Are reviewers biased by the first few scores?
Cultural Biases: Do reviewers rate domestic beers more favorably than international ones? How does beer consumption per capita influence ratings?
Naming Bias: Does a beer's name set expectations that influence its rating?

Datasets and Methodology
To answer these questions, we analyzed a combination of datasets, including:

BeerAdvocate Dataset: Comprising ratings, user information, and brewery details.
Beer Consumption Data: Total and per capita beer consumption by country (sourced from World Population Review).
Our methodology involved the following steps:

Temporal Analysis: We examined ratings over time, looking for patterns or anomalies related to holidays or events. Using monthly and daily aggregation, we calculated average ratings and identified significant disparities.
Anchoring Effect: Correlation tests (Pearson and Spearman) were used to measure the relationship between the first few ratings and overall ratings. We also explored the role of textual reviews in amplifying anchoring effects.
Cultural Bias: By categorizing ratings into domestic and international groups, we performed t-tests and mean comparisons. We also correlated beer consumption per capita with average ratings, accounting for country biases.
Naming Bias: Using text analysis, we extracted keywords from beer names and conducted sentiment analysis. Statistical tests (e.g., Chi-square) were applied to identify associations between specific words and rating trends.

Finding


1: Average Rating per Year (Ratebeer Dataset)
Observation:
The chart shows that the average rating starts at around 3.25 in the year 2000, then experiences a slight drop before steadily increasing over time. By 2017, the average rating reaches approximately 3.40, indicating a clear upward trend.

Analysis:

Upward Trend: The gradual increase in ratings over the years suggests that beers are either improving in quality or that consumer expectations and rating behaviors have shifted positively.
Initial Dip: The small dip in early years (2000–2002) may reflect stricter ratings or fewer beer varieties available in the market during that period.
Industry Evolution: This trend aligns with the growth of the craft beer industry, which gained popularity in the mid-2000s, potentially contributing to higher ratings as more unique and quality beers entered the market.

2: Average Rating per Year (BeerAdvocate Dataset)
Observation:
The chart begins with an average rating near 3.85 in 1995. A significant spike occurs around 2000, where the average rating exceeds 4.0, followed by a sharp decline to below 3.75. After 2005, ratings gradually rise again, reaching over 3.95 by 2017.

Analysis:

Sharp Spike in 2000: The unusually high average rating in 2000 may indicate a small sample size or the presence of exceptionally well-rated beers. Alternatively, early adopters of the platform may have been more generous with their scores.
Decline and Recovery: The drop post-2000 could reflect the growing diversity of beers being rated, as more average-quality beers entered the market. The recovery after 2005 suggests improvements in beer quality or shifts in consumer preferences.
Long-Term Growth: The steady upward trend post-2005 reflects the maturing of the beer industry and an increasing number of premium craft beers that resonate with consumer tastes.
Comparison of the Two Charts
Both datasets show an upward trend in average ratings over time, indicating overall improvements in beer quality or changes in consumer behavior.
The BeerAdvocate dataset exhibits more fluctuation, particularly around the year 2000, possibly due to differences in user demographics, sample size, or platform-specific rating behaviors.
The Ratebeer dataset shows a more consistent trend, with smaller deviations and a steady increase.



## Figure 3：Correlation Analysis
![Correlation Analysis](assets/img/Correlation%20between%20first%20and%20other%20rating.png)
3. Correlation Between First and Other Ratings
Observation: The scatterplot shows a strong positive correlation between the first rating and subsequent ratings, with a regression line indicating consistency across ratings. The densest cluster is near higher ratings (e.g., 4.0–4.5), suggesting most beers initially receive favorable scores.

Analysis:

Anchoring Effect: The high correlation demonstrates the anchoring effect, where the first rating significantly influences subsequent ratings. Users are likely influenced by the initial rating, either consciously or subconsciously.
Impact on Objectivity: This effect introduces bias, potentially over-representing early opinions. It highlights the need for algorithms to reduce the weight of initial ratings when calculating averages.

4. Histogram of Domestic Ratings
## Figure 4：Histogram of Domestic Ratings
![Histogram of Domestic Ratings](assets/img/Correlation%20between%20first%20and%20other%20rating.png)
Observation: The histogram shows that most domestic beers have low rating counts, with a steep decline as the count increases. The majority of beers have fewer than 100 ratings, with a long tail for those with higher popularity.

Analysis:

Bias in Domestic Ratings: The sharp skew suggests that only a few domestic beers are widely rated, which may lead to an overrepresentation of highly rated beers in domestic averages.
Recommendation: To address this bias, normalization techniques could ensure less-rated beers don’t disproportionately impact the overall perception of domestic beers.

5. Histogram of International Ratings
## Figure 5：Histogram of International Ratings 
Observation: Similar to domestic ratings, the histogram of international ratings is highly skewed, with most beers having low rating counts. However, the number of beers with higher rating counts (e.g., >1,000) is more prominent than in domestic ratings.

Analysis:

Popularity Disparity: International beers appear to receive more reviews on average, possibly due to a wider consumer base or broader availability.
Cross-Country Comparisons: This disparity in rating volume can skew comparisons between domestic and international ratings. Countries with large populations or high beer consumption might dominate the dataset.

6. Comparison Between the First Rating and the Following Rating Mean
## Figure 6：Comparison Analysis
![Comparison Analysis](assets/img/Camparison%20between%20the%20first%20rate%20and%20the%20following%20rate%20me.png)
Observation: The bar chart compares the first rating with the mean of subsequent ratings for specific beers. For all beers, the first rating is either higher or comparable to the average of following ratings.

Analysis:

Expectation vs. Reality: The trend where initial ratings are consistently higher indicates an optimism bias, where early reviewers rate products higher, possibly due to enthusiasm or expectation setting.
Recommendation: Platforms could consider adjusting for this discrepancy by tracking how ratings evolve over time and highlighting more balanced, recent ratings.


Research Questions and Corresponding Analyses
How does time influence the ratings? Are there trends that bias the ratings, and can we link them to holidays or festivals?
Visualizations:
Average Rating per Year (Ratebeer Dataset)
Average Rating per Year (BeerAdvocate Dataset)
Findings:
Both datasets show a positive trend in ratings over the years, indicating that either beer quality has improved or consumer rating behaviors have shifted.
The BeerAdvocate dataset shows higher variability, including a significant spike around 2000, potentially reflecting smaller sample sizes or differing user demographics.
The Ratebeer dataset exhibits a steadier upward trend, suggesting consistent improvements in beer ratings over time.
Conclusion: Time introduces a bias toward higher ratings, possibly reflecting market evolution, better beer quality, or shifting consumer preferences. Future research could link these trends to specific events, such as craft beer growth or cultural festivals.
What is the influence of the first (or first few) ratings on the final rating? Are future reviewers biased by these first ratings?
Visualization: Correlation Between First and Other Ratings
Findings:
A strong positive correlation exists between the first ratings and subsequent ratings. This demonstrates the anchoring effect, where early ratings heavily influence future scores.
The densest cluster near higher ratings suggests that initial reviews often set a favorable precedent for others.
Conclusion: Early ratings significantly bias subsequent reviews. Platforms could implement algorithms to reduce the weight of initial reviews in overall averages to enhance objectivity.
Do people rate beers from their country differently than the rest of the world? Do high-beer-consumption countries rate beers more favorably?
Visualizations:
Histogram of Domestic Ratings
Histogram of International Ratings
Findings:
Domestic ratings are highly skewed, with most beers receiving fewer than 100 reviews, indicating that a few popular domestic beers dominate the averages.
International ratings show a broader distribution, with more beers receiving higher counts of reviews (>1,000), suggesting a larger consumer base or wider availability.
Domestic beers often receive slightly higher ratings, reflecting cultural bias or preference for familiar products.
Conclusion: Ratings are influenced by cultural bias, with domestic beers often rated more favorably. Additionally, differences in review volume between domestic and international beers highlight the need for normalization in comparisons.
Does the beer’s name influence the final rating of consumers?
Visualization: Comparison Between the First Rating and the Following Rating Mean
Findings:
Early ratings are consistently higher than the average of subsequent ratings, suggesting an optimism bias driven by initial expectations. This could also be influenced by positive or appealing beer names setting a favorable tone for reviews.
Conclusion: Beer names, along with early ratings, create a bias toward higher initial scores. Platforms could experiment with anonymizing beer names during early reviews to reduce this effect.
Key Insights Across All Visualizations
Temporal Trends:

Both datasets show a clear upward trend in ratings over the years, influenced by the evolution of the beer market, growing consumer awareness, and shifts in preferences.
Anchoring Effect:

The strong correlation between early and subsequent ratings highlights the anchoring effect, which biases overall scores. This effect is further amplified by textual reviews and possibly the beer's name.
Cultural Bias:

Domestic beers tend to receive higher ratings, reflecting cultural preferences. Normalization across domestic and international ratings is necessary for fair comparisons.
Rating Distributions:

Both domestic and international ratings are highly skewed, with a few beers receiving most reviews. This emphasizes the need to account for rating volume differences when analyzing trends.


