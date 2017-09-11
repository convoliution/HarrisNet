# HarrisNet
An overambitious attempt to train an RNN to produce EDM. I chose to tentaively name this project after acclaimed
Scottish producer [Calvin Harris](https://en.wikipedia.org/wiki/Calvin_Harris), and it is not safe to assume that
this is a compliment.

## Why am I doing this?
I came across [this project](https://github.com/MattVitelli/GRUV) undertaken by two students named Aran Nayebi
and Matt Vitelli for Stanford University's [CS224d course](https://cs224d.stanford.edu/). It drew my attention
because I am interested in music as well as machine learning, and I decided to try to replicate their results
as an exercise to become acquainted with the recurrent neural network architecture.  

I took a look at their source code, the [YouTube compilation](https://www.youtube.com/watch?v=0VTI1BBLydE) they
produced, and [the paper](https://github.com/MattVitelli/GRUV) they wrote. I suspect that there may have been
oversights in their methodology that contributed to the overfitting that is observable in their video, and that
their nonetheless impressive work can be built upon further.


## What can I do?
Nothing. Well, close to that.  

I suspect that through a more careful prediction procedure, I could try to reduce overfitting. I have also added
a step in preprocessing the training data; I normalized each audio clip's tempos, and I believe this can help the
network more easily learn the concepts of beat and rhythm.
