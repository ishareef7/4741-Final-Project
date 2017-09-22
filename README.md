# Predicting Repeat Buyers
Project Proposal (ORIE 4741 Project by Hao Rong (hr335), Frank Zhang (fz252), Ishmail Grady (isg9))


# Problem Statement
Merchants usually run promotions on particular dates in order to attract a large number of new buyers. However, many of the attracted buyers are one-time buyers, and these promotions may have little long lasting impact on sales. To help merchants promote their strategy, it is important to identify which customers may be potential repeat buyers. This can greatly reduce the promotion cost and enhance the return on investment by concentratiing marketing efforts. Customer targeting is very challenging, especially for fresh buyers. 
We want to try to solve this problem by building prediction model on the long-term user behavior log providing by Tmall.com. It contains a set of information of merchants, buyers and the commercial behavior during the promotion on the "Double 11" day. We want to predict the probability that the new buyers of certain store would purchase items from the same merchants again within 6 months.

# Dataset Description 
The data set contains anonymized users' shopping logs in the past 6 months before and on the "Double 11" promotion day, and the label information indicating whether they are old buyers, new one-time buyer or new repeated buyers. Data is sampled in a biased way by Tmall due to privacy consideration. But it is still useful to make inference and prediction on these data (Data source: Tianchi competition dataset)
	
	
| Data Fields | Description |
|--------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| user_id | A unique id for the shopper. |
| age_range | User' s age range: <18; [18:24]; [25:29]; [30:34]; [35:39]; [40:49]; >=50; unknown. |
| gender | User' s gender: female, male, unknown. |
| merchant_id | A unique id for the merchant. |
| label | Value from {0, 1, -1}. ' 1' denotes ' user_id' is a repeat buyer for ' merchant_id' ,  while ' 0' is the opposite. ' -1' represents that ' user_id' is not a new customer of  the given merchant, which means they already bought things 6 month ago. |
| activity_log | Set of interaction records between {user_id, merchant_id}, where each record is  an action represented as ' item_id:category_id:brand_id:time_stamp:action_type'.  (Category_id is a unique id for the category that the item belongs to. Brand_id is  a unique id for the brand of the item. Action type includes four actions: click,  add-to-cart, purchase, add-to-favourite.) |
