Now, you can call the untitled function with a .txt file containing the desired suffix as argument, and it will create the new Untitled file:
$ cat suffix.txt
painting
$ untitled suffix.txt
Untitled painting.txt created.
$ ls
suffix.txt  Untitled painting.txt

If there are already existing files with the same suffix, the function will automatically increase the number in parenthesis:
$ cat suffix.txt
slide presentation
$ touch "Untitled slide presentation.txt" "Untitled slide presentation (2).txt"
$ untitled suffix.txt
Untitled slide presentation (3).txt created.
$ ls
suffix.txt  Untitled slide presentation.txt  Untitled slide presentation (2).txt  Untitled slide presentation (3).txt
