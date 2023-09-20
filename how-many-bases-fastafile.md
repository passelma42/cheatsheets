# Count how many bases there are in my fasta files
# Goal
I want a quick count on how many bases I have in my fasta file
ou can count the number of bases (A, T, G, and C) in a FASTA file using various command-line tools.  
One common approach is to use a combination of grep, tr, and wc commands. Here's an example command to count the bases in a FASTA file:

```bash
grep -v '>' your.fasta | tr -d '\n' | wc -c
```
Where:  
1. grep -v '>' your.fasta: This command uses grep to exclude lines starting with '>' (FASTA headers) from your FASTA file. This leaves only the sequence lines.  
2. tr -d '\n': This uses the tr (translate or delete characters) command to delete newline characters ('\n') from the sequence, effectively joining the sequence into a single line.  
3. wc -c: Finally, the wc command with the -c option is used to count the number of characters in the resulting sequence, which corresponds to the total number of bases (A, T, G, and C).  

Make sure to replace your.fasta with the actual filename of your FASTA file. This command will provide you with a count of all the bases in the file.  

# Code
```bash
grep -v '>' your.fasta | tr -d '\n' | wc -c
```
