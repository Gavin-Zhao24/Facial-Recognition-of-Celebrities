### Overview

Have you ever seen a photo of a person who looks extremely familiar, and the name is on the tip of your tongue, but you just can't quite get it? Well, if you're bad with names like me, this happens frequently especially for celebrities. That's why we thought it would be useful to develop a model that can tell you the name. To make the project more feasible, we decided to limit the pool of celebrities to our 10 favourite cast members in the Marvel Avengers series.

The idea is to take an image of a face and run it through a model that will tell you if the person is actually part of the Avengers cast. If so, then a second model will give the name of the Avengers celebrity.
![image](https://user-images.githubusercontent.com/90473344/156234656-13089f1f-63d3-463c-9637-fe57b0d19d88.png)
There are two models to train in this pipeline, so we will work on each one separately. However, we will preprocess the data used for both models all at once. The models will leverage transfer learning by using pretrained models in PyTorch, but the fully-connected classifiers will be handwritten and trained on the output features of the pretrained models. Afterwards, both models are combined with some preprocessing steps to create the entire pipeline.
