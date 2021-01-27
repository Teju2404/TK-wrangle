# TK-wrangle
## Input data file: shallow1.txt
## Output data file: result.txt
## Assigned Play:
- The Merry Wives of Windsor
- Speaker 1 is Tejaswi Reddy Kandula
- Speaker 2 is Devin Ingersoll
- Who speaks more SHALLOW or SIR HUGH EVANS? is the question asked to us.
- I used the below curl commands
- curl "http://shakespeare.mit.edu/merry_wives/full.htm"
- curl "http://shakespeare.mit.edu/merry_wives/full.htm" -O
- curl "http://shakespeare.mit.edu/merry_wives/full.htm" | sed 's/<\/*[^>]*>//g' > shallow1.txt
- For sorting and counting i have used below commands
- tr ' ' '\12' < shallow1.txt
- tr ' ' '\12' < shallow1.txt | sort
- tr ' ' '\12' < shallow1.txt | sort | uniq -c
- tr ' ' '\12' < shallow1.txt | sort | uniq -c | sort -nr
- tr ' ' '\12' < shallow1.txt | sort | uniq -c | sort -nr > result.txt
- grep -i '^SHALLOW$' shallow1.txt
- grep -i '^SIR HUGH EVANS$' shallow1.txt
- SIR HUGH EVANS speaks more with more words.