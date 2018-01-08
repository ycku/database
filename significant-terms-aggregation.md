---
tags: Graph Database
---

# Significant Terms Aggregation[^1]

本篇編譯自 ElasticSearch Graph，可以從實務面瞭解 Graph 的應用情況。

回傳文件集合中有趣或不常見的詞語集合。

應用範例：

* Suggesting "H5N1" when users search for "bird flu" in text
* Identifying the merchant that is the "common point of compromise" from the transaction history of credit card owners reporting loss
* Suggesting keywords relating to stock symbol $ATI for an automated news classifier
* Spotting the fraudulent doctor who is diagnosing more than his fair share of whiplash injuries
* Spotting the tire manufacturer who has a disproportionate number of blow-outs

In all these cases the terms being selected are not simply the most popular terms in a set. They are the terms that have undergone a significant change in popularity measured between a_foreground_and_background_set. If the term "H5N1" only exists in 5 documents in a 10 million document index and yet is found in 4 of the 100 documents that make up a user’s search results that is significant and probably very relevant to their search. 5/10,000,000 vs 4/100 is a big swing in frequency.

---



[^1]:  [Significant Terms Aggregation \| Elasticsearch Reference \[6.1\] \| Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/6.1/search-aggregations-bucket-significantterms-aggregation.html)

