**Bandit Level 0 -> level 1 password:**

>>ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If


**Bandit Level 1 → Level 2 password:**

>>263JGJPfgU6LtdEvgfWU1XP5yac29mFx

* use '<' for files starting with a hyphen



**Bandit Level 2 → Level 3 password:**

>>MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

* use tab for files with spaces



**Bandit Level 3 → Level 4 password:**

>>2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

* use file <filename> to get the type of a file



**Bandit Level 4 → Level 5 password:**

>>4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw



**Bandit Level 5 → Level 6 password:**

>>HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

* there is a hidden file, .file2, is where the password is hidden.
* to list all hidden files do (ls -la)


**Bandit Level 6 → Level 7 password:**

>>morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

* **command**: find / -user bandit7 -group bandit6 -size 33c -exec cat {} \\; 2>/dev/null
* exec executes the find command on each file
* {} is replaced by the current file path found by find.
* \\; ends the -exec statement.


**Bandit Level 7 → Level 8 password:**

>>dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

\- grep command searches in file


**Bandit Level 8 → Level 9 password:**

>>4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

* **command**: sort data.txt | uniq -u
* the '|' operator(pipe operator) is used to redirect the standard output of one command to the standard input of another command. 



**Bandit Level 9 → Level 10 password:**
>>FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
- use the strings command and manually search
- strings data.txt | grep '^='


**Bandit Level 10 → Level 11 password:**
>>dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
- use base64 -d to decode a base64 file

**Bandit Level 11 → Level 12 password:**
>>7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
- string in data.txt has been rotated by 13 positions therefore we need to rerotate using tr function
- echo "Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4" | tr 'A-Za-z' 'N-ZA-Mn-za-m'


**Bandit Level 12 → Level 13 password:**
>> FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
- make a dir and copy the hex compressed file into it under a new name. Repeatedly decompress the file with tar, gzip2, bzip2