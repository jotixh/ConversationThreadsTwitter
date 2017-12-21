# Conversation Threads Twitter


This is a dataset of conversation threads yielded on Twitter. 
It was used in our paper [1] published in ECIR 2018 conference. 

If you want to use this dataset for research prurposes, please cite us as:

[1] Herrera, Jose; Poblete, Barbara; Denis; Parra. Learning to Leverage Microblog Data for QA. In Proceeding of European Conference on Information Retrieval (2018). 


# Dataset description


The dataset is a set of files in json format. 
Each file is a set of threads retrieved using our query formulations. 
And, for each thread, we retrieve their replies. 


```python
{
    "id": "cur-155",
    "q": "What is a female moose called?",
    "THREADS": {
        "634786506570248192": {
            "replies": [
                "634783395797671936",
                "634785975479087104",
                "634786506570248192"
            ]
        },
        "747481816483958785": {
            "replies": [
                "747481816483958785"
            ]
        },

        ....
}

```

The id of threads are not necesarily the initial tweet of a thread. 
For example, the thread `634786506570248192` is basically the id of the thread, but is not the initial thread. 
Because the correct order is `634783395797671936`, `634785975479087104`, `634786506570248192`.

We did in that way because, as we mention in our paper, we first retrieve tweet, and then, if it belongs to a thread, we retrieve the other replies. But the id of the thread is the tweet that it was found firstly. 