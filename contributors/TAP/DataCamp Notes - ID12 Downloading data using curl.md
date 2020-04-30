## DataCamp Notes:
### ID12: DataCamp: Shell Tutorial: Downloading data using curl
1. What is curl:
Curl:
. is short for Client for URLs
. is a Unix comand line tool
. transfers data to and from a server
. is used to download data from HTTP(s) sites and FTP servers

2. Check curl installation:
Check curl installation:
. using command : man curl
. press q to exit curl manual

3. Learning curl Syntax:
Basic curl syntax:
. curl [option flags] [URL]
URL is required
. curl also supports HTTP, HTTPS, FTP, and SFTP.
For a full list of options available:
. curl --help

4. Downloading a Single File:
Example:
A single file is stored at :
. https://websitename.com/datafilename.txt
Use the optional flag -o to save the file with its original name:
. curl -0 https://websitename.com/datafilename.txt
To rename the file, use the lower case -o + new file name:
. curl -o renameddatafilename.txt https://websitename.com/datafilename.txt

5. Downloading Multiple Files using Wildcards:
Oftentimes, a server will host multiple data files, with similar filename:
. https://websitename.com/datafilename001.txt
. https://websitename.com/datafilename002.txt
...................
. https://websitename.com/datafilename100.txt
Using Wildcards(*):
Download every file hosted on https://websitename.com/ that starts with datafilename ends in .txt:
. curl -o https://websitename.com/datafilename*.txt

6. Downloading Multiple Files using Globbing Parser:
. curl -o https://websitename.com/datafilename[001-100].txt
Increment through the files and download every Nth file:
. curl -o https://websitename.com/datafilename[001-100:10].txt

7. Preemptive troubleshooting:
Curl has two particularly useful option flags in case of timeouts during download:
. -L : redirects the HTTP URL if a 300 error code occurs
. -C : resumes a previous file transfer if it times out before completion
