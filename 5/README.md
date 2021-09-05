# 5 Compare text files

Sample command:

    compare newfile.txt oldfile.txt


Sample output:

    -- newfile.txt: line 2
    + new line in newfile
    -- newfile.txt: line 6
    - removed line in oldfile
    + replaced line in newfile

Data:

    newfile.txt:

    the quick
    new line in newfile
    brown fox
    jumps over
    the lazy 
    replaced line in newfile
    grumpy dog

    oldfile.txt:

    the quick
    brown fox
    jumps over
    the lazy 
    removed line in oldfile
    grumpy dog

