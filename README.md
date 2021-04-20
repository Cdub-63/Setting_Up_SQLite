# Setting Up SQLite
Binaries for SQLite can be installed at the SQLite Download page (https://www.sqlite.org/download.html).

## Windows
For Windows machines:
  - Download the sqlite-tools-win32-x86-xxxxxx.zip file and unzip it.
  - From your git-bash terminal, open the directory of the unzipped folder with cd ~/Downloads/sqlite-tools-win32-x86-xxxxxx/sqlite-tools-win32-x86-xxxxxx/.
  - Try running sqlite with the command winpty ./sqlite3.exe. If that command opens a sqlite> prompt, congratulations! You’ve installed SQLite.

![image](https://user-images.githubusercontent.com/44756128/115457462-334c7500-a1ea-11eb-9a9b-f2f1ffd3c1f8.png)

We want to be able to access this command quickly from elsewhere, so we’re going to create an alias to the command. Exit the sqlite> prompt by typing in Ctrl + C, and in the same git-bash terminal without changing folders, run these commands:

echo "alias sqlite3=\"winpty ${PWD}/sqlite3.exe\"" >> ~/.bashrc

and

source ~/.bashrc

The first command will create the alias sqlite3 that you can use to open a database. The second command will refresh your terminal so that you can start using this command. Try typing in the command sqlite3 newdb.sqlite. If you’re presented with a sqlite> prompt, you’ve successfully created the sqlite3 command for your terminal. Enter Ctrl + C to quit. You can also exit by typing .exit in the prompt and pressing Enter.

![image](https://user-images.githubusercontent.com/44756128/115457689-760e4d00-a1ea-11eb-86bd-42eddd08c052.png)

## Mac
For Macs, use the Mac OS X (x86) sqlite-tools package:
  - Install it, and unzip it.
  - In your terminal, navigate to the directory of the unzipped folder using cd.
  - Run the command mv sqlite3 /usr/local/bin/. This will add the command sqlite3 to your terminal path, allowing you to use the command from anywhere.
  - Try typing sqlite3 newdb.sqlite. If you’re presented with a sqlite> prompt, you’ve installed SQLite! Enter control + d to quit. You can also exit by typing .exit in the   prompt and pressing return.

## Linux
In Ubuntu or similar distributions:
  - Open your terminal and run sudo apt-get install sqlite3. Otherwise, use your distribution’s package managers.
  - Try typing in the command sqlite3 newdb.sqlite. If you’re presented with a sqlite> prompt, you’ve successfully created the sqlite3 command for your terminal. You can exit by typing .exit in the prompt and pressing enter.
