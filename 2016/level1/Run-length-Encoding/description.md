Run-length encoding is a simple form of lossless data compression in which sequences of repeated data, or runs, are replaced by a single unit of the sequence and the number of times that unit repeats. It is most useful on data which contain many runs, such as simple graphics and animations.

In this problem, you will be given an archive of files that have been compressed using a form of run-length encoding. Unfortunately, the archive was stored on a server in a datacenter that experienced an electromagnetic pulse when a transformer exploded. Some of the files may have been corrupted in the blast. Your job is to decode the archive and toss out any corrupted data.

Here are the details of the encoding scheme:

The original files contained arbitrary hexadecimal data expressed in ASCII. The encoding was performed by replacing runs of single hex digits with a backslash character, followed by the length of the run, followed by the digit that was repeated. The run length is always encoded by a single hex digit. Normally, this would imply that the longest compressible run is 16 digits, but since it would be counterproductive to encode runs of length 1 or 2, those runs are left unchanged, and so the longest compressible run is actually 18. Thus, a 0 run length in the encoding represents 3 repeated digits, a 1 represents 4 digits, and so on.

For example, the run

CCCCC

would be encoded as

\2C

If the file contained a run longer than 18 digits, it simply broke the run into multiple encodings, starting from the left. For example, a run of 38 'A' digits would be replaced with

\FA\FAAA

Input definition

The input will contain an arbitrary number of lines of ASCII characters, each of which represents the run-length encoding of a single file.

In an uncorrupted file, only characters in the set {0, ..., 9} U {A, ..., F} U '\\' will appear, and all alphabetic characters will be capitalized. In other words, a valid file will contain hexadecimal digits along with the backslash ('\') character. A corrupted file could violate any of these constraints.

Output definition

Your output should contain the same number of lines as the input. On each line, print either the corresponding full, decoded file in all caps or, if the input's value indicated a courrupt file, the string "CORRUPTED".

Example input

0\083ACD4\5B007AA2F
919191919191\CC
88C\4B23\\3A7A622D2
AB8a933\2R004EE
Example output

08883ACD4BBBBBBBB007AA2F
919191919191CCCCCCCCCCCCCCC
CORRUPTED
CORRUPTED
