# Markov Chain Model
In this program, I implemented a Markov chain model to generate text based on an input file. The main structure of the program consists of the following key components:

# Table Class:
Purpose: This class builds a frequency table using the input text, stores the frequency of each character following a given context (defined by `contextLength`), and generates text based on this table.

# Functions:
- buildTable: This function processes the input text to build a frequency table, where the context is stored and each character that follows it is stored as a map of characters and their frequencies.
- pickNextChar: This function selects the next character based on the frequency of characters that follow the given text.
- createText: This function generates text based on the frequency table and a given text. It generates a string of the specified length.
- displayAsJSON: This function outputs the frequency table in JSON format.
   
# Main Function:
- Purpose: This function is responsible for reading command line arguments, opening the input file, processing the text, and invoking the Table class to generate text based on the command line arguments read.
- It handles edge cases like ensuring the number of characters to be generated is greater than the context length (max_val), validating command line arguments, and reading the input file.
- The program iterates through increasing levels of context size (from 1 to max_val or the k command line argument read), generating text for each level and printing the results. If -m is passed, it outputs the frequency table in JSON format.

# What Went Well:
- The basic functionality of the program (building the frequency table, generating text based on context, and handling different context levels) works as expected.
- The program correctly handles command-line arguments and reads the input file
- The random text generation works based on Shannon's algorithm, producing text matching a level of coherence at the respective context level.

# What Could Be Improved:
- Edge Case Handling: Although the program handles most edge cases, there may still be some uncommon cases I didn't account for.
- Efficiency: While this program works for the files given, performance could be slow for very large text files.

# What Was Left Out or Not Fully Implemented:
- Essentially the same as what could be improved, edge case handling and better efficiency could be included to allow for a diverse amount of file lengths to be used.
