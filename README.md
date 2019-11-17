# Tensorflow 2.0 Question Answering Kaggle Competition

### Data
- Each sample contains a Wikipedia article, a related question, and the candidate long form answers. The training examples also provide the correct long and short form answer or answers for the sample, if any exist.
- Data fields: 
  - document_text - the text of the article in question (with some HTML tags to provide document structure). The text can be tokenized by splitting on whitespace.
  - question_text - the question to be answered
  - long_answer_candidates - a JSON array containing all of the plausible long answers.
  - annotations - a JSON array containing all of the correct long + short answers. Only provided for train.
  - document_url - the URL for the full article. Provided for informational purposes only. This is NOT the simplified version of the article so indices from this cannot be used directly. The content may also no longer match the html used to generate document_text. Only provided for train.
  - example_id - unique ID for the sample.
  
### Evaluation
Submissions are evaluated using [micro F1](https://en.wikipedia.org/wiki/F1_score) between predicted and expected answers. Predicted long and short answers must match exactly the token indices of one of the ground truth labels ((or match YES/NO if the question has a yes/no short answer). There may be up to five labels for long answers, and more for short. If no answer applies, leave the prediction blank/null.

### Resources
- Starter notebook with BERT: https://www.kaggle.com/philculliton/using-tensorflow-2-0-w-bert-on-nq


