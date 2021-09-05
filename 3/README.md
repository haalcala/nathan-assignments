# 3a Split files in lines

Sample command:


    split_files myfile.ext 1mb

Output:

    Splitting myfile.ext to 1mb each chunk

    Files:

        myfile.ext.1 (102KB)
        myfile.ext.2 (14KB)
        myfile.ext.3 (5KB)


# 3b Merge

Sample command:


    split_files  myfile.ext.1  myfile.ext.2  myfile.ext.3 myfile.ext

Output:

    Merging files myfile.ext.1  myfile.ext.2  myfile.ext.3 to myfile.ext ...
    Merging files myfile.ext.1  myfile.ext.2  myfile.ext.3 to myfile.ext ... done.

    Files:

        myfile.ext