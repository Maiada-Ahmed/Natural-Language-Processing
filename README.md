# Natural-Language-Processing

## Sentiment Analysis on Amazon Product Review:
The rapid growth of the internet helped spread electronic commerce, resulting in a shift from the traditional Brick and Mortar business model to purchasing directly through the internet. Moreover recently, there has been even more demand for online shopping due to the spread of covid-19, all the restrictions imposed on people movement and limitations on markets footfall. Over time, online shopping has evolved and is available now in many types such as online marketplaces like Amazon and social media. This flexibility allowed consumers to be aware of the product characteristics and quality before purchasing. In addition, product reviews written by the consumers play a significant role in the decision making, buying experience and shopping satisfaction since reviews are available for most kinds of products, even those unique ones. Hence, consumers tend to make buying decisions mainly based on other consumers' reviews and are influenced a lot by the reviews and those who wrote these reviews since they represent an actual experience. For that reason, E-commerce retailers have acknowledged how critical product reviews are since they can help to boost sales and enhance the product by extracting insights about customers' needs and concerns (AlZu’bi et al. 2019).

On the other hand, product reviews became a vital part of the online store's business model beyond branding and marketing since they can provide insights on the performance of other areas of the company from the customer's point of view. Accordingly, many ideas were introduced to ensure consumers are exposed to the most valuable reviews, either by allowing users to vote for any given review as helpful or unhelpful or by using a rating system on reviews. Natural Language Processing (NLP) has been an academic discipline for many decades and made its way in the last 5-10 years to adoption beyond academia in different industries and various applications or use cases such as sentiment analysis that helps convert unstructured text data (i.e. customer interactions, social media comments or reviews) into meaningful insights (Jurafsky & Martin 2014).

Sentiment analysis is one of the most common types of text classification that automatically indicates people's emotions towards something, whether it is positive, negative or neutral. In this coursework the focus was on predicting the sentiment for Amazon product reviews using supervised learning techniques.

## Dataset: Description of the Selected Dataset:
After careful research and based on relevancy to the topic of NLP, the "The Multilingual Amazon Reviews Corpus" was identified and acquired. The dataset is available from AWS (Amazon website) as open-source data on the following link (here). To examine the license and availability to use, from the following link (here).

It is a consumer-facing dataset capturing a consumer opinion or attitude towards products sold in Amazon, and the dataset is part of "Multilingual Amazon Reviews Corpus" (MARC), a collection of Amazon reviews covering various languages such as Japanese, Spanish, Chinese, English and French. In the dataset each language is represented with 3 different json files, train, test and development. The focus of this coursework is to analyse the English language corpus since the understanding of the language would make it more efficient to pre-process, normalise and model. However, it is expected that the model can be applied in the same way to other languages. These reviews were collected in the period from 2015 to 2019, and the dataset consists of 200,000 records for the train category set and 5,000 records equally for both development and test datasets. They are merged together in a one dataframe for two reseaons, first, to apply the pre-processing in all the dataset. Second, to utilise the train_test_split function in sklearn and split the data into 80/20, as the default dataset split is 2.5% for each test and development from the total dataset which seems quite small to test on that size (Keung et al. 2020).

The acquired data covers 31 different product categories such as apparel, automotive, beauty, book, camera and many more. Each record contains all the required information such as the review text, the review title, the star rating, an anonymised reviewer ID. In total, a record will have eight attributes in the columns (review id, product id, reviewer id, stars, review body, review title, language, product category) with string data types for all of them except the rating variable is an integer. The product id and language were dropped as it is just redundant. Moreover, review body and review title were merged together since the title has some insights which can lead to the sentiment of the review body.
