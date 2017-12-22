# Conversation Threads Twitter


This is a dataset of conversation threads yielded on Twitter. 
It was used in our paper [1] published in ECIR 2018 conference. 

If you want to use this dataset for research prurposes, please cite us as:

[1] Herrera, Jose; Poblete, Barbara; Denis, Parra. Learning to Leverage Microblog Data for QA. In Proceeding of European Conference on Information Retrieval (2018). 


# Dataset description

The dataset is in a json file. The description is as follows. 

For example, one instance is as 

```bash
 't9-689': {
            'q': 'What is the highest mountain in the world?',
            'r': 'LA060190-0193 | Mt. Everest | '},
            'THREADS': {'0': ['855270972626051074', '855273460506873857'],
                        '1': ['853095581354528770']},
```

* `t9-689`: it is a internal identification of a question used by us. 

* `q`: it is the questions text (obtained from TREC and curated dataset of QA, see references below).

* `r`: it is the possible answers of question *q*. NOTE: please, omit replies such as 'LA060190-0193', because they are internals id of TREC. 

* `THREADS`: it is a set candidate threads that could answer the question *q*. Each thread is composed by the pair (key, value), where *key* is the relevance and the *value* are the candidate threads (i.e., set of tweets).
In the above example, the (key, value) pair ('0', ['855270972626051074', '855273460506873857']) means that the candidate thread (composed by tweets: 855270972626051074 and 855273460506873857) has not the answer. 
The second thread, composed by just one tweet 853095581354528770 was annotated as '1', it means that is highly probably that the thread contains the correct answer. 



# References:

* TREC QA http://trec.nist.gov/data/qa.html 
* Curated dataset https://github.com/brmson/dataset-factoid-curated)
