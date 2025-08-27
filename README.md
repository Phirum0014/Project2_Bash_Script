# Safe Trash-enabled rm and restore System

**Student Name:** Phirum  
**Date:** 27 August 2025

---

## Scripts

### `rm`
- Safe deletion script.
- Moves files/directories to `/tmp/trash` instead of permanently deleting.
- Supports `-r` for recursive deletion of directories.
- Logs each deletion with timestamp, original path, and trash path in `/tmp/trash/trash.log`.
- Handles errors for nonexistent files or directories without `-r`.

### `restore`
- Restores deleted files/directories from `/tmp/trash`.
- Uses the log file to find the original location.
- Restores the most recent deletion if multiple matches.
- Warns or renames if the destination already has a file.

---

## How to use

1. Delete a file:

```bash
rm file.txt
