# Lab Report 3
 
## `grep -c`

The `-c` in `grep -c` refers to count, so `grep -c` essentially goes through the specified file and returns the number of lines that match the specified string. This command option can be useful for finding out how many lines contain a specific string rather than seeing the printed-out lines containing the specified text.

```
$ grep -c the stringsearch-data/technical/911report/chapter-1.txt
313
```

```
$ grep -c disease stringsearch-data/technical/biomed/1468-6708-3-3.txt
9
```

## `grep -H`

The command `grep -H` prints all the lines that match the given string, as well as the file name that contains the match. This command is useful when used after a `find` command that stores specific file paths in a text file to see the line and file path in the text file that contains the specificed string.

```
$ grep -H FBI stringsearch-data/technical/911report/chapter-1.txt
stringsearch-data/technical/911report/chapter-1.txt:    Passengers on three flights reported the hijackers' claim of having a bomb. The FBI told us they found no trace of explosives at the crash sites. One of the passengers who mentioned a bomb expressed his belief that it was not real. Lacking any evidence that the hijackers attempted to smuggle such illegal items past the security screening checkpoints, we believe the bombs were probably fake.
stringsearch-data/technical/911report/chapter-1.txt:    At the White House, the video teleconference was conducted from the Situation Room by Richard Clarke, a special assistant to the president long involved in counterterrorism. Logs indicate that it began at 9:25 and included the CIA; the FBI; the departments of State, Justice, and Defense; the FAA; and the White House shelter. The FAA and CIA joined at 9:40. The first topic addressed in the White House video teleconference-at about 9:40-was the physical security of the President, the White House, and federal agencies. Immediately thereafter it was reported that a plane had hit the Pentagon. We found no evidence that video teleconference participants had any prior information that American 77 had been hijacked and was heading directly toward Washington. Indeed, it is not clear to us that the video teleconference was fully under way before 9:37, when the Pentagon was struck.
stringsearch-data/technical/911report/chapter-1.txt:    while the children continued reading. He then returned to a holding room shortly before 9:15, where he was briefed by staff and saw television coverage. He next spoke to Vice President Cheney, Dr. Rice, New York Governor George Pataki, and FBI Director Robert Mueller. He decided to make a brief statement from the school before leaving for the airport. The Secret Service told us they were anxious to move the President to a safer location, but did not think it imperative for him to run out the door.
```
```
$ grep -H pollution stringsearch-data/technical/government/Env_Prot_Agen/bill.txt
stringsearch-data/technical/government/Env_Prot_Agen/bill.txt:To amend the Clean Air Act to reduce air pollution through
stringsearch-data/technical/government/Env_Prot_Agen/bill.txt:or the State or local air pollutioncontrol agency, with an approved
stringsearch-data/technical/government/Env_Prot_Agen/bill.txt:countries wouldprevent air pollution generated in those countries
stringsearch-data/technical/government/Env_Prot_Agen/bill.txt:from ongoing and future electricitygeneration and pollution control
stringsearch-data/technical/government/Env_Prot_Agen/bill.txt:operates, maintains and repairspollution control equipment to limit
stringsearch-data/technical/government/Env_Prot_Agen/bill.txt:contribute to, air pollution in excess of any national ambient air
stringsearch-data/technical/government/Env_Prot_Agen/bill.txt:pollution) (42 U.S.C. 7641 et seq.) is-
```

## `grep -r`

The `-r` in `grep -r` stands for recursive, so the command goes through all the files in the specified directory and prints all the lines and their respective file names that match the specified string. This command option is useful for searching for lines and their respective file name within the provided directory without having to store all the file paths in a text file first or manually doing `grep` for each file.

```
$ grep -r California stringsearch-data/technical/911report/
stringsearch-data/technical/911report/chapter-11.txt:                California went on the watch for his like.
stringsearch-data/technical/911report/chapter-13.4.txt:                chemistry, from California State University, Sacramento. Sufaat did not start on the
stringsearch-data/technical/911report/chapter-13.4.txt:                reasons for sending Hazmi and Mihdhar to California do not seem especially
stringsearch-data/technical/911report/chapter-13.4.txt:                explanation for the California destination. The possibility that the two hijackers
stringsearch-data/technical/911report/chapter-13.4.txt:                addresses-one in the United States ("possibly in California") and one in South
stringsearch-data/technical/911report/chapter-13.4.txt:                California." Intelligence report, interrogation of KSM, June 15, 2004.
stringsearch-data/technical/911report/chapter-13.4.txt:                acclimate the hijackers to the United States, particularly San Diego, California."
stringsearch-data/technical/911report/chapter-13.4.txt:                California, but Atta told him to discontinue this effort. Intelligence report,
stringsearch-data/technical/911report/chapter-13.4.txt:                his training in California, see FBI report of investigation, interview of Adnan
stringsearch-data/technical/911report/chapter-13.5.txt:            85. Hazmi and Mihdhar used their true names to obtain California driver's licenses
stringsearch-data/technical/911report/chapter-3.txt:                California (UNOCAL) to build a pipeline across the country. While there was probably
stringsearch-data/technical/911report/chapter-5.txt:                became the primary target. For similar reasons, California also became a target for
stringsearch-data/technical/911report/chapter-5.txt:                headquarters, nuclear power plants, and the tallest buildings in California and the
stringsearch-data/technical/911report/chapter-5.txt:                such as San Diego and Long Beach, California; brochures for schools; and airline
stringsearch-data/technical/911report/chapter-6.txt:            One of the 16, Raed Hijazi, had been born in California to Palestinian parents; after
stringsearch-data/technical/911report/chapter-6.txt:                spending his childhood in the Middle East, he had returned to northern California,
stringsearch-data/technical/911report/chapter-6.txt:                that Hijazi had lived in California and driven a cab in Boston and that Deek was a
stringsearch-data/technical/911report/chapter-7.txt:            Why Hazmi and Mihdhar came to California, we do not know for certain. Khalid Sheikh
stringsearch-data/technical/911report/chapter-7.txt:                Mohammed (KSM), the organizer of the planes operation, explains that California was
stringsearch-data/technical/911report/chapter-7.txt:                that al Qaeda had any agents in Southern California. We do not credit this
stringsearch-data/technical/911report/chapter-7.txt:                California, so that they could begin pilot training as soon as possible. KSM claims
stringsearch-data/technical/911report/chapter-7.txt:                Culver City, one of the most prominent mosques in Southern California.
stringsearch-data/technical/911report/chapter-7.txt:                fellow inmates at a California prison in September- October 2003 that he had known
stringsearch-data/technical/911report/chapter-7.txt:                rest of his time in California, until mid-December; he would then leave for Arizona
stringsearch-data/technical/911report/chapter-7.txt:                Translating between English and Arabic, he assisted them in obtaining California
stringsearch-data/technical/911report/chapter-7.txt:                of California declined to prosecute him on charges arising out of his alleged
stringsearch-data/technical/911report/chapter-7.txt:                impression is that soon after arriving in California, Hazmi and Mihdhar sought out
stringsearch-data/technical/911report/chapter-7.txt:                child arrived, he could stand life in California no longer. In late May and early
stringsearch-data/technical/911report/chapter-7.txt:                California, and Arizona; and he briefly started at a couple of them before returning
stringsearch-data/technical/911report/chapter-7.txt:                an English as a second language program in Oakland, California, which he had
stringsearch-data/technical/911report/chapter-8.txt:                    California in the mid-1990s. A clandestine source said in 1998 that a Bin Ladin
stringsearch-data/technical/911report/chapter-8.txt:            In June 2000, Mihdhar left California and returned to Yemen. It is possible that if,
```
```
$ grep -r Toronto stringsearch-data/technical/biomed/
stringsearch-data/technical/biomed/1471-2180-2-32.txt:          of Toronto and Robert Sauer, MIT). In pKL106, the wild
stringsearch-data/technical/biomed/1471-2210-1-7.txt:          from Baxter Healthcare Corp. (Toronto, ONT, Canada) and
stringsearch-data/technical/biomed/1472-6882-2-5.txt:        in Toronto, Ontario.
stringsearch-data/technical/biomed/1472-6882-2-5.txt:        the Hospital for Sick Children in Toronto, Ontario, Canada.
stringsearch-data/technical/biomed/bcr285.txt:          method that was first developed in Toronto [ 15] and
stringsearch-data/technical/biomed/bcr285.txt:          method that was first developed in Toronto [ 15] and
stringsearch-data/technical/biomed/bcr631.txt:          Fitall (MTR software, Toronto, Canada) modified with an
```

## `grep -l`

The command `grep -l` prints the name of the file(s) that contain the matching string. This command is most useful when paired with the `-r` command option because it will list all the files within the specified directory that contain the matching string.

```
$ grep -l York stringsearch-data/technical/911report/chapter-1.txt
stringsearch-data/technical/911report/chapter-1.txt
```
```
$ grep -rl CIA stringsearch-data/technical/911report/
stringsearch-data/technical/911report/chapter-1.txt
stringsearch-data/technical/911report/chapter-10.txt
stringsearch-data/technical/911report/chapter-11.txt
stringsearch-data/technical/911report/chapter-13.1.txt
stringsearch-data/technical/911report/chapter-13.2.txt
stringsearch-data/technical/911report/chapter-13.3.txt
stringsearch-data/technical/911report/chapter-13.4.txt
stringsearch-data/technical/911report/chapter-13.5.txt
stringsearch-data/technical/911report/chapter-3.txt
stringsearch-data/technical/911report/chapter-5.txt
stringsearch-data/technical/911report/chapter-6.txt
stringsearch-data/technical/911report/chapter-8.txt
stringsearch-data/technical/911report/preface.txt
```
