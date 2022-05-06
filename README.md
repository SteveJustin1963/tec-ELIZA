# tec-CHAT

NLP app done with the Tec1, MINT and Speech chip.   

In 1966, program ELIZA was developed, which aimed at tricking it users by making them believe that they were having a conversation with a real human being. ELIZA was designed to imitate a therapist who would ask open-ended questions and even respond with follow-ups. It responds to questions with answers that sound like they were provided by a therapist. The program is designed to mimic human conversation, and it is often used to gull people into thinking they are talking to a real person. HAT DOES ELIZA DO? Using "'pattern matching" and substitution methodology, the program gives canned responses that made early users feel they were talking to someone who understood their input. The program was limited by the scripts that were in the program. (ELIZA was originally written in MAD-Slip.) 

 

## NLP; GPT-3, T5, Transformers

GPT-3 is a computer system that is designed to generate human-like responses to questions. It is based on a neural network that has been trained on a large amount of data. The system is designed to generate responses that are similar to what a human would say. GPT-3 is the third generation GPT Natural Language Processing model created by OpenAI. It is the size that differentiates GPT-3 from its predecessors. The 175 billion parameters of GPT-3 make it 17 times as large as GPT-2. It also turns GPT-3 about ten times as large as Microsoft's Turing NLG model. [6]

This website [3] provides a simple way to generate text using the T5 transformer. You simply provide a prompt, and the transformer will generate text based on the prompt. The text generation is based on the T5 transformer, which is a neural network model that is trained on a large amount of text data. The transformer learn the relationships between the words in the text data, and can then generate new text that is similar to the training data. The T5 transformer is a neural network model that is trained on a large amount of text data. The transformer learn the relationships between the words in the text data, and can then generate new text that is similar to the training data.and can generate text on its own.it can also improve the quality of the text it generates by fine-tuning the model on specific domains or tasks and can generate text in multiple languages and multiple genres, that is both grammatically correct and fluent. 

Google is using the T5 text-to-text transfer learning algorithm to improve the performance of its natural language processing models. The T5 algorithm can be used to fine-tune a model to a specific task, and this can improve the performance of the model on that task. For example, the T5 algorithm was used to improve the performance of a Google Translate model. The T5 algorithm can also be used to improve the performance of other NLP tasks, such as question answering and text classification. The T5 algorithm is a powerful tool for transfer learning, and it can be used to improve the performance of many different types of NLP models. [4]

Text-to-text transfer transformer (T5) is a new approach for natural language understanding (NLU) that can be used to read and comprehend any text. It was developed by Google Research and is based on the transformer architecture. T5 is trained on a large amount of text data in order to learn the general knowledge about the world. This allows it to transfer that knowledge to any text, regardless of the domain or the task. For example, T5 can be used to generate summaries of news articles, generate descriptions of images, or answer questions based on a passage of text. T5 has shown promising results on a variety of NLU tasks, including question answering, text classification, and text generation. In addition, T5 is efficient to train and can be used on a variety of hardware platforms, including CPUs, GPUs, and TPUs. Overall, T5 is a promising new approach for NLU that has the potential to revolutionize the field.[5]

## Speech on the tec-1

We have https://github.com/SteveJustin1963/tec-SPEECH that allows us to make phonetic sounds, but we have to write the sound strings to drive the chip. We need a very simple ai system. We could write code to call an API from a paid site like OpenAI.com to do the hard lifting, but thats not fun for the Z80, what NLP text generators are there for 8 bit computers?  well no, sad. ok The Natural Language Toolkit (NLTK) with Python is one of the leading tools in NLP model building. maybe we can build from that. an example of a program using .py to do NLP.


```
// The following is a program that uses NLTK to perform NLP tasks such as tokenization and POS tagging:
import nltk
from nltk.tokenize import word_tokenize
from nltk.tag import pos_tag
text = "I am learning NLP with NLTK"
tokens = word_tokenize(text)
tags = pos_tag(tokens)
print(tags)
```

or

```
The following is a program that uses NLTK to perform NLP tasks such as sentence parsing and semantic analysis:
import nltk
from nltk.parse import stanford
from nltk.sem import relextract
text = "I am learning NLP with NLTK"
sentences = nltk.sent_tokenize(text)
parser = stanford.StanfordParser(model_path="edu/stanford/nlp/models/lexparser/englishPCFG.ser.gz")
parsed_sentences = parser.raw_parse_sents(sentences)
for sentence in parsed_sentences:
print(sentence)
relextract.demo()
```

### what is  NLP text  

NLP text is a type of text that can be processed by natural language processing algorithms. There are many different algorithms used for natural language processing, but some of the most common ones include 
- part-of-speech tagging
- parsing
- sentence segmentation
 
## some Python code for these;


### tagging:
```
tagger = nltk.pos_tag(nltk.word_tokenize("This is a sentence."))
print(tagger)
```

### Parsing:

```
parser = nltk.RegexpParser("NP: {<DT>?<JJ>*<NN>}")
tree = parser.parse(tagger)
print(tree)
```

### Sentence segmentation:
```
sent_tokenizer = nltk.data.load("tokenizers/punkt/english.pickle")
text = "This is a sentence. This is another sentence."
print(sent_tokenizer.tokenize(text))  
```

### Tokenization:
```
tokenizer = nltk.tokenize.treebank.TreebankWordTokenizer()
text = "This is a sentence."
print(tokenizer.tokenize(text)) 
```

### Stemming:
```
stemmer = nltk.stem.PorterStemmer()
text = "This is a sentence."
print([stemmer.stem(token) for token in tokenizer.tokenize(text)]) 
```
### Lemmatization:
```
lemmatizer = nltk.stem.WordNetLemmatizer()
text = "This is a sentence."
print([lemmatizer.lemmatize(token) for token in tokenizer.tokenize(text)]) 
stopword removal:
stopwords = nltk.corpus.stopwords.words("english")
text = "This is a sentence."
print([token for token in tokenizer.tokenize(text) if token not in stopwords]) 
n-grams:
text = "This is a sentence."
tokens = tokenizer.tokenize(text)
for i in range(len(tokens) - 1):
   print(tokens[i], tokens[i+1])
bigrams = nltk.bigrams(tokens)
for bigram in bigrams:
   print(bigram) 
collocations = nltk.collocations.BigramAssocMeasures()
finder = nltk.collocations.BigramCollocationFinder.from_words(tokens)
finder.nbest(collocations.likelihood_ratio, 2)
```
seems using Python may be the way to go then convert it down to mint, from [7] NLP is a process of extracting information from text data. It can be used to find important features in text data, such as keywords, topics, and sentiment. NLP can also be used to automatically generate text, such as summaries and translations. There are many Python libraries available for NLP, including NLTK, spaCy, and gensim. These libraries can be used to preprocess text data, extract features, and train models. by studying these methods we may come up with a Mint way.

### NLTK 
is a Python library for natural language processing. It can be used to preprocess text data, extract features, and train models.
```
import nltk

# Preprocess text data
text = "This is a sample text."
tokens = nltk.word_tokenize(text)

# Extract features
nltk.pos_tag(tokens)

# Train models
nltk.NaiveBayesClassifier.train(tokens)
```

### spaCy
is a Python library for natural language processing (NLP). It can be used to preprocess text data, extract features, and train models.

```
spaCy is compatible with Python 2.7 and 3.5+.

Installation:

pip install spacy

Usage:

import spacy

nlp = spacy.load('en')

doc = nlp(u'This is a sentence.')

for token in doc:
    print(token.text, token.lemma_, token.pos_, token.tag_, token.dep_,
          token.shape_, token.is_alpha, token.is_stop)

```
This is a sentence. this be a sentence. PRON PRP ROOT Xxxxx True False

This outputs the text, lemma, part-of-speech tag, syntactic dependency, shape, and whether the token is alphanumeric or a stopword.

### Gensim 
is a Python library for topic modeling and text similarity. It can be used to train models, such as word2vec, and to find similar documents.
Here is an example of using gensim to train a word2vec model:

from gensim.models import word2vec
```
# Load text data
text = ["This is a sentence", "This is another sentence"]

# Train word2vec model
model = word2vec.Word2Vec(text, size=100, window=5, min_count=1, workers=4)

# Find similar words
model.wv.most_similar("sentence")
```







## Ref 
1. https://en.wikipedia.org/wiki/ELIZA
2. https://web.njit.edu/~ronkowit/eliza.html
3. https://towardsdatascience.com/poor-mans-gpt-3-few-shot-text-generation-with-t5-transformer-51f1b01f843e
4. https://ai.googleblog.com/2020/02/exploring-transfer-learning-with-t5.html
5. https://github.com/google-research/text-to-text-transfer-transformer
6. https://www.itbusinessedge.com/development/what-is-gpt-3/
7. https://towardsai.net/p/nlp/natural-language-processing-nlp-with-python-tutorial-for-beginners-1f54e610a1a0
8. 
