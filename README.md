---
layout: default
title: "The biases behind rating: Uncovering the hidden influences in beer ratings"
---

# **The Biases Behind Rating: Uncovering the Hidden Influences in Beer Ratings**

## **Introduction**

The world of beer reviews is rich with data, offering insights into consumer preferences and biases. The main goal of any rating app is to provide **objective scores**, helping users navigate a world of choices. However, ratings are inherently **subjective**, shaped by the biases and perceptions of reviewers.

In this data story, we explore the various biases that influence beer ratings, ranging from **time-related trends** to **cultural and naming biases**. By identifying these influences, we propose adjustments that enhance the objectivity and accuracy of ratings.

---

## **The Key Questions**

Our analysis focuses on the following critical questions:

1. **Temporal Trends**: How do ratings change over time? Are there seasonal variations or spikes linked to events or holidays?
2. **Anchoring Effects**: Do early ratings significantly impact subsequent ones? Are reviewers biased by the first few scores?
3. **Cultural Biases**: Do reviewers rate domestic beers more favorably than international ones? How does beer consumption per capita influence ratings?
4. **Naming Bias**: Does a beer's name set expectations that influence its rating?

---

## **Datasets and Methodology**

### **Datasets**
1. **BeerAdvocate Dataset**: Comprising ratings, user information, and brewery details.
2. **Beer Consumption Data**: Total and per capita beer consumption by country (sourced from World Population Review).

### **Methodology**
- **Temporal Analysis**: We examined ratings over time, looking for patterns or anomalies related to holidays or events. Using monthly and yearly aggregations, we calculated average ratings and identified significant disparities.
- **Anchoring Effect**: Correlation tests (Pearson and Spearman) were used to measure the relationship between the first few ratings and overall ratings.
- **Cultural Bias**: Ratings were categorized into domestic and international groups, with t-tests and mean comparisons performed. We correlated beer consumption per capita with average ratings.
- **Naming Bias**: Text analysis was used to extract keywords from beer names. Statistical tests (e.g., Chi-square) identified associations between specific words and rating trends.

---

## **Findings**

### **1. Temporal Trends**

#### **Figure 1: Ratebeer Dataset**
![Average Rating per Year (Ratebeer Dataset)](assets/img/Average%20Rateing%20per%20Year%20Ratebeer.png)

**Observation**:  
The chart shows the average rating starts at **3.25** in 2000, dips slightly, and then steadily increases, reaching **3.40** by 2017.

**Analysis**:  
- **Upward Trend**: Ratings increase over the years, suggesting improvements in beer quality or shifts in consumer behavior.
- **Initial Dip**: Early ratings (2000–2002) may reflect stricter evaluations or fewer beer options.
- **Industry Evolution**: The rise of craft beer in the mid-2000s likely contributed to higher ratings.

---

#### **Figure 2: BeerAdvocate Dataset**
![Average Rating per Year (BeerAdvocate Dataset)](assets/img/Average%20Rating%20per%20Year%20BeerAdvocate%20dataset%20.png)

**Observation**:  
The chart shows a spike in ratings around 2000 (>4.0), followed by a sharp decline, and a steady upward trend after 2005.

**Analysis**:  
- **Sharp Spike**: The unusually high rating in 2000 may reflect a small sample size or generous early users.
- **Decline and Recovery**: Ratings drop as more beers are rated but recover post-2005, reflecting better beer quality.
- **Comparison**: The BeerAdvocate dataset exhibits more fluctuations than the Ratebeer dataset.

---

### **2. Anchoring Effect**

#### **Figure 3: Correlation Analysis**
![Correlation Analysis](assets/img/Correlation%20between%20first%20and%20other%20rating.png)

**Observation**:  
The scatterplot shows a **strong positive correlation** between first and subsequent ratings, with a densest cluster near **4.0–4.5**.

**Analysis**:  
- **Anchoring Effect**: Early ratings heavily influence subsequent reviews, introducing bias.
- **Impact on Objectivity**: This bias over-represents early opinions, suggesting a need to reduce the weight of initial ratings.

---

### **3. Cultural Bias**

#### **Figure 4: Histogram of Domestic Ratings**
![Histogram of Domestic Ratings](assets/img/Histogram%20of%20Domestic%20Ratings.png)

**Observation**:  
Most domestic beers have fewer than **100 ratings**, with a long tail for highly rated beers.

**Analysis**:  
- **Bias in Domestic Ratings**: A few popular domestic beers dominate the average.
- **Recommendation**: Normalization techniques can ensure fair representation for less-rated beers.

---

#### **Figure 5: Histogram of International Ratings**
![Histogram of International Ratings](assets/img/Histogram%20of%20International%20Ratings.png)

**Observation**:  
International beers have a broader distribution, with more beers receiving **>1,000 ratings** compared to domestic beers.

**Analysis**:  
- **Popularity Disparity**: International beers have a wider consumer base, leading to more reviews.
- **Cross-Country Comparisons**: Rating volume differences highlight the need for normalization across countries.

---

### **4. Naming Bias**

#### **Figure 6: Comparison Analysis**
![Comparison Analysis](assets/img/Camparison%20between%20the%20first%20rate%20and%20the%20following%20rate%20me.png)

**Observation**:  
The first rating is consistently higher than the mean of subsequent ratings, indicating an **optimism bias**.

**Analysis**:  
- **Expectation vs. Reality**: Early reviewers may give higher ratings due to enthusiasm or appealing beer names.
- **Recommendation**: Platforms could anonymize beer names for early reviewers to reduce this bias.

---

## **Key Insights**
1. **Temporal Trends**:  
   - Both datasets show an upward trend in ratings, influenced by industry growth and consumer preferences.
2. **Anchoring Effect**:  
   - Early ratings strongly bias overall scores, requiring adjusted weightings for objectivity.
3. **Cultural Bias**:  
   - Domestic beers are rated more favorably, reflecting cultural preferences. Normalization is necessary for fair comparisons.
4. **Naming Bias**:  
   - Optimistic early ratings are influenced by beer names, suggesting anonymization as a solution.

---

## **Conclusion**

This analysis reveals that beer ratings are shaped by multiple biases, including temporal trends, anchoring effects, cultural preferences, and naming influences. Addressing these biases through normalization, weighting adjustments, and anonymization can lead to more objective ratings, benefiting both consumers and breweries.

