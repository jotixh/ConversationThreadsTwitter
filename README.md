# Conversation Threads Twitter


This is a dataset of conversation threads yielded on Twitter. 
It was used in our paper [1] published in ECIR 2018 conference. 

If you want to use this dataset for research prurposes, please cite us as:

[1] Herrera, Jose; Poblete, Barbara; Denis, Parra. Learning to Leverage Microblog Data for QA. In Proceeding of European Conference on Information Retrieval (2018). 


# Dataset description

The dataset is in a json file. The description is as follows. 

For example, 

```bash
 't9-689': {
            'q': 'What is the highest mountain in the world?',
            'r': 'LA060190-0193 | Mt. Everest | '},
            'THREADS': {'0': ['855270972626051074', '855273460506873857'],
                        '1': ['853095581354528770']},
```

* `t9-689` is a internal id of a question. 

* `q`: is the questions (retrieved from TREC and curated dataset of QA, see references above).

* `r`: possible answers. Please, omit replies such as 'LA060190-0193' (they are internals id of TREC). 

* `THREADS`: it is composed by the pair (key, value), where *key* is the relevance and the *value* are the threads (i.e., set of tweets). 
In the example, the (key, value)  '0':  ['855270972626051074', '855273460506873857'] means that the thread composed by tweets 855270972626051074 and 855273460506873857, was annotated as not relevant (value '0').
The second thread, composed by just one tweet 853095581354528770 was annotated as relevant (value '1').




# References:

* TREC QA http://trec.nist.gov/data/qa.html 
* Curated dataset https://github.com/brmson/dataset-factoid-curated)
