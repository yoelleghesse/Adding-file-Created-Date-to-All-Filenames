The File Timestamp Prefixer is a Python script that prefixes the filenames of all files in a directory tree with the creation timestamp of each file. It utilizes the pathlib module to work with file paths and directories, and the datetime module to retrieve and format the creation timestamps of the files.

Clone the repo:

``git clone https://github.com/your-username/file-timestamp-prefixer.git``

Run the script:

``python file_timestamp_prefixer.py``

- Recursively iterates through a directory and its subdirectories.
- Retrieves the creation timestamp of each file and prefixes it to the filename in the format YYYY-MM-DD_HH:MM:SS.
- Uses the pathlib module for handling file paths and directories in a platform-independent manner.

Config:

- Modify the root_dir variable to specify the directory where the files are located.
- Ensure that the directory structure contains the files that you want to prefix with timestamps.

Ex., Suppose you have the following directory structure:

``files/
    ├── file1.txt (created on 2023-02-20 10:30:45)
    ├── folder1/
    │   ├── file2.txt (created on 2023-02-21 12:15:30)
    │   └── file3.txt (created on 2023-02-22 14:20:00)
    └── folder2/
        ├── file4.txt (created on 2023-02-23 16:45:10)
        └── file5.txt (created on 2023-02-24 18:00:25)
``

After running the script, the files will be renamed as follows:

``files/
    ├── 2023-02-20_10:30:45_file1.txt
    ├── folder1/
    │   ├── 2023-02-21_12:15:30_file2.txt
    │   └── 2023-02-22_14:20:00_file3.txt
    └── folder2/
        ├── 2023-02-23_16:45:10_file4.txt
        └── 2023-02-24_18:00:25_file5.txt
``
