# Title: Spotify_RiseOfML_Part2
## Source: https://engineering.atspotify.com/2021/11/18/the-rise-and-lessons-learned-of-ml-models-to-personalize-content-on-home-part-ii/ 
## Summary:  

1. How and why they evaluate models
1. Trust but verify your recommendations... with dashboards
    1. Used Kubeflow pipelines for training models
    1. Evaluation was the biggest pain
        1. because of infrastructure tools (TFMA) it was hard for them to compare ML models to non-ml algorithms
        1. custom evaluation metrics are hard to implement in TFMA
    1. Evaluating models against simpler non-ML solutions
    > we don’t typically start solutions to a problem with an ML solution. We first identify a heuristic, or rule-based, solution, and the most appropriate way to evaluate it.
    1. First things first: have a baseline for comparison
        1. to define what "better recommendations" are
        1. usually the easiest and most efficient solution is a heuristic / rule based solution, e.g. suggest the most frequently played items
    1. Comparing model performance to baseline performance is difficult
    1. they typically use typically use normalized discounted cumulative gain (NDCG@k)
    > we wanted to ensure that the model was not just predicting the most popular content. To do so, we were going to evaluate the model with a diversity metric that measured the difference between specific characteristics of items in each playlist.
    1. Looking at more than just the numbers for evaluating recommendations
        1. They built dashboards that compares different models with the same set of features
        1. This gives lot of intuition about the (new) model that they might want to push to prod, once they catched a model that only recommended the most popular playlists for europeans
        1. dashboard can show the quality of the recommendations (!)
1. The struggles of automated model retraining and deployment
    1. Retraining
        1. Sometimes the task of a model requires frequent retraining (e.g. it can only recommend shows previously seen in training data) 
        1. Lack of retraining is a tech debt in and of itself (and one of the biggest source)
        1. Implement for the short term while waiting for the long term
    1. Deployment
        > poll our internal storage directory every 10 minutes to check if there was a new revision of the model; if so, the service would pull the model down from where it was stored and start using that model to make predictions
        
        > The first step in automating retraining is automating train dataset and test dataset curation, fetching the correct features and performing the necessary feature transformations. 
        
        > Enabling CI/CD for retraining and model deployment is hard, but it’s becoming easier with the new tools available and makes the quality and reliability of our models better. And at first glance, you might not think you need retraining for a model because of the task it performs, but without it, your model could make predictions in unpredictable ways and increase your tech debt.

## Further readings: 
https://engineering.atspotify.com/2021/11/18/the-rise-and-lessons-learned-of-ml-models-to-personalize-content-on-home-part-i/ 
https://engineering.atspotify.com/
## My opinion: 
1. Such a great blog series, I wish more companies did this
1. Ask them what were they looking for on the dashboards, what was the most useful metric / whatever that helped them compare models and make better decisions
## Tags: #spotify #ml #mle #machinelearningengineer #mlstack #data #infrastructure 

