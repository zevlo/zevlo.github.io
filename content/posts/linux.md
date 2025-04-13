---
title: "Learning Linux"
date: 2025-02-21
description: "Documenting my progress as I build a solid Linux foundation for DevOps."
draft: false
---

## Introduction
Welcome to the first step of my DevOps journey: learning Linux. In this blog post, I'll outline my **goal**, the **topics** I'm focusing on, and the **projects** that I'll undertake to solidify my understanding. This learning phase is all about building a strong foundation in Linux, which underpins almost all modern DevOps tools and practices.

---

## Goal
- **Get comfortable with the Linux command line, file system, user permissions, basic system administration, and essential tools.**
- **Build a foundation for all subsequent DevOps work.** 
- **Learn about the Linux file system hierarchy** (e.g., `/`, `/home`, `/var`, `/etc`, etc.).

Essentially, I want to feel at home in a Linux environment—navigating directories, understanding file permissions, managing processes, and automating tasks.

---

## Topics
1. **Basic commands**  
   Commands like `ls`, `cd`, `cp`, `mv`, `cat`, `grep`, and `find` are the backbone of day-to-day operations in Linux. Mastering these will make me more efficient in navigating and manipulating files.

2. **User and group management**  
   Tools such as `adduser`, `passwd`, `chmod`, and `chown` allow for secure multi-user environments. Understanding these is critical to maintaining proper access controls.

3. **Process management**  
   Utilities like `ps`, `top`, and `kill` help me monitor and manage running processes. This knowledge is indispensable when diagnosing performance issues or rogue processes.

4. **Package management**  
   Depending on the distribution, I might use `apt`, `yum`, or `dnf`. Knowing how to install, update, and remove packages is key to keeping systems up to date and secure.

5. **Basic shell scripting structure**  
   Learning about shebang lines, variables, loops, and conditionals will empower me to automate repetitive tasks. Even a simple script can save hours of manual work.

6. **TryHackMe: “Linux Fundamentals” series**  
   This interactive platform offers a fun way to practice and reinforce Linux skills in a gamified environment. It’ll help me fill in any knowledge gaps and keep things exciting.

---

## Projects
1. **Set up a Linux VM**  
   I can use VirtualBox or a small cloud instance (e.g., AWS Free Tier) to create a safe sandbox for experimenting with Linux commands and configurations.

2. **Create a user, configure SSH keys, and secure SSH access**  
   After spinning up the VM, I’ll create a non-root user, generate and copy SSH keys, and disable root login in the `sshd_config`. This step will help me understand the basics of securing a remote Linux system.

3. **Practice file/directory permissions**  
   I’ll create directories, assign various permissions, and test restricted access. This hands-on exercise will clarify concepts like `chmod`, `chown`, and user groups.

4. **Write a simple shell script**  
   My script will automate system updates or gather system information (e.g., CPU, memory, disk usage) to showcase loops, conditionals, and variables. This will reinforce my shell scripting basics.

---

## Closing Thoughts
Learning Linux might seem daunting at first, but it’s an investment that pays massive dividends in the world of DevOps. By tackling the goals, topics, and projects outlined above, I’ll be well on my way to a deeper understanding of how Linux systems operate, paving the way for more advanced DevOps skills.

In the next posts, I’ll share my experiences, pitfalls, and solutions as I complete each project. Stay tuned for more on this DevOps learning journey.
