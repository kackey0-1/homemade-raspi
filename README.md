# Raspi k8s

https://qiita.com/TK_Yudai/items/3c7d22fb6a6e7d90f622
https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/
https://qiita.com/kentarok/items/6e818c2e6cf66c55f19a

## Execute ansible

```bash
brew install hudochenkov/sshpass/sshpass
ansible-playbook site.yml -v --ask-pass -u ubuntu -i <host_name>
```

memo

```bash
# restart container runtime
service containerd restart
# restart kubelet
service kubelet restart

sudo vim /var/lib/kubelet/config.yaml
containerd config default
journalctl -xeu kubelet
netstat -anp | grep LISTEN | grep tcp
```
