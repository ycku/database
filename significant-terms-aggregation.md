---
tags: Graph Database
---

# Significant Terms Aggregation[^1]

回傳文件集合中有趣或不常見的詞語集合。

> 本篇編譯自 ElasticSearch Graph，可以從實務面瞭解 Graph 的應用情況。

應用範例：

* 當使用者在搜尋「禽流感」（bird flu）時建議「H5N1」
* 從信用卡持卡人的交易歷史記錄中識別出「盜刷的共同點」
* 為自動新聞分類器建議與股票代碼 $ATI 有關的關鍵字
* Spotting the fraudulent doctor who is diagnosing more than his fair share of whiplash injuries
* Spotting the tire manufacturer who has a disproportionate number of blow-outs

In all these cases the terms being selected are not simply the most popular terms in a set. They are the terms that have undergone a significant change in popularity measured between a\_foreground\_and\_background\_set. If the term "H5N1" only exists in 5 documents in a 10 million document index and yet is found in 4 of the 100 documents that make up a user’s search results that is significant and probably very relevant to their search. 5/10,000,000 vs 4/100 is a big swing in frequency.

---

[^1]:  [Significant Terms Aggregation \| Elasticsearch Reference \[6.1\] \| Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/6.1/search-aggregations-bucket-significantterms-aggregation.html)

