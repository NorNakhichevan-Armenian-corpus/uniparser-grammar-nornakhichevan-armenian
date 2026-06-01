# uniparser-grammar-nornakhichevan-armenian
This repository contains the lexemes and paradigms files in the Uniparser format, which are used for parsing the Nor-Nakhichevan Armenian dialect.

Refer to Uniparser repository (https://github.com/NorNakhichevan-Armenian-corpus/uniparser-grammar-nornakhichevan-armenian/upload/main/lexemes) and to the Eastern Armenian Uniparser repository (https://github.com/timarkh/uniparser-grammar-eastern-armenian/), both of which are used here.

### Usage
```python
# !pip install uniparser_morph
from uniparser_morph import Analyzer

# load the files from this repository

a = Analyzer()
a.lexFile = './lexemes/'
a.paradigmFile = './paradigms/'
a.load_grammar()

a.analyze_words('Ձևաբանության')

# The parser is initialized before first use, so expect some delay here (usually several seconds)
# You will get a list of Wordform objects
# You can also pass lists (even nested lists) and specify output format ('xml' or 'json')
```
