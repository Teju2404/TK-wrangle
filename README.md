# TK-wrangle
## Input data file: shallow1.txt
## Output data file: shallow.txt and evans.txt
## Assigned Play:
- The Merry Wives of Windsor
- Speaker 1 is SHALLOW
- Speaker 2 is SIR HUGH EVANS
- Who speaks more SHALLOW or SIR HUGH EVANS? is the question asked to us.
- The below are the curl commands:
```
 curl "http://shakespeare.mit.edu/merry_wives/full.htm"
```
```
 curl "http://shakespeare.mit.edu/merry_wives/full.htm" -O
```
```
 curl "http://shakespeare.mit.edu/merry_wives/full.htm" | sed 's/<\/*[^>]*>//g' > shallow1.txt
 ```
- To count the total number of Speakers:
- Speaker 1:grep '^SHALLOW' 'shallow1.txt' -c
- Speaker 2:grep '^SIR HUGH EVANS' 'shallow1.txt'-c
- To transfer total count of SHALLOW to the output file:
-  grep '^SHALLOW' 'shallow1.txt' -c > shallow.txt
- To transfer total count of SIR HUGH EVANS to the output file:
- grep '^SIR HUGH EVANS' 'shallow1.txt' -c > evans.txt
- SIR HUGH EVANS speaks more with more words.