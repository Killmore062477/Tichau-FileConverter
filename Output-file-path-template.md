This template allows you to define how you want to generate the output file path (depending on the input file path).
You have access to the following informations:

Pattern		| Description				| Example (with input path: *C:\Music\Artist\Album\Song.wav*)
----------------|---------------------------------------|-----------------------------------------------------------------
(p)		| Input file path			| C:\Music\Artist\Album\
(p:d)		| My documents folder path		| C:\Users\UserName\Documents\
(p:m)		| My music folder path			| C:\Users\UserName\Music\
(p:v)		| My videos folder path			| C:\Users\UserName\Videos\
(p:p)		| My pictures path			| C:\Users\UserName\Pictures\
(f)		| Input file name			| Song
(o)		| Output file format			| mp3
(i)		| Input file format			| wav
(d0)		| Input parent folder name		| Album
(d1)		| Input sub parent folder name		| Artist
(n:i)		| Page number index			| (usefull for documents like pdf)
(n:c)		| Total page count			| (usefull for documents like pdf)
(d:format)	| Date using [.net ToString format](https://learn.microsoft.com/en-us/dotnet/api/system.datetime.tostring?view=net-8.0). Available for version >= 2.0 | 6.15.2008 9'15'07 PM

*Tips: You can use uppercase to retrieve caps lock informations. Example: (f) -> Default / (F) -> DEFAULT*

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

CDA extraction:
		
	Input: E:\Track01.cda
	Template: (p:m)CDA Extraction\(f)
	Generated output: C:\Users\UserName\Music\CDA Extraction\Track01.mp3

Pdf to image:
		
	Input: C:\Documents\TwoPagesDocument.pdf
	Template: (p)(f) (n:i) of (n:c)
	Generated outputs: C:\Documents\TwoPagesDocument 1 of 2.png and C:\Documents\TwoPagesDocument 2 of 2.png

Uses of conversion date:
		
	Input: C:\Music\Artist\Album\Song.wav
	Template: (p)(d:yyyy-MM-dd)\(f) 
	Generated outputs: C:\Music\Artist\Album\2008-15-06\Song.mp3