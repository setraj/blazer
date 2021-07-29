# blazer - CLI tool for uploading/downloading files

- Control thread count
- File verification with SHA
- Rich meta data
- Robust
- Resume from interruption

# usage
blazer -url=example.com/1.pdf -thread=10 -out=file.pdf

## Bugs:
- Handle improper URL
- Handle the case where there is no internet
- while downloading file if there is interruption and if the downloaded file is incomplete, what will you do,
you can find out incomplete file download by checking expected bytes to be written and bytes written, and then 
you can try to retry that attempt
- Get "https://sample-videos.com/img/Sample-jpg-image-30mb.jpg": read tcp 192.168.43.62:41606->103.145.51.95:443: read: connection reset by peer
- TCP timeout incase of large file
- Try to download a large file like 10 or 20 gb and 


## Resuming file

## Calcualating ETA
- ETA depends on the number of threads, download speed, speed of server

## Experiments and benchmarks
- Create a ruby server and try to serve a 10 gb file and try to do the same in go and other servers and
estimate performance and also node js

# Todo:
- show time elapsed
- support for verbose logging
- print the performance graph as well to see perfromance difference, using different number of threads and 
- storing data in current drive
- show progress
- also need support for google-drive, dropbox, a simple youtube version too.
- use interactive terminal to show progress across each thread, so it more cooler
- upload it to free file sharing service upto some MB, you can build one for yourself and share
// it with others, write in go, or node js and also use it here, a simple service
// the life of the service can be just 1 hour, there you can learn so many interesting things
- download files after giving username and password(with authentication)
- export as package too, later somehow
- show current download speed and ETA
large file sizes

# Roadmap:
- Write a compatable, high speed server to compliment this client
- Support torrent based
- GUI maybe in electron or QTCreate
