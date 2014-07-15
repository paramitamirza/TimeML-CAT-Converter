TimeML-CAT-Converter
====================

Python codes for converting text with TimeML annotation to CAT-XML annotation, and vice versa.

###Requirements
* Python 2.7 or higher
* an NLP tool for tokenization and sentence splitter, i.e. [Stanford CoreNLP](http://nlp.stanford.edu/software/corenlp.shtml) or [TextPro](http://textpro.fbk.eu/)

###To convert text with TimeML annotation to CAT-XML annotation
_! A parser for tokenization and sentence splitting is needed !_

For now, the tool can parse the output of [Stanford CoreNLP](http://nlp.stanford.edu/software/corenlp.shtml) and [TextPro](http://textpro.fbk.eu/).
The path(s) of the parser(s) need to be set in `converter/parser.config` file:
e.g.
```
STANFORD_CORENLP_PATH = "/home/user/stanford-corenlp/"
STANFORD_CORENLP_VERSION = "3.3.1"
TEXTPRO_PATH = "/home/user/TextPro/"
```

Usage:
```
python convertTimeMLToCAT.py dir_name [options]        or
python convertTimeMLToCAT.py file_name [options]

options: -p parser_name: stanford | textpro (for tokenization and sentence splitting, default: textpro)
         -o output_dir_name/file_name (default: dir_path/dir_name_CAT for directory and file_path/file_name_CAT.xml for file)
```   
             
###To convert text with CAT-XML annotation to TimeML annotation
Usage:
```
python convertCATToTimeML.py dir_name [options]        or
python convertCATToTimeML.py file_name [options]

options: -o output_dir_name/file_name (default: dir_path/dir_name_TimeML for directory and file_path/file_name.tml for file)
```
      
