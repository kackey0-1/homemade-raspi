# Build k8s on Rasberry PI 4

## References

- https://www.technicalife.net/raspberry-pi-kubernetes/#toc11 
- https://zenn.dev/eiden0029/articles/kubernetes-cluster
- https://qiita.com/TK_Yudai/items/3c7d22fb6a6e7d90f622
- https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/
-  https://qiita.com/kentarok/items/6e818c2e6cf66c55f19a

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

## cgroupについて

https://qiita.com/kentarok/items/6e818c2e6cf66c55f19a#os%E3%82%A4%E3%83%A1%E3%83%BC%E3%82%B8%E3%81%B8%E3%81%AE%E8%BF%BD%E5%8A%A0%E8%A8%AD%E5%AE%9A
