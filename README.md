smart_windows_search
====================

given a file and a windows directory path, find (duplicate) files with the same size and md5sum in the search path

Motivation:
I was not sure if I should delete a video file on my flash card. It would be nice if I can find out
if the file has been stored somewhere on my computer. The trick is the file might have been renamed.
So the simple windows search (by name) won't do it.

With this script, you run it at command prompt.
* It compares your file with the search directory, if it finds a file with the same size,
  it further compares the md5sum of the two files. If there is a match, then we have found a
  duplicate

Requirements:
----------------------
* only tested on windows
* for 32 bit machine [python 3.3 x86] (http://www.python.org/ftp/python/3.3.2/python-3.3.2.msi)
* for 64 bit machine [python 3.3 x86-64] (http://www.python.org/ftp/python/3.3.2/python-3.3.2.amd64.msi)

Usage:
----------------------
      C:\Python3.3\python d:\scripts\smart_windows_search.py -h
      usage: C:\Python3.3\python smart_windows_search.py [-h] --file FILE --dir DIR

      optional arguments:
        -h, --help         show this help message and exit
        --file FILE        the file we want to check
        --dir DIR          the directory we want to check against for duplicate file
       
Example:
---------------------
After you downloaded the windows python msi file and install it. Let's say, you installed your python
at: C:\Python3.3 directory.

To find out the file: e:\DCIM\Canon\MVI_1101.mvi is already on D: drive, just run:

     C:\Python3.3\python D:\tmp\smart_windows_search.py --file e:\DCIM\Canon\MVI_1101.mvi --dir D:\
     
#
