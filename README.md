# Kitty Ipsum to Doggy Ipsum Converter

## Project Overview

This project transforms whimsical "kitty ipsum" text files into equally delightful "doggy ipsum" text files using a Bash script. The conversion replaces feline-related terms with canine equivalents, creating a fun and engaging way to explore text manipulation.

## Files Included

### Input Files

#### kitty_ipsum_1.txt
- **Lines**: 27  
- **Words**: 332  
- **Characters**: 1738  
- **Occurrences of "meow" or "meowzer"**: 7 (Lines: 1, 4, 10, 22, 23)  
- **Occurrences of "cat," "cats," or "catnip"**: 7 (Lines: 1, 3, 7, 17, 21, 22, 26)

#### kitty_ipsum_2.txt
- **Lines**: 28  
- **Words**: 307  
- **Characters**: 1678  
- **Occurrences of "meow" or "meowzer"**: 9 (Lines: 4, 8, 12, 20, 24, 25, 28)  
- **Occurrences of "cat," "cats," or "catnip"**: 8 (Lines: 10, 14, 19, 20, 25, 26, 28)

### Output Files

#### doggy_ipsum_1.txt
- **Converted from** `kitty_ipsum_1.txt`  
- Replaces "meow" with "woof" and "catnip" with "dogchow"  
- Other feline terms are swapped with canine equivalents.

#### doggy_ipsum_2.txt
- **Converted from** `kitty_ipsum_2.txt`  
- Similar replacements as above.

## Script Details

### translate.sh
This Bash script performs the text transformation:
```bash
#!/bin/bash
cat $1 | sed -E 's/catnip/dogchow/g; s/cat/dog/g; s/meow|meowzer/woof/g'
```

## Input and Output

- **Input**: A kitty ipsum file (`kitty_ipsum_1.txt` or `kitty_ipsum_2.txt`)  
- **Output**: A doggy ipsum file (`doggy_ipsum_1.txt` or `doggy_ipsum_2.txt`)  

## How to Use

1. Place the `translate.sh` script in the same directory as your kitty ipsum files.
2. Run the script in your terminal:
   ```bash
   ./translate.sh kitty_ipsum_1.txt > doggy_ipsum_1.txt
   ./translate.sh kitty_ipsum_2.txt > doggy_ipsum_2.txt

