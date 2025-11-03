# 01 — msfconsole basics

**Goal:** become fluent with `msfconsole` commands, module discovery, configuring modules, launching a module, and handling sessions (meterpreter/reverse shells). This is foundational — you should be able to find a module, configure it, and run it against a lab target.

**Preconditions / Lab**
- Attacker: Kali Linux (or any machine with Metasploit Framework installed).
- Target: an intentionally vulnerable VM (Metasploitable2, VulnHub box, or TryHackMe lab) on an isolated host-only/internal network you control.
- Never run these against systems you do not own or have explicit permission to test.

---

## Table of contents
1. Start and stop msfconsole  
2. Basic navigation: help, search, use, info  
3. Show and set options (required and optional)  
4. Running modules (exploit vs auxiliary)  
5. msfvenom preview (documentation-only command example)  
6. Handling sessions (meterpreter basics)  
7. Resource scripts (`.rc`) example  
8. Checkpoints & small exercises  
9. Troubleshooting notes

---

## 1) Start and stop msfconsole
Open a terminal and run:
```bash
# start msfconsole (may take a few seconds)
msfconsole
