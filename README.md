# Market-Basket-Analysis-
#### I’ve created a blog on the crucial topic of decoding consumer behavior using MBA. For a detailed understanding of the project, I recommend reading it as it provides an in-depth explanation. Below, I’ll highlight some key points, but for the full version, please visit the blog through the link:
Read the blog here: https://medium.com/@shivtalati99/decoding-consumer-behavior-mba-248c7ae68bd0

Association Rule Mining

Association rule analysis is a technique used in data mining to discover relationships or associations between variables in large datasets. It's most commonly applied in the context of market basket analysis to find out which products tend to be bought together.

**Market Basket Analysis** - Is a technique used by large retailers to uncover associations between items. It works by looking for combinations of items that occur together frequently in transactions, providing information to understand the purchase behavior. The outcome of this type of technique is, in simple terms, a set of rules that can be understood as “if this, then that”.

**Support:** Support is an indication of how frequently the itemset appears in the dataset.
Support is a so-called frequency constraint. Its main feature is that it possesses the property of down-ward closure which means that all sub sets of a frequent set (support > min. support threshold) are also frequent. This property (actually, the fact that no super set of a infrequent set can be frequent) is used to prune the search space (usually a tree of item sets with increasing size) in level-wise algorithms (e.g., the APRIORI algorithm). The disadvantage of support is the rare item problem. Items that occur very infrequently in the data set are pruned although they would still produce interesting and potentially valuable rules.

**Confidence:** Confidence is an indication of how often the rule has been found to be true.
Confidence is not down-ward closed and was developed together with support (the so-called support-confidence framework). While support is used to prune the search space and only leave potentially interesting rules, confidence is used in a second step to filter rules that exceed a min. confidence threshold. A problem with confidence is that it is sensitive to the frequency of the consequent (Y) in the data set. Caused by the way confidence is calculated, Ys with higher support will automatically produce higher confidence values even if they exists no association between the items.

**Lift:** The ratio of the observed support to that expected if X and Y were independent.
Leverage measures the difference of X and Y appearing together in the data set and what would be expected if X and Y where statistically dependent. The rational in a sales setting is to find out how many more units (items X and Y together) are sold than expected from the independent sells. Using min. leverage thresholds at the same time incorporates an implicit frequency constraint. E.g., for setting a min. leverage thresholds to 0.01% (corresponds to 10 occurrence in a data set with 100,000 transactions) one first can use an algorithm to find all itemsets with min. support of 0.01% and then filter the found item sets using the leverage constraint. Because of this property leverage also can suffer from the rare item problem.
