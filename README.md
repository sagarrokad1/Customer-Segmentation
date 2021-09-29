# Customer-Segmentation

## PROBLEM STATEMENT

In this project, our task was to identify major customer segments on a
transnational data set which contained all the transactions occurring
between 01/12/2010 and 09/12/2011 for a UK-based and registered
non-store online retail.The company mainly sells unique all-occasion gifts.
Many customers of the company are wholesalers.

## APPROACH

### Data Pre-Processing:
  ● Before diving into insights from the data, we removed duplicate
    entries from the data. The data contained 5268 duplicate entries (about ~1%).

  ● We had also removed the ones where CustomerID values were NaNs.

  ● As per the data, if the invoice number code starts with the letter ‘c’, it
    shows a canceled order.All the canceled orders contain negative
    quantities (since it was a cancellation) and hence were removed from
    the data.

### Exploratory Data Analysis:-

We performed exploratory data analysis to get insights from the data to
observe following things:-
  1. The United Kingdom and Saudi Arabia had the highest and lowest
  occurrences in the dataset.
  2. Month of November had the highest sales. Similarly, on weekdays
  Thursday had the highest sale.
  3. The store had good sales in the first week of the month, specifically
  on the 4th day. As we go towards the month end, the sales start
  declining.
  4. Maximum sales happened on Thursdays and Wednesdays around 12
  PM to 4 PM
  5. Most frequently used item was PAPER CRAFT,LITTLE BIRDIE, and the
  least used item was CAPIZ CHANDELIER.
  6. Most purchased item is WHITE HANGING HEART T-LIGHT HOLDER
  and Least purchased item was FRYING PAN RED POLKADOT.
  7. The percentage of repeat customers was substantially more than the
  percentage of one time customers.
  
### RFM Segmentation:

RFM stands for Recency, Frequency, and Monetary. RFM analysis is a
commonly used technique to generate and assign a score to each
customer based on how recent their last transaction was (Recency), how
many transactions they have made in the last year (Frequency), and what
the monetary value of their transaction was (Monetary).

### Models Implementation:-

### Clustering:

  #### Clustering with K-means (Elbow method):
  First, we had used an elbow method to find out the best
  possible no. of clusters for our dataset and got (no. of
  clusters)K=3.

  #### Clustering with K-means (Silhouette analysis):
  For our dataset we found out that the best possible average silhouette
  score is 0.39 which was for K=2.

  #### Hierarchical Clustering:
  Hierarchical Clustering clustering uses a Dendrogram technique for
  choosing the best possible cluster.
  So after implementing it we found out that the best possible cluster
  according to our given dataset was K=2.

### Conclusion:

  ● High monetary and more frequent(Target customer):- These
  were those customers who had good Recency, Frequency,
  Monetary, as from the hierarchical cluster plot the blue patches
  were representing those target customers.
  ● High monetary value but less frequent: These customers were
  coming very less in the store but whenever they came they were
  spending a huge amount of money.
  ● Low monetary value but more frequent(Careful): These
  customers were coming so frequently to the store but spending
  quite less.
  ● Low monetary and less frequent: These were the customers
  who were not the good for the store because they are spending
  less and are less frequent.
  ● So after doing customer segmentation we can say the company should
  focus on High monetary and more frequent customers(Target customer)
  and apart from that they can also focus on High monetary value but less
  frequent customers by giving lucrative offers and coupons.
