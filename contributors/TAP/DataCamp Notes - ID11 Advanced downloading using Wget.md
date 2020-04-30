## DataCamp Notes:
### ID11: DataCamp: Shell Tutorial: Advanced downloading using Wget
1. Multiple file downloading with Wget:
Save a list of file locations in a text file
. cat url_list.txt
Dowloading from the URL locations stored within the file url_list.txt using -i
. wget -i url_list.txt

2. Setting download constraints for large files:
Set upper download bandwidth limit(by default in bytes per second) with --limit-rare
Syntax:
. wget --limit-rare={rate}k {file_location}
Example
. wget --limit-rare=200k -i url_list.txt

3. Setting download constraints for small files
Set a mandatory pause time(in seconds) between file downloads with --wait
Syntax:
. wget --wait={seconds} {file_location}
Example:
. wget --wait=2.5 -i url_list.txt

4. curl versus Wget:
curl advantages:
. can be used for downloading and uploading files from 20+ protocols
. easier to install across all operating system
Wget advantages:
. Its ability for handling multiple file downloads
. dowload just about anything from a full file directory(e.g file directory, HTML page)