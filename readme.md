Для успешного запуска плейбука необходимо прописать корректные параметры доступа к удаленному серверу в файле

./inventory/host_vars/ah.yml

пример:

```
# Real host ip
ansible_host: <your IP>

# SSH user which connect to servers
ansible_user: <your admin user>
ansible_ssh_pass: <your pass>

#ansible_ssh_private_key_file: <path to key, if public key enabled>

# Uncomment for Latest DEB-based distros (Ubuntu, Debian)
ansible_python_interpreter: /usr/bin/python3
```

запуск производить командой:

```
ansible-playbook -i ./inventory/hosts.yml ./clickhouse.yml
```