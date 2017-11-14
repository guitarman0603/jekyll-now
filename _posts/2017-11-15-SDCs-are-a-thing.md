---
layout: post
title: SDCs are a thing!
---

here everyone is busy coming up with Deep learning models, there is an absolutely another world out there working to keep up with the hardware that will be needed for training them.
({{ site.baseurl }})

Obviously, the announcement of second generation TPUs by google for their Tensor flow framework is definitely going to be a very big step in this field; as the claims made by it seem quite impactful. 
This is when I came across the research going on in the field of DNN accelerators and that got me quite stirred up. What exactly do SDCs mean? How do they originate? How do we detect them? Why is mitigating them very necessary? Especially in the field of DNN accelerators. These are the first few questions that popped into my head, the moment I started reading about these terms. To understand more about SDCs I came across a paper by IBM, which basically explains what SDC really are.
To understand what these exactly mean is not difficult. They have always been here, it’s just that did we pay much attention to it.The i5 and the i7 are the same chips. The i5 is the lower binned chip with 2 mb L3 cache disabled and hyperthreading disabled. They all are manufactured together, however, not all of them are capable of reaching the particular frequency and that is how they are distinguished amongst. The reason why I gave this example because I feel it explains how unstable hardware can be. To handle this a lot of mitigation techniques are introduced, to stabilize the hardware, at least to some extent. That is where the classification of different types of errors come into picture, such as the hard and the soft errors. To detect the errors there are certain techniques existing, such as Triple Modular Redundancy(TMR). 
What are SDCs?
While training the NNs, it was observed that despite every precaution, we were not getting proper outputs. What could be the reason? Silent data corruption. SDCs are insidious, which means that while reading from the hardware, there are times when due to clarity it ends up reading 1 for 0 or vice versa. However, how do we detect them? Can we? Well, there are certain techniques by which we can eliminate, however mitigate these and it is application dependent. 
I found this topic really interesting and see a lot of scope related to this in the future. However, I still have not related the SDCs to the DNNs yet. But, I guess that the story is self explanatory now. DNN accelerators while training, tend to experience SDCs, which might end up with outputs not expected. Especially for models with large amounts of data sets, the impact of SDCs can be quite dire.
If anyone reading this comes across ANYTHING even remotely related to this, feel free to ping me.
