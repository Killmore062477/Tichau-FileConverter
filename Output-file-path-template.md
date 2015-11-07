This template allow you to define how you want to generate the output file path (depending on the input file path).
You have access to the following informations:

Pattern	| Description					| Example (with input path: *C:\Music\Artist\Album\Song.wav*)
--------|-------------------------------|-----------------------------------------------------------------
(p)   	| Input file path				| C:\Music\Artist\Album\
(f)  	| Input file name				| Song
(o)		| Output file format			| mp3
(i)		| Input file format				| wav
(d0)	| Input parent folder name		| Album
(d1)	| Input sub parent folder name	| Artist

*Tips: You can use uppercase to retrieve caps lock informations. Example: (f) -> Default / (F) -> DEFAULT *

### Examples

Simple default template (just change the extension): 

	Input: C:\Music\Artist\Album\Song.wav
	Template: (p)(f)
	Generated output: C:\Music\Artist\Album\Song.mp3

File name customization:

	Input: C:\Music\Artist\Album\Song.wav
	Template: (p)(O)_(f) (from (i))
	Generated output: C:\Music\Artist\Album\MP3_Song (from wav).mp3
		
File path customization:
		
	Input: C:\Music\Artist\Album\Song.wav
	Template: D:\(o)\(d1)\(f)
	Generated output: D:\mp3\Artist\Song.mp3