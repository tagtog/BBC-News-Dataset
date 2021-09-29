### BBC News Classification

 * Text documents are one of the richest sources of data for businesses.

* This is a public dataset from the BBC comprised of 2225 articles, each labeled under one of 5 categories: business, entertainment, politics, sport, or tech.

* The dataset is broken into 1490 records for training and 735 for testing. The goal will be to build a system that can accurately classify previously unseen news articles into the right category.
* Website: https://www.kaggle.com/c/learn-ai-bbc/data

**Data fields**
* ArticleId - Article id unique # given to the record
* Article - text of the header and article
* Category - category of the article (tech, business, sport, entertainment, politics)

------

### This dataset in tagtog

The data for training and testing are uploaded to tagtog into the folders: train and test.

* In tagtog, the article text is upload in a .txt file. 
* The name of the file is article-id.txt and the file contains the text corresponding to that article-id. 
* Data field Category is the document label for text in tagtog for training records.
* Testing records do not have the document label.

**In the training sample, there were samples that were duplicates**.

**The final records in tagtog after removing the duplicates are**:
* [train](https://tagtog.net/ashishnarwal/BBC-News-Classification/pool%2Ftrain): 1439 (1490 - 51)
* [test](https://tagtog.net/ashishnarwal/BBC-News-Classification/pool%2Ftest): 684 (735 - 13 - 38)

Therefore, in total [this dataset in tagtog holds **2123 articles**](https://www.tagtog.net/ashishnarwal/BBC-News-Classification/-search/*) (train;1439 + test;684).

#### Details for duplicate removal

The 1st article-id is uploaded in tagtog and the 2nd article-id is a duplicate of the 1st. So, the file corresponding to the 2nd article-id is not uploaded in tagtog.

* list of duplicates articles ( ids ) in training samples (size 51):
``` 
{
'476': 853,
 '840': 1022,
 '171': 302,
 '292': 658,
 '1098': 1326,
 '69': 497,
 '777': 1102,
 '513': 1464,
 '1794': 1049,
 '1218': 427,
 '1597': 1279,
 '964': 2216,
 '2144': 1860,
 '1194': 1555,
 '741': 1453,
 '890': 1050,
 '2098': 1115,
 '2208': 1701,
 '1981': 1480,
 '1065': 1210,
 '1938': 1368,
 '1680': 21,
 '1445': 2121,
 '1468': 1204,
 '2042': 789,
 '301': 1248,
 '687': 164,
 '1565': 1786,
 '794': 1881,
 '372': 1993,
 '39': 1661,
 '86': 14,
 '2151': 839,
 '828': 494,
 '221': 583,
 '1615': 1160,
 '739': 2193,
 '1847': 145,
 '1733': 903,
 '757': 1056,
 '1570': 2084,
 '636': 1937,
 '110': 957,
 '1670': 311,
 '2080': 2078,
 '374': 1042,
 '569': 1689,
 '2017': 1111,
 '478': 1600,
 '544': 166
'876':710
}
 ```

* list of duplicates articles ( ids ) in testing samples (size 13):
```
 {
'1581': 1622,
 '1551': 1865,
 '931': 719,
 '1158': 895,
 '1405': 457,
 '1461': 752,
 '1059': 1246,
 '432': 887,
 '798': 237,
 '795': 1420,
 '838': 669,
 '1067': 1719,
 '1207': 350
}
```
* list of duplicates articles (ids) for testing samples that have duplicates in the training samples (size 38):
```
{
'804': 1319,
 '2131': 2134,
 '1587': 1061,
 '912': 1775,
 '486': 821,
 '880': 72,
 '248': 667,
 '1880': 1654,
 '1382': 1274,
 '581': 2162,
 '2056': 1519,
 '2214': 402,
 '1439': 1298,
 '1443': 604,
 '1229': 1601,
 '2207': 2039,
 '1375': 1895,
 '136': 782,
 '1968': 1705,
 '1043': 1907,
 '1146': 1325,
 '66': 1367,
 '1831': 265,
 '973': 131,
 '431': 779,
 '1756': 138,
 '169': 1899,
 '1323': 481,
 '885': 1636,
 '1801': 927,
 '897': 1300,
 '1854': 5,
 '645': 2218,
 '1606': 2018,
 '1182': 272,
 '587': 1685
'266':511
'2015':796
}
```