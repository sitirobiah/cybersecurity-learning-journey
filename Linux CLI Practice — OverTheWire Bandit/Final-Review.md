## Final review
Useful commands from the journey:
```bash
pwd
ls -la
cat filename
find . -type f
grep "text" filename
file filename
sort filename | uniq -u
ssh username@host -p 2220
chmod 600 keyfile
nc localhost PORT
```

## What matters most
The goal is not to memorize every command. It is to:
1. Read the challenge carefully.
2. Identify what information is missing.
3. Choose a command that can reveal that information.
4. Inspect the output and adjust the approach.
5. Explain what happened in your own words.

**Reminder:** Challenge-specific file names, ports, and conditions can differ. Use the official level instructions as the source of truth.
"""
files["02_Command_Reference/file_search_and_text.md"] = r"""# File Search and Text Commands

| Command | Simple meaning | Example |
|---|---|---|
| `pwd` | Show the current directory | `pwd` |
| `ls -la` | List files, including hidden files and details | `ls -la` |
| `cd folder` | Move to a directory | `cd /tmp` |
| `cat file` | Print a file's contents | `cat readme` |
| `find PATH -type f` | Find regular files | `find . -type f` |
| `grep "word" file` | Find lines containing text | `grep "hello" file` |
| `file name` | Identify a file type | `file data` |
| `strings file` | Extract readable strings | `strings data.bin` |
| `sort file` | Sort lines | `sort data.txt` |
| `uniq -u` | Show lines occurring once in sorted input | `sort data.txt \| uniq -u` |
| `diff A B` | Compare files | `diff old.txt new.txt` |
| `xxd file` | Display bytes in hexadecimal | `xxd data` |

**Tip:** Read command output carefully. Use `command --help` or `man command` to learn more when available.
"""
files["02_Command_Reference/permissions_and_ownership.md"] = r"""# Permissions and Ownership

## View permissions
```bash
ls -l
```
The output shows file type, permission bits, owner, group, size and timestamp.

## Change permissions
```bash
chmod 600 keyfile
```
`600` means the owner can read and write; group and others have no permissions.

## Search by owner or size
```bash
find / -type f -user username 2>/dev/null
find . -type f -size 100c
```
- `-user` filters by owner.
- `-size 100c` means exactly 100 bytes.
- `2>/dev/null` redirects error messages away from the terminal.

## Special permission: setuid
A setuid executable can run with the file owner's effective user ID. It is powerful and must be treated carefully.
"""
files["02_Command_Reference/ssh_and_scp.md"] = r"""# SSH and SCP

## SSH: remote terminal
```bash
ssh username@hostname -p 2220
```
- `ssh`: connect securely to a remote machine.
- `username@hostname`: account and server.
- `-p`: remote SSH port.

## SSH with a private key
```bash
chmod 600 keyfile
ssh -i keyfile username@hostname -p 2220
```
- `-i` selects the private key file.
- Restrict private-key permissions. Never commit private keys to a repository.

## SCP: copy files over SSH
```bash
scp -P 2220 localfile username@hostname:/remote/path/
```
- `scp` copies files between machines over SSH.
- `-P` (uppercase) sets the port for `scp`.
- Use `-p` (lowercase) with `scp` to preserve file timestamps and modes; it does not set the port.
"""
files["02_Command_Reference/network_tools_and_ports.md"] = r"""# Network Tools and Ports

## Netcat
```bash
nc localhost 30000
```
Connects to a service on the same machine at the specified port.

## OpenSSL TLS client
```bash
openssl s_client -connect localhost:30001
```
Starts a client connection that can negotiate TLS with a compatible service.

## Nmap
```bash
nmap -p 30000-30100 localhost
```
Checks the specified port range on the target. Scan only systems you own or have permission to test.

## Key terms
- **localhost:** the same computer from which the command runs.
- **IP address:** identifies a network interface or host.
- **Port:** identifies a service endpoint on a host.
- **TCP:** a transport protocol that provides a reliable byte stream.
- **TLS:** a protocol that can encrypt and authenticate a connection.
"""
files["02_Command_Reference/compression_and_archives.md"] = r"""# Compression and Archive Commands

| Tool | Purpose | Example |
|---|---|---|
| `file` | Identify file format | `file data` |
| `xxd` | Show hexadecimal bytes | `xxd data` |
| `xxd -r` | Convert a hex dump back to bytes | `xxd -r dump.hex output.bin` |
| `gzip -d` | Decompress gzip data | `gzip -d file.gz` |
| `bzip2 -d` | Decompress bzip2 data | `bzip2 -d file.bz2` |
| `tar -xf` | Extract a tar archive | `tar -xf archive.tar` |

**Workflow:** identify the file type with `file`, then choose the appropriate tool. When a challenge contains nested archives, work in a temporary directory and repeat the process as needed.
"""
files["02_Command_Reference/cron_and_suid.md"] = r"""# Cron and SUID

## Cron
Cron runs commands on a schedule.
```bash
ls -l /etc/cron.d/
cat /etc/cron.d/job_name
```
Read the configuration to find the command and user associated with a scheduled task.

## SUID
SUID is a special permission bit on executable files. When set, the program can run with the file owner's effective user ID.
```bash
ls -l
```
The permissions display may show `s` in the owner's execute position.

**Safety:** Learn about these mechanisms in an authorized lab. Do not attempt to exploit permissions or scheduled tasks on systems without permission.
"""
files["03_Lessons_Learned.md"] = r"""# Lessons Learned — OverTheWire Bandit

## Skills Practiced
- Navigating directories and reading files in a Linux terminal.
- Finding files using names, size, ownership and file type.
- Searching and transforming text.
- Understanding hidden files and Linux permissions.
- Connecting to remote systems with SSH and copying files with SCP.
- Using Netcat, OpenSSL and Nmap in a controlled lab.
- Inspecting compressed files and archives.
- Learning the basics of cron jobs and SUID permissions.

## My Learning Method
For each challenge, I practiced reading the instructions, identifying the information I needed, selecting a suitable command, and checking the output.

## What I Want to Improve
- Solve more tasks without following a tutorial.
- Explain why a command works, not only memorize its syntax.
- Become more comfortable with Linux permissions and networking.
- Keep clear notes and protect passwords, keys and other secrets.

## Next Step
Continue practicing Linux CLI tasks and apply the same method to beginner-friendly cybersecurity labs.

