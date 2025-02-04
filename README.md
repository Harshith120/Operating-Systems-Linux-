# Operating-Systems-Linux-

                                                                    **Objectives of the Program:**

**File System Management:**

The FSManage and Disk classes implement a custom file system.
Supports creating, formatting, opening, saving, and removing file systems.

**File Operations:**

Creating files: put(std::string name) - Adds a new file to the file system.
Reading files: get(std::string name) - Retrieves a file from the file system.
Listing files: list_fs() - Displays all stored files with metadata.
Removing files: remove(std::string name) - Deletes a file from the file system.
Renaming files: rename(std::string old_file_name, std::string new_file_name).
Checking file ownership: user(std::string name) - Displays and allows changing file ownership.

**Storage and Memory Management:**

Implements a block-based storage system using FS::DataBlock, FS::BlockPointer, and FS::DiskAttribute.
Uses bitmap allocation to track free space and prevent fragmentation.
Manages file metadata including inode, size, modification time, and ownership.

**Exception Handling and Error Handling:**

Uses try-catch blocks to handle errors when performing file operations.
Prevents file name duplication and prompts users before overwriting.
Ensures sufficient storage space before adding new files.

**Persistence of File System:****

Uses binary file I/O (ifstream and ofstream) to store and retrieve file system data.
Reads and writes the disk structure to a file (open_fs() and save_fs()).


**How It Works:**

When a new file system is created, it allocates blocks for file metadata, directory structure, and free space tracking.
Files are stored block-wise, meaning a file may span across multiple disk blocks.
File retrieval reads blocks in order and reconstructs the file.
If storage space is insufficient, the program throws an error.
Uses linked lists and data structures to organize file metadata efficiently.

**Use Case:**

This type of file system simulation is useful for:

Understanding file system architecture (inode-based storage, block allocation).
Implementing virtual file storage in embedded systems.
Designing custom storage solutions for specific applications.
