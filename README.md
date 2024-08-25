
###TruGene

**A Robust DNA Analysis Tool**

###Introduction:

TruGene is a powerful Python-based tool designed to compare a DNA sequence to a database of Short Tandem Repeat (STR) counts. It accurately identifies potential matches by finding the longest consecutive occurrences of STRs in the DNA sequence and checking for alignment with the database profiles.

###Features:

- Reads a database of STR counts in CSV format.
- Reads a DNA sequence from a text file.
- Calculates the longest match count for each STR in the DNA sequence.
- Compares the calculated STR counts to the database profiles.
- Identifies and prints the name of a matching profile, if present.
- Prints "No match found" if no matching profile is found in the database.

**How to Use:**

1. **Install Dependencies:**
   Ensure you have Python (version 3 recommended) and the `csv` module installed. You can install `csv` using `pip install csv`.
2. **Prepare Files:**
   - Create a CSV file named `data.csv` containing the database of STR counts, with the first row holding the STR names and subsequent rows representing profiles with names and STR counts.
   - Create a text file named `sequence.txt` containing the DNA sequence you want to analyze.
3. **Run TruGene:**
   Open a terminal or command prompt and navigate to the directory containing the script (`trugene.py`), the database file (`data.csv`), and the DNA sequence file (`sequence.txt`).
   Run TruGene using the following command:

   ```bash
   python trugene.py data.csv sequence.txt
   ```

   **Example Database (data.csv):**

   ```csv
   STR,Alice,Bob,Charlie
   AGATC,12,10,14
   CTTCTCT,4,4,6
   TTTTTT,5,10,5
   ```

   **Example DNA Sequence (sequence.txt):**

   ```
   AGCTAGCTAGCTAGCT
   ```

4. **Output:**
   TruGene will generate the following output:

   - If a matching profile is found in the database, it will print the matching person's name.
   - If no match is found, it will print "No match found".

**Additional Notes:**

- TruGene is designed to be user-friendly and easy to use.
- For more complex scenarios, consider extending the code to handle additional features or optimizations.
- Error handling can be incorporated to provide informative messages and gracefully handle unexpected input.

###License:

TruGene is provided under the [MIT License](https://choosealicense.com/licenses/mit/).



.
