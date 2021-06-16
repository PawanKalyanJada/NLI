# NLI
A distinct architecture to categories sentences on SNLI Dataset


There is a base model which encapsulates a distilbert model and some lstm layers to convert a sentence into a fixed-size vector.
The two sentences are fed into this base model and converted into vectors, then subtracted to get a context vector.
This context vector is now used to classify them into 3 categories: Neutral, Contradiction and Entailment

The model is trained only for a few epochs owing to GPU constraints but training for a larger time and using a LR Scheduler benifits this architecture.
Only first 50000 examples were taken for the training data. More data can be used to churn out the accuracy.
