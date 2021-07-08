# Predict-Future-Sales 

# Data Description-
  The task is to forecast the total amount of products sold in every shop for the test set. Creating a robust model that can handle such situations is part of the challenge.

# File Descriptions
  - sales_train.csv - the training set. Daily historical data from January 2013 to October 2015.
  - test.csv - the test set. You need to forecast the sales for these shops and products for November 2015.
  - sample_submission.csv- a sample submission file in the correct format.
  - items.csv- supplemental information about the items/products.
  - items_categories.csv- supplemental information about the items categories.
  - shops.csv- supplemental information about the shops.
  
# Data Fields
  - ID- an Id that represents a (Shop,item) tuple within the test set.
  - shop_id- unique identifier of a shop.
  - item_id- unique identifier of a product.
  - item_category_id- unique identifier of item category.
  - item_cnt_day- number of products sold. You are producting a monthly amount of this measure.
  - item_price- current price of an item.
  - date- date in format dd/mm/yyyy
  - date_block_num- a consecutive month number, used for convenience.January 2013 is 0,February 2013 is 1...,October 2015 is 33.
  - item_name- name of item
  - shop_name- name of shop
  - item_category_name - name of item category
  
Lets first discuss what we are given & what we have to predict-

training data-
   1.date- every date of items sold
   2.date_block_num - this number given to every month.
   3.shop_id- unique number of every item.
   4.item_id- unique number of every item.
   5.item_price- price of every item.
   6.item_cnt_day-number of items sold on a particular day.
   
testing data-
   1.ID- unique for every (shop_id,item_id)pair.
   2.shop_id- unique number of every shop.
   3.item_id- unique number of every item.
   
Now what we have to predict?we have to predict how many items of a type from each shop will be sold in whole month. Our submission should have ID & item_cnt_month columns.

