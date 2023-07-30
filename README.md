# Setup-New-Machine
Set of Ansible scripts to set up a new machine for SWX development

# Steps
1. Download this repo
2. Enter the download directory and run the prep bash script
```
./prep-ansible-install
```
Now Ansible should be installed on your machine. Check to make sure you have an ansible version >= 2.13.0

3. Set the location of this repo within machines.yml
```
repo_directory: "{{ home_directory }}/<path_to_this_repo>/Setup-New-Machine"
```

4. Run the core packages playbook.
```
ansible-playbook -i inventory/machines.yml playbooks/setup_core_packages.yml --ask-become-pass
```

5. A set of personal playbooks are included. You can choose which ones you would like to have. They can be executed in the following way
```
ansible-playbook -i inventory/machines.yml playbooks/<whichever_playbook_you_want_to_run> --ask-become-pass
```


