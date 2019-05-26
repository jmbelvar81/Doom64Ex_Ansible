# DOOM64 EX ANSIBLE PLAYBOOK AND ROLE
---

Repository with an Ansible Role that Allows you Install and Launch Doom64EX Game.

The original Doom64EX referenced in this *"automation"* sourcecode can be found on:

  - https://github.com/svkaiser/Doom64EX

## Objective

This Repository contains:

  - Inventory to indicate machines where install Doom64Ex 
    (The Password has to be included by you in local connections or another situation) 
  - Playbook to invoke the Role that install the Game using the required role 
  - An ansible role with the required tasks to obtain the sourcecode and compile it 

## Tested On

Currently this source code only was tested on:

  - Ubuntu 18.04

## HowTo Test Connectivity

From the directory that contains this role execute:

```bash
ansible -i inventories/doom64ex_inventory.yml all -m ping
```

## HowTo execute the Role

Also from the directory that contains the role, execute:

```bash
# Notes: 
#   - Use flag "-vvv" to debug in detail 
#   - Use flag "--check" to execute a dry-run "previously to real execution"
#
ansible-playbook -i inventories/doom64ex_inventory.yml doom64ex_playbook.yml
```

## VIP NOTE ABOUT THE N64 ROM 

It's necessary you obtain the N64 Game ROM for yourself. Then you can copy to directory:

> <path to ansible role>/files/original_n64_rom/

With the name:

> doom64.z64

**By Legal Reasons I CAN'T FACILITATE THE FILE :-( , SORRY!!!**
