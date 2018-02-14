# ansible-ethereum

### remote install

```
echo "[all]" > ./hosts
echo "192.168.0.1" >> ./hosts
ansible-playbook -i ./hosts ./coind/ethereum.yml -u centos --private-key=privatekeyfile
```

### local install

```
yum install -y epel-release
yum install -y git ansible
echo "[all]" > ./hosts
echo "localhost" >> ./hosts
ansible-playbook --connection=local -i ./hosts ./coind/ethereum.yml
```
