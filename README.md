# uniparser-grammar-nornakhichevan-armenian
This repository contains the "lexemes" and "paradigms" file directories in the Uniparser format, which are used for parsing the Nor-Nakhichevan Armenian dialect. 

The parser in this repository is derivative of the Eastern Armenian Uniparser repository (https://github.com/timarkh/uniparser-grammar-eastern-armenian/).

In the "wordlists" folder there are the results of a test run of the Nor-Nakhichevan parser on about 22,000 tokens that we found in our corpus (about 100,000 tokens in total) and the original Eastern Armenian parser for comparison.

To better understand the architecture, refer to Uniparser repository (https://github.com/timarkh/uniparser-morph).

### Usage
```python
# load the files from this repository

# !pip install uniparser_morph
from uniparser_morph import Analyzer

a = Analyzer()
a.lexFile = './lexemes/'
a.paradigmFile = './paradigms/'
a.load_grammar()

a.analyze_words('Ձևաբանության')

# The parser is initialized before first use, so expect some delay here (usually several seconds)
# You will get a list of Wordform objects
# You can also pass lists (even nested lists) and specify output format ('xml' or 'json')
```
