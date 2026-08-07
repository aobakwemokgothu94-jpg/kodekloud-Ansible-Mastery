kodekloud-Ansible-Mastery/
├── README.md          ← overview of the whole repo
├── Week 1/
│   ├── week1-ansible.yml
│   └── README.md      ← details for Week 1
├── Week 2/
│   ├── week2-ansible.yml
│   └── README.md      ← details for Week 2
├── Week 3/
│   ├── week3-ansible.yml
│   └── README.md      ← details for Week 3
└── Week 4/
├── week4-ansible.yml
└── README.md      ← details for Week 4
## Weeks Covered
- [Week 1 – Ansible Basics](./Week%201/README.md)
- [Week 2 – Ansible Modules Practice](./Week%202/README.md)
- [Week 3 – Advanced Ansible Modules](./Week%203/README.md)
- [Week 4 – Advanced Ansible Practice](./Week%204/README.md)

This repository contains my practice playbooks and notes for mastering Ansible, organized week by week.

## Weeks Covered
- **Week 1** – Ansible Basics  
  - Setup & Inventory  
  - Ad-hoc Commands  
  - Copy, File, Service modules  
  - [See Week 1 README](./Week%201/README.md)

- **Week 2** – Ansible Modules Practice  
  - Ping, Install Package, Archive, Unarchive, Blockinfile  
  - [See Week 2 README](./Week%202/README.md)

## How to Run
Use the following command to run any week’s playbook:
```bash
ansible-playbook weekX-ansible.yml -i inventory

## 📘Week 1 - Ansible Basics

This folder contains introductory playbooks for Week 1 practice.  
The focus is on getting familiar with Ansible fundamentals.

## Modules Covered
1. **Setup & Inventory** – Define hosts and groups  
2. **Ad‑hoc Commands** – Run quick checks with `ansible` CLI  
3. **Copy Module** – Transfer files to remote hosts  
4. **File Module** – Manage file attributes and permissions  
5. **Service Module** – Start, stop, and enable services  

## Example Usage
Run a playbook with:
```bash
ansible-playbook week1.yml -i inventory


##📘 Week 2 - Ansible Modules Practice

This folder contains the playbook `week2-ansible.yml` which demonstrates five Ansible modules.

## Tasks
1. **Ping** – Test connectivity with all hosts  
2. **Install Package** – Ensure nginx is installed  
3. **Archive** – Compress `/var/log` into a tarball  
4. **Unarchive** – Extract the tarball into `/tmp/logs`  
5. **Blockinfile** – Insert a custom server block into `nginx.conf`

## Usage
Run the playbook with:
```bash
ansible-playbook week2-ansible.yml -i inventory

##📘  Week 3 - Advanced Ansible Modules

This folder contains the playbook `week3-ansible.yml` which demonstrates advanced Ansible modules.

### Tasks
1. **File (Soft Links)** – Create a soft link from `/var/log/nginx` to `/tmp/nginx_logs_link`  
   *Revision Date: 2026-07-28*  
2. **ACL Module** – Grant user `developer` rwx permissions on `/var/www/html`  
   *Revision Date: 2026-07-29*  
3. **Service Module** – Ensure `nginx` service is running and enabled  
   *Revision Date: 2026-07-30*  
4. **Lineinfile Module** – Add `127.0.0.1 myapp.local` to `/etc/hosts`  
   *Revision Date: 2026-07-30*  
5. **Replace Module** – Replace port `8080` with `9090` in `nginx.conf`  
   *Revision Date: 2026-07-30*  

### Example Usage
```bash
ansible-playbook week3-ansible.yml -i inventory

## 📘 Week 4 - Advanced Ansible Practice

This folder contains the playbook `week4-ansible.yml` which demonstrates advanced Ansible concepts.

### Tasks
1. **Facts Gathering** – Collect system information using `setup`  
   *Revision Date: 2026-07-31*  
2. **Create Users and Groups** – Add group `developers` and user `devuser`  
   *Revision Date: 2026-08-01*  
3. **Jinja2 Templates** – Deploy configuration files from templates  
   *Revision Date: 2026-08-01*  
4. **Setup Httpd and PHP** – Install and configure Apache (`httpd`) with PHP support  
   *Revision Date: 2026-08-01*  
5. **Conditionals** – Apply tasks only when conditions are met (e.g., restart httpd on RedHat systems)  
   *Revision Date: 2026-08-01*  

### Example Usage
```bash
ansible-playbook week4-ansible.yml -i inventory
