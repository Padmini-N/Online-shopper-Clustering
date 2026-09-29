# Online Shoppers Clustering

Segmenting 12,330 e-commerce sessions into behavioural groups to find which visitors are worth targeting first, and when.

**Tools:** Python, pandas, scikit-learn (K-Means, PCA), SciPy (hierarchical clustering), matplotlib, seaborn

---

## Business problem

An online retailer gets thousands of website sessions but treats every visitor the same, so marketing effort is spread evenly across people with very different buying intent.

**The question:** which visitors are worth targeting first, and when?

## Data

- **Source:** [Online Shoppers Purchasing Intention Dataset](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset), UCI Machine Learning Repository
- **Size:** 12,330 sessions
- **Features:** page visits and time on page by page type, bounce and exit rates, page values, month, visitor type, weekend flag and whether the session ended in a purchase

See `data/README.md` for download instructions.

## Approach

1. **Prepare the data:** cleaned and encoded the session features and scaled them so no single measure dominates the clustering.
2. **Reduce dimensions:** used PCA to condense the behavioural features into the patterns that matter most.
3. **Cluster:** applied K-Means and hierarchical clustering to group visitors into behavioural segments.
4. **Profile the segments:** compared the clusters on engagement, page value and timing to describe who each group is.

## Insights

- Visitors split into **three distinct behavioural clusters**.
- **1,055 sessions** formed a high-intent group, the clearest target for conversion-focused campaigns.
- Activity **peaked in May and November**, so those are the months where campaign effort reaches the most engaged traffic.

<!-- Add charts once exported, for example:
![PCA clusters](images/pca_clusters.png)
![Monthly activity](images/monthly_activity.png)
-->

## Why it matters

Campaigns land better when you know who you are speaking to and when they are paying attention. The same segmentation and timing logic applies to targeting ads, planning content calendars, or choosing the right moment for a PR pitch.

## How to run

```
pip install -r requirements.txt
jupyter notebook
```

Open the notebook and run all cells. The CSV must be in `data/` first.

## Repository structure

```
online-shoppers-clustering/
├── README.md
├── online_shoppers_clustering.ipynb
├── requirements.txt
├── data/
│   └── README.md
└── images/
```

## Author

**Padmini (Mini) Nagesh**, Marketing & Media Data Analyst, Melbourne
[LinkedIn URL] | [Portfolio URL]
