# ubuntu_runner

## General 
```bash
sudo apt-get update
sudo apt-get upgrade
```

## Github runner 
```bash
mkdir actions-runner && cd actions-runner
curl -o actions-runner-linux-x64-2.288.1.tar.gz -L https://github.com/actions/runner/releases/download/v2.288.1/actions-runner-linux-x64-2.288.1.tar.gz
echo "325b89bdc1c67264ec6f4515afda4534f14a6477d9ba241da19c43f9bed2f5a6  actions-runner-linux-x64-2.288.1.tar.gz" | shasum -a 256 -c
tar xzf ./actions-runner-linux-x64-2.288.1.tar.gz
sudo ./bin/installdependencies.sh
./config.sh --url https://github.com/benjamindev-ops/template_CICD --token AWFE2ETYQPAVZH2LNY7JMM3CFJH3K   --unattended --work template_CICD
sudo ./svc.sh install
sudo ./svc.sh start
rm -rf actions-runner-linux-x64-2.288.1.tar.gz
```

## Jfrog Step 

```bash
curl -fL https://getcli.jfrog.io | sh
sudo mv ./jfrog /usr/local/bin/
jfrog config add
```

## Ansible step 
```bash
sudo apt install software-properties-common -Y
sudo apt-get install pip
sudo -H pip3 install ansible
ansible --version
```
