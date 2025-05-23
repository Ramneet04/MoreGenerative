# MoreGenrative

MoreGenerative takes one text file as input, where each line is assumed to be one training example, and generates more items like it. Under the hood, it is an autoregressive character-level language model, currently supporting Bigram and MLP-based architectures. For example, if we feed it a database of names, MoreGenerative will generate unique baby name ideas that sound realistic but aren't actual existing names. Similarly, with a dataset of company names, it can suggest new name ideas. You could also use it with valid scrabble words to produce English-like gibberish.

This project is intentionally lightweight — it’s a single, hackable Python file built with PyTorch, primarily intended for educational purposes rather than production use. It doesn't come with a million knobs or configurations, making it easy to understand and extend. Training works well on CPU, but GPU can speed things up significantly.

The current implementation follows a few key ideas from NLP literature:

Bigram model – one character predicts the next based on a count table

MLP model – a feed-forward neural net inspired by Bengio et al., 2003

Usage:

The included names.txt dataset contains common baby names (e.g., emma, olivia, ava...). To train the model:

```
emma
olivia
ava
isabella
sophia
charlotte
...

```

The names it can generate

```
carmahela.
jhovi.
kimrin.
thil.
halanna.
jazhien.
amerynci.
aqui.
nellara.
chaiiv.
kaleigh.
ham.
joce.
quinton.
lilea.
jamilio.
jeron.
jaryni.
jace.
chrudeley.
```

Have fun!