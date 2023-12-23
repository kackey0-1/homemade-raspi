# Raspi k8s

## Execute ansible

```bash
brew install hudochenkov/sshpass/sshpass
ansible-playbook site.yml -v --ask-pass -u ubuntu
```

## xxx

```bash
service containerd restart
service kubelet restart

sudo vim /var/lib/kubelet/config.yaml

containerd config default

service containerd status
service kubelet status 
journalctl -xeu kubelet
```
