markdown
 Forensics Commands Cheat Sheet

Disk Imaging
| Command | Purpose |
| :--- | :--- |
| `dd if=/dev/sda of=image.dd bs=4096` | Disk imaging |
| `dcfldd if=/dev/sda of=image.dd hash=md5` | Imaging with hash |
| `ftkimager` | Windows disk imaging |

 File Analysis
| Command | Purpose |
| :--- | :--- |
| `file <file>` | Identify file type |
| `strings <file>` | Extract readable text |
| `binwalk <file>` | Extract embedded files |
| `xxd <file>` | Hex dump |

Memory Analysis (Volatility)
| Command | Purpose |
| :--- | :--- |
| `volatility -f memory.dmp imageinfo` | OS profile |
| `volatility -f memory.dmp --profile=Win10x64 pslist` | Processes |
| `volatility -f memory.dmp --profile=Win10x64 netscan` | Network |
| `volatility -f memory.dmp --profile=Win10x64 cmdscan` | Command history |

Timeline
| Command | Purpose |
| :--- | :--- |
| `log2timeline timeline.plaso /mnt/evidence/` | Create timeline |
| `psort -o l2tcsv timeline.plaso > timeline.csv` | Export timeline |

 Hashing
| Command | Purpose |
| :--- | :--- |
| `md5sum <file>` | MD5 hash |
| `sha1sum <file>` | SHA1 hash |
| `sha256sum <file>` | SHA256 hash |
