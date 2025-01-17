Session Buddy Tool
===========

A simple tool for managing [Session Buddy Chrome Extension](https://chrome.google.com/webstore/detail/session-buddy/edacconmaakjimmfgnblocblbcdcpbko) data, on Windows

Features:
* export to JSON
* clear saved sessions
* merge multiple sessions into one


## Requirements
* [python 2.7.18](https://www.python.org/downloads/release/python-2718/)
* [python-cjson](https://pypi.org/project/python-cjson/)
* [pathlib2](https://pypi.org/project/pathlib2/)
* sqlite3 (comes with python 2.7.18)

## Setup

Install requiremtents:
```
$ py -2 pip install -r requirements.txt
```

## Usage
```
$ py -2 session_buddy_tool.py -h
usage: session_buddy_tool.py [-h] -a {export,merge,clean} [-e EXCLUDE]
                             [-d DATABASE_PATH]

optional arguments:
  -h, --help            show this help message and exit
  -a {export,merge,clean}, --action {export,merge,clean}
                        Action: export as a JSON file, merge, clean
  -e EXCLUDE, --exclude EXCLUDE
                        Path to file with excluded urls
  -d DATABASE_PATH, --database_path DATABASE_PATH
                        Path to the database file
```
Example:
```
py -2 session_buddy_tool.py -a export -d "C:\Users\test\AppData\Local\Google\Chrome Beta\User Data\Default\databases\chrome-extension_dlhjgdimhamgfjmeeapfdlbhibfagijd_0\1"
```
