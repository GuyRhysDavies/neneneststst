# neneneststst
A look at the possibilities for hierarchical modelling using nested sampling. 

We like HMC or NUTS samplers for hierarchical modelling as the can work very well in the large number of parameter space.  But they do not do so well with multi-model posteriors.  On the other hand, nested smaplers are great with multi-modal posteriors but do not enjoy the large parameter space. 

Here we will look at the possibilities for using a nested sampler for hierarchical modelling.

The main idea I will want to test: can we model idividual stars (this is in the star modelling context) using nested sampling and generate a posterior with uniform priors (yes we can).  Can we then treat that as a likelihood which we will use as our prior in our hierarchical modelling?  Can we summarise the posterior/likelihood of the individual stars using something that works well in the context of the Dynesty prior transform function (yes, if 1 multi-dimensional Guassian, but whiat if multimodal)?  If we can do all the above, can we model something like a cluster where the nested sampler takes care of all the shrikage?

Let's find out.
