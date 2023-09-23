# ansible

1. Create a inventory with all the servers that ansible will work with --> nano inventory add IPs or Domains
2. Connect ansible to all the servers
   --> -ansible all --key-file ~/.ssh/ansible -i inventory -m ping
shorten --> ansible all -m ping (if ansible.cfg was created)

3. ansible all -m gather_facts --limit

4. how to do an action with ansible:
   --> ansible all -m apt -a update_cache=true --become --ask-become-pass 
   --> --become --ask-become-pass gives you access to sudo so you can do everything

5. Downloading vim-nox with Ansible:
   --> ansible all -m apt -a name=vim-nox --become --ask-become-pass

6. Donwloading lastest version of snapd
   --> ansible all -m apt -a "name=snapd state=latest" --become --ask-become-pass

7.
