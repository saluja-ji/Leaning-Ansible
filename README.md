# Ansible Playbook: Shell vs Module Approach (Beginner Notes)

This repository contains a simple Ansible playbook written to **understand the difference between using shell commands and using Ansible modules**.

The example uses **nginx** because it is simple and commonly used.

---

## What this playbook demonstrates

The playbook contains **two clearly separated approaches**:

1. **Shell approach**
   - Uses raw Linux commands (`apt`, `systemctl`)
   - Imperative style (tell the system *what to run*)
   - Included only for learning purposes

2. **Module approach (recommended)**
   - Uses Ansible modules (`apt`, `service`)
   - Declarative style (describe the *desired state*)
   - This is the correct Ansible way

---

## File details

- Playbook file is written in **YAML**
- `---` marks the beginning of the YAML document
- Each `- name:` at the top level represents a **play**
- Tasks run **top to bottom** in order

---

## Important Ansible concepts used

- `hosts: all`  
  Runs the play on all hosts defined in the inventory file

- `become: true`  
  Uses `sudo` to run tasks that require root privileges

- `tasks:`  
  List of actions Ansible will execute

- `tags:`  
  Used to run only selected tasks

---

## How to run the playbook

### Run the entire playbook
```bash
ansible-playbook playbook.yml


