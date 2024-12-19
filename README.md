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
## Figure 1：Correlation Analysis
![Correlation Analysis](assets/img/Correlation%20between%20first%20and%20other%20rating.png)


1. Correlation Between First and Other Ratings
Observation: The scatterplot shows a strong positive correlation between the first rating and subsequent ratings, with a regression line indicating consistency across ratings. The densest cluster is near higher ratings (e.g., 4.0–4.5), suggesting most beers initially receive favorable scores.

Analysis:

Anchoring Effect: The high correlation demonstrates the anchoring effect, where the first rating significantly influences subsequent ratings. Users are likely influenced by the initial rating, either consciously or subconsciously.
Impact on Objectivity: This effect introduces bias, potentially over-representing early opinions. It highlights the need for algorithms to reduce the weight of initial ratings when calculating averages.



2. Histogram of Domestic Ratings
Observation: The histogram shows that most domestic beers have low rating counts, with a steep decline as the count increases. The majority of beers have fewer than 100 ratings, with a long tail for those with higher popularity.

Analysis:

Bias in Domestic Ratings: The sharp skew suggests that only a few domestic beers are widely rated, which may lead to an overrepresentation of highly rated beers in domestic averages.
Recommendation: To address this bias, normalization techniques could ensure less-rated beers don’t disproportionately impact the overall perception of domestic beers.

3. Histogram of International Ratings
Observation: Similar to domestic ratings, the histogram of international ratings is highly skewed, with most beers having low rating counts. However, the number of beers with higher rating counts (e.g., >1,000) is more prominent than in domestic ratings.

Analysis:

Popularity Disparity: International beers appear to receive more reviews on average, possibly due to a wider consumer base or broader availability.
Cross-Country Comparisons: This disparity in rating volume can skew comparisons between domestic and international ratings. Countries with large populations or high beer consumption might dominate the dataset.

4.Comparison Between the First Rating and the Following Rating Mean
## Figure  4：Comparison Analysis
![Comparison Analysis](assets/img/Camparison%20between%20the%20first%20rate%20and%20the%20following%20rate%20me.png)
Observation: The bar chart compares the first rating with the mean of subsequent ratings for specific beers. For all beers, the first rating is either higher or comparable to the average of following ratings.

Analysis:

Expectation vs. Reality: The trend where initial ratings are consistently higher indicates an optimism bias, where early reviewers rate products higher, possibly due to enthusiasm or expectation setting.
Recommendation: Platforms could consider adjusting for this discrepancy by tracking how ratings evolve over time and highlighting more balanced, recent ratings.

Key Takeaways
Anchoring Effect: Early ratings heavily influence subsequent ones, highlighting the need for strategies to minimize this bias.
Domestic vs. International Ratings: The disparity in rating counts suggests the need to account for volume differences when making comparisons.
Skewed Distributions: Both domestic and international rating distributions are highly skewed, emphasizing the importance of normalizing data.
Optimism Bias in Early Ratings: Higher initial ratings suggest user bias, which platforms can address to provide more objective averages.


Conclusion
Our analysis reveals that beer ratings are shaped by a complex interplay of biases, from temporal and cultural influences to anchoring and naming effects. By understanding these biases, rating platforms can create more accurate and objective systems, providing consumers with reliable insights. This study is a step towards unraveling the hidden factors that shape consumer behavior, not just in beer ratings but across various domains.

Next Steps
Future work could explore additional biases, such as price perception or regional taste preferences, and apply similar methodologies to other product categories. Ultimately, the goal is to refine rating systems to reflect true consumer satisfaction.
