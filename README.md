### 🛡️ Metasploit: Meterpreter

**Room:** [Metasploit: Meterpreter — TryHackMe](https://tryhackme.com/room/meterpreter)  
**Status:** ✅ Completed  
**Date:** *03 June 2025*

---

### 🎯 Objective  
Understand how Meterpreter works, how it avoids detection, explore core commands, and practise post-exploitation techniques using Meterpreter on a compromised system.

---

### 🗝️ Key Concepts  
- **Meterpreter** — A powerful in-memory payload that allows full post-exploitation control over a compromised machine.
- **In-Memory Execution** — Meterpreter does not write to disk, reducing the chance of antivirus detection.
- **Encrypted C2** — Communicates with the attacker over encrypted channels, avoiding some IDS/IPS systems.
- **Staged vs Inline Payloads** — Payloads can be sent in steps (staged) or all at once (inline), depending on the situation.
- **Post-Exploitation** — Meterpreter includes many tools for gathering info, privilege escalation, and lateral movement.

---

### 🛠️ Tools Used  
- `msfvenom` — To list available payloads with `--list payloads | grep meterpreter`.  
- `msfconsole` — For launching and managing Meterpreter sessions.  
- `getuid`, `getpid`, `ps` — To identify user level and current process info.  
- `migrate`, `hashdump`, `search`, `shell`, `getsystem` — For key post-exploitation tasks.  
- `load kiwi` — Loaded Kiwi extension to access mimikatz-style credential tools.

---

### ⚠️ Challenges Faced  
- **Understanding the stealth** — It was tricky to grasp how Meterpreter hides in memory with no obvious file or process name.
- **Too many commands** — The number of commands was overwhelming at first, especially remembering which ones work only in certain situations.
- **Privilege management** — Migrating between processes risks losing SYSTEM access. I had to be careful about which process I moved to.

---

### 🧠 What I Learned  
- Meterpreter doesn’t leave a file trace, which is why it runs as something like `spoolsv.exe` instead of `meterpreter.exe`.
- You can’t always spot Meterpreter by checking running processes or DLLs.
- Tools like `ps`, `getuid`, and `getpid` help track what Meterpreter is doing.
- Meterpreter has lots of command categories (networking, system, UI, webcam, audio, etc.) and loads extra tools with `load`.

---

### 🌐 Real-World Application  
> Meterpreter is used by penetration testers and attackers to gain control of compromised machines, dump credentials, escalate privileges, and move laterally. It’s highly effective due to its stealth and wide feature set. In real-world pentests, commands like `hashdump`, `getsystem`, and `load kiwi` are often used to pivot further into the network.

---

### 💭 Reflections  
- **Not going to lie — the room before this room really made me question whether cyber security is right for me.**  
  It felt very hard, and I don’t know why it hit me so differently. There were moments I felt like giving up because the tools felt too advanced and hard to follow.  
- But now that I’ve completed this room, I feel more confident. This was one of the most technical and in-depth collection of rooms yet, and I got through it.  
- I’ll need more practice using Meterpreter commands and understanding post-exploitation workflows — especially `migrate`, `hashdump`, and `load`.  
- The main thing is I **didn’t quit**. These rooms tested me, but I finished it.
