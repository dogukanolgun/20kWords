# 20k Word Club
### [Word List](https://github.com/msnyder5/20kWords/blob/main/20kWordClub/valid.txt) - [Available Words](https://github.com/msnyder5/20kWords/blob/main/20kWordClub/available.txt) - [Twitter](https://twitter.com/20kWordClub)
Welcome to the GitHub repository of the 20k Word Club. There are a number of resources included in this repo for the 20k Word Club and other Clubs, as well as for general ENS bulk searching.

### 20kWordClub/valid.txt
Only 19,404/20,000 words are valid.

### 20kWordClub/available.txt
As of last update, 673 words are available, with 36 sales in the past day.

### input/20kWordClub.txt
The source list of the 20k most common English words. This list of words is sourced from [here](https://github.com/first20hours/google-10000-english).

# Input and Output Files
`search.py` will process every text file in `/input` into seperate folders in `/output`.

## Provided Inputs
`20kWordClub`, `10kClub`, `24hClub`, `100kClub`, `365Club`, `999Club`, `Animals`, `Countries`, `Country Abbreviations`, `DoubleLetterClub`, `Hyph-ENS`, `Pi`, `ScientificNotation`, `ThreeLetterClub`

Submit an issue or pull request on the GitHub if you have a domain list you'd like me to add.

## Outputs
### /output/./valid.txt
The full list of valid words in the input list. Removes one and two letter words (no longer registerable).

### /output/./available.txt
A text file containing all of the available domains.

### /output/./domains.csv
A CSV containing data on all of the input domains. Columns include, `Name`, `Length`, `Status`, `Premium`, `URL` and important dates.

### /output/./length/n chars.txt
Individual text files containing all of the words of the same length.

# search.py
Python script for bulk searching ENS domains.

## Setup
You must have python3 installed in order to run this script (See [here](https://www.python.org/downloads/) if you do not have python).

Run `pip install -r requirements.txt` or `pip install grequests pycryptodome` to install the rquired python packages.

## Running
Simply run `py search.py` and the output files will be created/updated.

## Customization
### Custom Domain Lists
You can use the script on any text file with names seperated by newlines. Simply add the text file to the `/input` folder and run the script.

### Config
It is possible to change the sort order and enable/disable outputs. See the comments in `config.py` for more details.