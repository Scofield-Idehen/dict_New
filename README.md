# Dictionary Lookup Program

This program allows users to input a word and look up its definition from a JSON data file. It provides suggestions if the word is misspelled and prompts the user to confirm the suggestion.

## Table of Contents

- [Usage](#usage)
- [Requirements](#requirements)
- [Example](#example)

## Usage

The program loads the JSON data from `data.json` and stores it in a Python dictionary. The user is prompted to input a word. The program checks if the word exists in the data dictionary.

- If an exact match is found, the definition is printed.

- If no match is found, it uses `difflib` to find close matches and prompts the user to confirm if the suggestion is what they meant.

- If a close match is confirmed, the suggested word's definition is printed.

- If no close match is found or the user denies the suggestion, a message is printed that the word is not found.

- The definition is printed as a list if there are multiple definitions, otherwise printed directly.

- After outputting the result, it prompts the user for a new word lookup.

## Requirements

- Python 3
- `json` module
- `difflib` module

## Example

```plaintext
Input your word: rabbit
Do you mean rabbit?: Y
['a small tailless furry animal with long ears, typically kept as a pet or for its fur.']

Input your word: televison
Do you mean television?: Y
['a system for transmitting visual images and sound that are reproduced on screens.']

Input your word: abcdef
this abcdef not found

Input your word:
