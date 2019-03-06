# Delete the first line of a file 
```bash
sed -i -e "1d" $FILE 
```

# Delete a range of lines from a file 
```bash
 sed -i -e "1,4d" test.txt
```
Where 1 is the start of the range and 4 is the end of the range of lines you want to delete
