<p align="center">
  <img src="revuhl.png" alt="Revuhl Logo" width="200">
</p>

<h1 align="center">Revuhl</h1>

<p align="center">
  A fast, self-contained reverse shell generator for authorized penetration testing.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/shells-34+-green.svg" alt="Shells">
  <img src="https://img.shields.io/badge/dependencies-zero-brightgreen.svg" alt="No Dependencies">
</p>

---

## Features

- **34+ Reverse Shells** — Bash, Netcat, Python, PHP, PowerShell, CMD, Ruby, Perl, Socat, Lua, Awk, Java, curl, wget, msfvenom, and more
- **Live Preview** — Commands update instantly as you type your IP and port
- **Click to Copy** — One-click clipboard copy on every command
- **Encoding** — Optional Base64 or URL encoding for payload obfuscation
- **TTY Upgrade Snippets** — Built-in shell stabilization commands (Python PTY, stty, Socat TTY, rlwrap)
- **Listener Command** — Auto-generated `nc -lvnp` listener shown at the top
- **Zero Dependencies** — Single HTML file, no frameworks, no build step, works offline
- **Dark Theme** — Clean, modern UI designed for low-light environments

## Usage

1. Open `index.html` in any modern browser
2. Enter your **IP address** and **port**
3. Select a reverse shell from the list on the left
4. Click **Copy** to copy the generated command
5. Expand **TTY Shell Upgrade** for post-exploitation shell stabilization

## Shells Included

| Category | Shells |
|----------|--------|
| Bash | Bash -i, Bash read, Bash 5, Bash UDP |
| Netcat | nc -e, nc -c, nc mkfifo, nc -i (OpenBSD), ncat SSL, BusyBox nc |
| Python | Python3, Python3 subprocess, Python2 |
| PHP | exec, proc_open, system |
| PowerShell | TCPClient, Base64-encoded |
| CMD | cmd.exe wrapper |
| curl/wget | Pipe to bash |
| Ruby | spawn, fork |
| Perl | Socket, IO |
| Socat | Basic, TTY |
| Misc | Lua, Awk, Java, xterm, msfvenom (Linux/Windows) |

## TTY Upgrade

Expand the **TTY Shell Upgrade** section for step-by-step shell stabilization:

```
python3 -c 'import pty;pty.spawn("/bin/bash")'
# Ctrl+Z
stty raw -echo; fg
export TERM=xterm-256color
export SHELL=/bin/bash
stty rows 40 columns 160
```

## Disclaimer

**Revuhl is intended for authorized penetration testing and security assessments only.** Unauthorized access to computer systems is illegal. Always obtain proper written authorization before testing. The author is not responsible for misuse.

## License

[MIT](LICENSE)
