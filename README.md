# PronounciationPredictor

This is a program that tries to predict how a word is pronounced given how it's spelled. The dataset this was trained on is [The CMU Pronouncing Dictionary](http://www.speech.cs.cmu.edu/cgi-bin/cmudict). It uses an encoder decoder transformer structure, that has been implemented from scratch. The data used is version 0.7b, accessed from the github repository linked above.

### Performance

Currently, it achieves a validation loss of 0.1026 and a testing loss of 0.1003. Cross Entropy loss was used. This performance empirically performs quite well. Some examples of spellings, predicted pronounciations, and true pronounciations are included below. Mistakes are relatively minor. Infact, since many words in the database have multiple pronounciations, some seeming differences are to be expected.

| Spelling | Actual Pronounciation | Predicted Pronounciation |
| -------- | --------------------- | ------------------------ |
| WARNED | W AO1 R N D | W AO1 R N D |
| KNOCKOUTS | N AA1 K AW2 T S | N AA1 K AW2 T S |
| CONVICTS | K AH0 N V IH1 K T S | K AA1 N V IH0 K T S |
| PERMENTER | P ER1 M AH0 N T ER0 | P ER1 M AH0 N T ER0 |
| HEWE | HH Y UW1 | HH Y UW1 |
| OVERSEEN | OW1 V ER0 S IY2 N | OW1 V ER0 S IY1 N |
| HABIG | HH AE1 B IH0 G | HH AE1 B IH0 G |
| STOLT | S T OW1 L T | S T OW1 L T |
| BELIEVES | B IH0 L IY1 V Z | B IH0 L IY1 V Z |
| PREISER | P R AY1 S ER0 | P R AY1 Z ER0 |


### Next Steps
Integrate a way for the computer to 'say' a predicted pronounciation

Try and do some Mechanistic Interpretability research on the model. Does this model have induction circuits? I do not believe there is a need for them in this use case, but they are a fundamental emergent feature in text based transformers. Is there a way we can identify behavior like supressing consecutive vowel sound tokens, which is something I expect to see. I wish to come up with other behaviors that this model might show and see if they can be reverse engineered.
