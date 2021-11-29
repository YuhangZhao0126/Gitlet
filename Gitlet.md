# Gitlet

## Internal structure

* **blobs**: The saved contents of files. Since Gitlet saves many versions of files, a single file might correspond to multiple blobs: each being tracked in a different commit.

- **trees**: Directory structures mapping names to references to blobs and other trees (subdirectories).

- **commits**: Combinations of log messages, other metadata (commit date, author, etc.), a reference to a tree, and references to parent commits. The repository also maintains a mapping from *branch heads* to references to commits, so that certain important commits have symbolic names.

  ### hash

  * including all metadata and references when hash a **commit**
  * 区分 hash for **commits** and hash for **blobs**
    1. well thought directory structure within .getlet
    2. Another way to do so is to hash in an extra word for each object that has one value for blobs and another for commits.

  SHA-1 hash value: 40-character hexadecimal string

![image-20211107172711315](C:\Users\Joker\Desktop\Master\openCourses\cs61b\Gitlet\image-20211107172711315.png)



* head
* objects
* refs