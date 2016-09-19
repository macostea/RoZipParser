# RO Zip Data Parser

[![Build Status](https://travis-ci.org/macostea/CoduriPostaleDataParser.svg?branch=develop)](https://travis-ci.org/macostea/CoduriPostaleDataParser)

This project is used to parse zip code files from the official Romanian government website. 

You can find the official xls files following this link:
http://data.gov.ro/dataset/coduri-postale-romania


## Installation
`pip install -r requirements.txt`

## Usage
This project can be used standalone to parse and convert the official documents or as a module inside another application.

**Important!**
The official data file is in the old xls format (Microsoft Excel <2007). The file **MUST** be converted in Office Open XML file format (Microsoft Excel 2007 - xlsx). 

### Command line
Convert to csv 
`python parser.py <inputfile> --csv <output.csv>`

### Module
```python
from codeparser import CodeParser

parser = CodeParser("<PATH TO XLSX FILE")
codes = parser.get_codes()
```

Each entry in the returned list is a model.Code instance.

Please see the test files for additional usage information.

## License
CoduriPostaleDataParser is released under the MIT license. See LICENSE for details

# Contact
Follow me on twitter [@mcostea](https://twitter.com/mcostea)