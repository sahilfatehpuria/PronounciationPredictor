# PronounciationPredictor

This is a program that tries to predict how a word is pronounced given how it's spelled. The dataset this was trained on is [The CMU Pronouncing Dictionary](http://www.speech.cs.cmu.edu/cgi-bin/cmudict). It uses an encoder decoder transformer structure, that has been implemented from scratch.

### Performance

Currently, it achieves a validation loss of 0.1026 and a testing loss of 0.1003. Cross Entropy loss was used. This performance empirically performs quite well. Some examples of spellings, predicted pronounciations, and true pronounciations are included below.


### Next Steps
Compare performance to a pretrained transformer. Interesting to see the process to finetune a GPT for this task
