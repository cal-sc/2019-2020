## DataCamp Notes:
### ID10: DataCamp: Shell Tutorial: Downloading data using Wget
1. What is Wget:
Wget:
. derives its name from World Wide Web and get
. native to Linux but compatible for all operating systems
. used to download data from HTTP(S) and FTP
. better than curl at downloading multiple files recursively

2. Check if Wget is installed correctly:
. command : Which wget

3. Wget installation by operating system:
. Wget source code: https://www.gnu.org/software/wget/
. Linux: run : sudo apt-get install wget
. MacOS: use homebrew and run : brew install wget
. Windows: download via gnuwin32

4. Browsing the Wget Manual:
. man command to print the Wget manual

5. Learning Wget Syntax:
Basic Wget syntax:
. wget [option flags] [URL]
URL is required.
. Wget also supports HTTP, HTTPS, FTP, and SFTP

6. Downloading a single file:
Option flags unique to Wget:
. -b: go to background immediately after startup
. -q: turn off the Wget output
. -c: resume broken download
. wget -bqc https://websitename.com/datafilename.txt
