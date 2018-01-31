current-dir = $(shell pwd)
ansible = $(shell command -v ansible)
ansible-playbook = $(shell command -v ansible-playbook)
ansible-flags = -e ansible_python_interpreter=/usr/bin/python3
playbook = provisioning/playbook.yml

export ANSIBLE_HOSTS=$(current-dir)/provisioning/inventory
export ANSIBLE_CONFIG=$(current-dir)/provisioning/ansible.cfg

ping :
	$(ansible) all $(ansible-flags) -m ping

run-playbook :
	$(ansible-playbook) $(playbook) $(ansible-flags)

list-hosts :
	$(ansible-playbook) $(playbook) $(ansible-flags) --list-hosts
