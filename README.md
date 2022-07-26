Mostly to find my duotrigordle starting words

```
head -c 100 world-words
cat world-words | tr "," "\n" | sed  's/"//g' > world-words-list
head world-words-list
for i in `cat world-words-list`; do echo -n $i | sed -e 's/\(.\)/\1\n/g'; done > world-words-list-letters
cat world-words-list-letters | sort | uniq -c  | sort -rn | head -n 15
cat world-words-list-letters | sort | uniq -c  | sort -rn | egrep -v '[slate]$'  | head
cat world-words-list-letters | sort | uniq -c  | sort -rn | egrep -v '[slaterhino]$'  | head
cat world-words-list-letters | sort | uniq -c  | sort -rn | egrep -v '[slaterhinodumpy]$'  | head
```
