---
layout: post
title: "Ansible Mastery - Weeks 1 to 4"
categories: ansible mastery
---

# Ansible Mastery: Weeks 1–4

---

## 📄 Week 1 Summary: Ansible Tasks
**Focus:** Container management and troubleshooting with Ansible.  
**Hosts:** `app_servers`  
**Privilege Escalation:** `become: yes`

### 🔑 Key Activities
- Installed Docker and ensured the service was enabled and running.  
- Deployed an Nginx container with port 80 exposed.  
- Practiced container lifecycle management by removing containers.  
- Copied files into containers (e.g., `index.html`) to customize content.  
- Troubleshot container issues by checking logs and displaying results.

### ✅ Takeaways
- Automated Docker installation and service management.  
- Practiced container lifecycle tasks: start, remove, copy files.  
- Gained experience in troubleshooting containers directly through Ansible.  
- Established a foundation for containerized application deployment.

---

## 📄 Week 2 Summary: Ansible Modules Practice
**Focus:** Practicing core Ansible modules for connectivity, package management, file archiving, and configuration updates.  
**Hosts:** `all`  
**Privilege Escalation:** `become: true`

### 🔑 Key Activities
- Verified connectivity with all hosts using `ping`.  
- Installed and ensured `nginx` was present with `package`.  
- Archived `/var/log` into a `.tar.gz` file.  
- Extracted archived logs with `unarchive`.  
- Inserted a custom block into `nginx.conf` using `blockinfile`.

### ✅ Takeaways
- Tested host connectivity with `ping`.  
- Automated package installation and management.  
- Practiced archiving and extracting files for maintenance.  
- Modified configuration files dynamically with `blockinfile`.  
- Strengthened skills in managing both system state and application configuration.

---

## 📄 Week 3 Summary: Advanced Ansible Modules Practice
**Focus:** Exploring advanced modules for file management, access control, service handling, and configuration editing.  
**Hosts:** `all`  
**Privilege Escalation:** `become: true`

### 🔑 Key Activities
- Created symbolic links with the `file` module.  
- Applied fine-grained access control using `acl`.  
- Ensured `nginx` service was running and enabled with `service`.  
- Inserted lines into `/etc/hosts` using `lineinfile`.  
- Automated text replacement in configs with `replace`.

### ✅ Takeaways
- Managed symbolic links with `file`.  
- Strengthened collaboration and security with `acl`.  
- Practiced reliable service management with `service`.  
- Ensured configuration consistency using `lineinfile`.  
- Automated configuration changes with `replace`.

---

## 📄 Week 4 Summary: Advanced Ansible Practice
**Focus:** Combining system facts, user management, templating, web service setup, and conditional logic for complex automation.  
**Hosts:** `all`  
**Privilege Escalation:** `become: true`

### 🔑 Key Activities
- Gathered system facts with `setup`.  
- Created a `developers` group and added a `devuser` account.  
- Deployed `nginx.conf` using a Jinja2 template.  
- Installed `httpd` and `php`, ensured `httpd` was running.  
- Restarted `httpd` conditionally when OS family was RedHat.

### ✅ Takeaways
- Gathered and leveraged system facts for smarter automation.  
- Automated user and group creation for consistent environments.  
- Applied Jinja2 templating for flexible configuration management.  
- Installed and managed web services (`httpd` + `php`).  
- Used conditionals to ensure tasks ran only when appropriate.
