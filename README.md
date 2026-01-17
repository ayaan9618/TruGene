#Algorithmic Analysis of DNA Profiles Using Short Tandem Repeats (STRs)



---

## What This Project Does

This is a Python algorithmic program that analyzes DNA sequences to identify individuals based on their genetic markers. Specifically, it looks at Short Tandem Repeats (STRs) - small patterns in DNA that repeat multiple times and vary between people - to create a unique genetic profile.

The program reads a DNA sequence, counts how many times certain STR patterns repeat consecutively, and then compares those counts against a database of known profiles to find a match.

---

## Background

Short Tandem Repeats are basically short DNA sequences that repeat back-to-back. For example, if the pattern "AGATC" repeats 3 times in a row, you'd see "AGATCAGATCAGATC" in the DNA sequence. Different people have different numbers of these repeats, which makes STRs really useful for identification purposes.

The tricky part is writing code that can accurately count the *longest* consecutive run of each STR pattern in a potentially very long DNA sequence. This project tackles that problem using string-matching algorithms.

---

## How It Works

### Input Files

The program needs two things:

1. **A CSV database** containing:
   - Names of individuals
   - Their STR repeat counts for various patterns

2. **A text file** with:
   - A raw DNA sequence (just the letters A, C, G, and T)

### The Algorithm

Here's what happens when you run the program:

1. **Load the data** - Read in the CSV database and extract which STR patterns we're looking for
2. **Analyze the DNA** - For each STR pattern, scan through the entire DNA sequence and find the longest stretch where that pattern repeats consecutively
3. **Build a profile** - Collect all the STR counts into a genetic profile
4. **Find a match** - Compare this computed profile against every person in the database
5. **Report results** - If there's an exact match, print that person's name. Otherwise, report "No match"

The algorithm is careful to handle overlapping patterns correctly, which can be surprisingly tricky to get right.

---

## Running the Program

### What You Need

- Python 3.x (any recent version should work)
- No special libraries required - just Python's built-in CSV module

### Command

```bash
python dna.py database.csv sequence.txt
```

### Example Files

**database.csv:**
```csv
name,AGATC,CTTCTCT,TTTTTT
Alice,12,4,5
Bob,10,4,10
Charlie,14,6,5
```

**sequence.txt:**
```
AGATCAGATCAGATCCTTCTCTTTTTT
```

### What You'll See

The program will output either:
- The name of the matching individual, or
- "No match found" if the profile doesn't match anyone in the database

---

**Language:** Python  
**Focus Area:** Computational Biology & String Algorithms

## Limitations

This is a simplified model. Some important caveats:

- It assumes perfect data with no sequencing errors or mutations
- Only finds exact matches - no "close enough" results
- Real forensic DNA analysis is much more complex and uses statistical models
- Input files need to be formatted correctly or the program won't work

Basically, this demonstrates the core string-matching concept behind DNA profiling, but it's not something you'd use for actual forensic work.

---

## Potential Applications

Even though this is a learning project, the concepts apply to:

- Understanding how forensic DNA databases work
- Learning about bioinformatics algorithms
- Practicing string manipulation and pattern matching
- Exploring computational approaches to genetics

---


## Technical Notes

The program is written in pure Python without any external bioinformatics libraries. The time complexity is roughly linear with respect to the DNA sequence length (for each STR pattern), which means it scales reasonably well.

The core challenge was implementing the consecutive repeat counter correctly - especially handling edge cases where patterns might overlap or appear in tricky ways.

---

## License

This project is released under the MIT License.
