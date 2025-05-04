# AB-Campaign-Testing
Campaign AB Testing

Dataset
Due to file size constraints, the dataset is not included in this repo.
You can download it here:[https://www.kaggle.com/datasets/manishabhatt22/marketing-campaign-performance-dataset]

📊 Statistical Testing Summary This project evaluates whether different marketing channels lead to different conversion rates, using both frequentist testing and causal inference.

🔹 A/B Testing (Email vs. Google Ads) T-test (on raw conversion rates):

p = 0.7544 → ❌ Not significant

📉 Average conversion rates between Email and Google Ads are not statistically different

Cohen’s d (effect size):

d = 0.0024 → ⚠️ Extremely small

Even if significant, the difference is not practically meaningful

Z-test (binary conversion ≥ 10%):

p = 0.6148 → ❌ Not significant

📊 Both channels had exactly the same number of “converted” users (13,264)

✅ Conclusion: No statistically or practically significant difference between Email and Google Ads

🔹 Causal Inference (Propensity Score Matching) After matching users with similar characteristics (e.g., segment, location):

ATE (Google Ads – Email) = +0.0009

p-value = 0.0032 → ✅ Statistically significant

📌 However:

The estimated improvement in conversion rate is just +0.09%

Not large enough to influence a business decision

✅ Conclusion: While matched analysis detects a very small lift for Google Ads, the effect size is too minor to justify favoring one over the other

🔹 Multi-Channel Testing (All 6 Channels) ANOVA (mean comparison):

p = 0.7159 → ❌ No significant differences across channels

Tukey HSD (pairwise test):

All reject = False → ❌ No pairwise differences significant

✅ Conclusion: Across Email, Google Ads, YouTube, Instagram, Facebook, and Website, no channel significantly outperforms the others in terms of conversion rate

🧠 Final Takeaway All marketing channels perform similarly in this dataset. No statistically significant or practically important difference in conversion rate was found. This suggests that campaign success may be driven more by creative, targeting, or timing than the channel itself.
