# 20k Words Club
Welcome to the github repository of the ENS 20k Words Club. There are a number of resources included for the 20k Words collection, as well as for general ENS bulk searching. You can join the 20k Words Club Discord here: https://discord.gg/nG5cyX4fw8. See `output/validwords.txt` for the full list of words in the 20k Words Club.

# Input and Output Files
Contains pregenerated output for 20k Words. You can use `main.py` to refresh this data, or any domain list.

## input/allwords.txt
The source list of the 20k most common English words. This list of words is sourced from https://github.com/first20hours/google-10000-english.

## output/validwords.txt
The full list of valid words in the input list. Removes one and two letter words (no longer registerable). Only 19,404/20,000 words are valid.

## output/available.txt
A text file containing all of the available domains. As of last update, 681 words are available, with 37 sales in the past day.

## output/names.csv
A CSV containing data on all of the input domains. Columns include, `Name`, `Length`, `Status`, `Premium`, and more.

## output/letters/n letters.txt
Individual text files containing all of the words of the same length.

# main.py
Python script for bulk searching ENS domains.

## Setup
You must have python3 installed in order to run this script (See https://www.python.org/downloads/ if you do not have python).

Run `pip install -r requirements.txt` or `pip install grequests pycryptodome` to install the rquired python packages.

## Running
Simply run `py main.py` and the output files will be created/updated.

## Customization
### Custom Domain Lists
You can use the script on any text file with names seperated by newlines. Simply change the value of `INPUT` on line 8 to point to the desired text file.

### Custom File Names
It is possible to set custom file names to analyze multiple word lists without overwriting files. Change the file name variables on lines 9-12 to change the file names. File folder and extension are handled for you, just input the name like `'validwords'`. For `LETTERS` you must keep one set of `{}` in the string where the word length will be inserted.