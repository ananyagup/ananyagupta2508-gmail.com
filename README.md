AllenNLP Coreference Resolution in Python - Readable clusters

Using AllenNLP Coreference Resolution in Python (getting clusters which are ACTUALLY readable)

There's been a dearth of documentation on the front of how to use AllenNLP's amazing coreference resolution. While the code to use it as a library in python is available on the site (https://demo.allennlp.org/coreference-resolution), once you get the results its quite confusing initially to know what to make of them. 

Here is the code on how to analyze the AllenNLP coreference clusters to make them "human readable" I guess.

from allennlp.predictors.predictor import Predictor
predictor = Predictor.from_path("https://storage.googleapis.com/allennlp-public-models/coref-spanbert-large-2020.02.27.tar.gz")
predictor.predict(
  document="The woman reading a newspaper sat on the bench with her dog."
)

