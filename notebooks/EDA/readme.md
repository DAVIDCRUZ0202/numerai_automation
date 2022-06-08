# Exploratory Data Analysis

### Note

This data is not available in the repo because it is massive. Just go to [numer.ai](numer.ai) and click `download`. Once your data is downloaded, just move the `numerai_training_data.csv` file to your local space, and you're good to go!
<img src="assets\download_data.png" alt="download_data" width="400" height="400">

# EDA Summary

Here's the quick and fast: The data is obfuscated(masked), and also fully cleaned, normalized, centered. This means that the data is ready to be worked on with machine learning models right away. For due diligence and proof of this, I'll share some visuals and outcomes of some of my analysis. As always, you can read through the notebook to see more details.

* The data has a uniform distribution of values for features, and a normal distribution of values for the target. There are no null values.

<img src="assets\1.summary_stats.png" alt="summary_stats" width="400" height="400">

* The `era` feature gives us a temporal quality to monitor, but it's still a highly complicated concept to further engineer in new and helpful ways. Here is a chart which shows the varying size of eras

<img src="assets\2.era_sizes.png" alt="era_sizes" width="400" height="400">

* Our `target` feature is normally distributed

<img src="assets\3.target_dist.png" alt="target_dist" width="400" height="400">

* also, the `target` is centered around it's mean

<img src="assets\4.target_centered.png" alt="target_centered" width="400" height="400">

* intra-feature correlations show us that features with similar prefixes have varying levels of correlation

<img src="assets\5.feature_corrs.png" alt="feature_corrs" width="400" height="400">

* A high level heatmap shows us that the data set is overall not correlated in any specific direction.

<img src="assets\6.heatmap.png" alt="heatmap" width="400" height="400">

To conclude, we can move on with machine learning, and with these foundations of what the data looks like, we can easily come back to iterate on our work and create more engineered features.
