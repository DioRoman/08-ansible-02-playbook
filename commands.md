cd /mnt/c/Users/rlyst/Netology/ter_vm_dev/src

cd /mnt/c/Users/rlyst/Netology/08-ansible-02-playbook/playbook

ansible-playbook -i inventory/prod.yml vector.yml --limit "vector"

ansible-playbook -i inventory/prod.yml clickhouse.yml --limit "clickhouse"

terraform destroy -auto-approve && terraform apply -auto-approve

ansible-lint site.yml

sudo truncate -s 0 /var/log/syslog