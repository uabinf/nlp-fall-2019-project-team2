## Duplicate Question Pair Detection in Natural Language Processing
By Raiful Hasan and Mohammad Aminul Hoque 

* [Overview](#overview)
* [Dataset](#dataset)

### Overview
Identifying the duplicate questions is challenging, the sentence composition and word selection vary among persons. 
There is a way to find the document similarity based on the degree of overlapping in classic natural language processing. 
However, in duplicate question detection, it not perform well, because most of the questions are too small and the degree 
of overlapping is insufficient. We have implemented an LSTM based architecture that will detect the duplicate question if 
they have the same intent.

### Dataset
For this project, we have used the Quora question pair dataset. It contains publicly available Quora question. The dataset has been labeled manually by humans. Table 1 shows the sample data of the dataset.


| id | qid1 | qid2 | question1 | question2 | is_duplicate | 
| --- | --- | --- | --- | --- | --- |
| 25 | 53 | 54 | What is web application? | What is the web application framework? | 0 |
| 139 | 279 | 280 | What is the ideal life after retirement? | What's life after retirement? | 0 |
| 197 | 395 | 396 | What are some must watch TV shows before you die? | Are there any must watch TV shows? | 1 | 
| 221 | 443 | 444 | What is my puk code? | What's the PUK for TF64SIMC4? | 1 | 

Table 1: Sample data in Quora dataset

Here is the description of the field of the dataset - 

| Field | Description |
| --- | --- |
| id | unique id for each question pair |
| qid1 | the id for question 1 in the pair |
| qid2 | the id for question 2 in the pair |
| question1 | the full text for question1 |
| question2 | the full text for question2 |
| is_duplicate | 1- if questions are duplicate or 0 – if questions are not duplicate |

The attributes of the datasets are -

| Attribute | Values |
| --- | --- |
| Total number of entries | 4,04,290 |
| Total duplicate pairs | 149302 (37%) |
| Training set | 3,04,290 |
| development set | 50,000 |
| Testing set | 50,000 |


