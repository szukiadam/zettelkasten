# Title: Spotify_RiseOfML
## Source: https://engineering.atspotify.com/2021/11/15/the-rise-and-lessons-learned-of-ml-models-to-personalize-content-on-home-part-i/
## Summary: 

1. Stage 1: Candidate generation: The best albums, playlists, artists, and podcasts are selected for each listener.
1. Stage 2: Ranking: Candidates are ranked in the best order for each listener.  
1. Different models for podcast, shortcuts, playlists
1. They went from offline predictions to real-time
1. Pipeline checks the prediction score of a model, and if it reaches a threshold it is automatically pushed to prod
> A while ago, we discovered that we had been transforming one of the model’s features slightly differently at training time than at serving time, leading to potentially degraded recommendations — and there was no way to detect this, so it continued to happen for four months.Think about this for just a second. Such a simple part of our stack — at most, a few lines of code — was doing the wrong thing and impacted the recommendations produced by our model.
> .. we knew long term that we needed to either have a single source of data for both training and serving, or we needed to ensure that data was produced and transformed the same way in both stages.
1. One transformation implementation to rule them all
> The second approach we took to ensure our training and serving features did not differ was to use Tensorflow Data Validation (TFDV) to compare training and serving data schemas and feature distributions on a daily basis. 
1. Their system alerts for significant differences in feature sets, it uses the Chebyshev distance metric
> .. we quickly learned that it’s easy to make mistakes when moving models to production because the data often uses a different processing library.


## Further readings: https://engineering.atspotify.com/2021/11/15/the-rise-and-lessons-learned-of-ml-models-to-personalize-content-on-home-part-ii/ 
## My opinion: 
Funny to see that even such big tech companies also make somewhat rookie mistakes (but also shows how hard is it to make sure that a code does EXACTLY the same thing as an other)
Curious what they meant by using different libraries in serving vs batch, is performance the only reason for this?
## Tags: #spotify #ml #mlops #data  

