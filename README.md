# Automated File Sorter Python Project

Automated File Sorter! This Python tool is designed to keep your file directories organized by automatically sorting files into specific folders based on their file types. With this script, managing and decluttering your workspaces becomes much easier, as files are categorized without manual effort.

**Project Overview**

The Automated File Sorter leverages Python’s **os** and **shutil** modules to move files into designated folders based on their file extensions. This project is perfect for users who regularly work with mixed file types in one directory, such as **.json**, **.txt**, **.PNG**, and **.xlsx** files. By creating folders for each type and moving files accordingly, this script helps maintain a neat and structured file explorer.

**How It Works**

Specify the Directory Path: Define the directory you want to organize by setting the **path** variable.
Create Folders by File Type: The script checks for folders labeled by file type (e.g., "json files", "image files") and creates them if they don't already exist.
Sort Files into Folders: Files with extensions like **.json**, **.txt**, **.PNG**, and **.xlsx** are moved into their respective folders.

**Code Explanation**

**1) Imports and Path Setup:**

      import os, shutil
      path = r"C:/path/to/your/directory"

* **os:** Provides functions for interacting with the operating system.
  
* **shutil:** Offers high-level file operations, like moving files.

**2) Folder Creation:**

      folder_names = ['json files','image files', 'text files', 'excel files']
      for loop in range(0,4):
          if not os.path.exists(path + folder_names[loop]):
              os.makedirs(path + folder_names[loop])

* Checks if folders for each file type exist; if not, they are created.

**3) File Sorting Logic:**

      for file in file_name:
          if ".json" in file and not os.path.exists(path + "json files/" + file):
              shutil.move(path + file, path + "json files/" + file)
          # Other file types follow similar structure

* Loops through each file and moves it to its designated folder based on its extension.

**Customization**

To add support for other file types, simply:

1) Add a folder name to **folder_names**.
2) Insert an additional **elif** clause to check for the file extension and move it to the corresponding folder.

**Conclusion**

This Automated File Sorter is an efficient solution for anyone who regularly handles multiple file types in a single directory. By running this Python script, users can save time, avoid clutter, and streamline file organization in any workspace.





