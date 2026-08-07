
- name: Week 1 Ansible Tasks
  hosts: app_servers
  become: yes

  tasks:
    # Task 1: Install Docker Packages and Start Docker Service
    - name: Install Docker
      apt:
        name: docker.io
        state: present
        update_cache: yes

    - name: Enable and start Docker service
      systemd:
        name: docker
        enabled: yes
        state: started

    # Task 2: Deploy Nginx Container on Application Server
    - name: Run Nginx container
      docker_container:
        name: nginx_app
        image: nginx:latest
        state: started
        ports:
          - "80:80"

    # Task 3: Delete Docker Container
    - name: Remove Nginx container
      docker_container:
        name: nginx_app
        state: absent

    # Task 4: Copy File to Docker Container
    - name: Copy index.html into container
      docker_container_copy:
        container: nginx_app
        src: ./index.html
        dest: /usr/share/nginx/html/index.html

    # Task 5: Troubleshoot Docker Container Issue
    - name: Check container logs
      command: docker logs nginx_app
      register: logs

    - debug:
        var: logs.stdout
  
