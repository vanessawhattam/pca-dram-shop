# ADA: Dram Shop PCA

In this assignment we use PCA to investigate purchasing habits of Dram Shop customers. Since the Dram Shop has so many items, we need dimensionality reduction to help us understand the patterns of consumption. This assignment does not start you with any code, so you'll need to create a Jupyter notebook to hold your analysis. 


Here are the steps you'll undertake: 

1. Write a query in GBQ that pulls the data in the view `vw_customers_top_1k_items`. This view has the customer identifier 
  and the customer's history with the item. This view is limited to the top 1000 items in terms of total spend, though you could
  easily modify things for your purpose. You may want to collapse this to "clean_item_name" instead of "catalog_object_id" to reduce the processing time. 
1. Using the pandas function `pivot`, pivot the data into a "wide" format with customer IDs as the rows and beverages as the items. You can see an example [here](https://stackoverflow.com/questions/22798934/pandas-long-to-wide-reshape-by-two-variables). 
1. Using the `PCA` function from `sklearn.decomposition`, perform a PCA on this data set. Plot the amount of explained variation in the first 20 components.
1. For each of the first 6 components, print the items with the 15 largest loadings in absolute value. 
1. Write up a brief interpretation on what aspect of the data that component seems to be capturing.

