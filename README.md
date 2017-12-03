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

## It's been a few months; what's going on?
I realized I basically abandoned this project without a word (totally not because I accidentally deleted my training dataset and didn't want to bother with recreating it), so here's where I left off—based on what I remember, anyway.

I was encountering issues at the generative stage; the produced waveform would die off into silence after about 10 samples or so. I realized I wasn't normalizing my data, so I stored the mean and variance of the samples to normalize the training data and un-normalize the output. This resulted in some rather promising audio samples...until I realized that it was producing the same sounding sample every time—even from noise. So then it occured to me that the mean sample I was calculating from training batches was doing the heavy lifting, and the network itself was still producing noise.

It also seemed to me that Nayebi and Vitelli's original code was feeding in large chunks of training data as seeds for their generated sample, which may account for their outputs sounding like overfitted results—it may indeed be the original training data, with random noise being added by the network.

At this point I gave up, and have moved on to other, arguably equally unsuccessful projects.
