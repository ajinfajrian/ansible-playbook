## README

1. Edit inventory file with your environment
2. Edit vars on playbook `k8s-nginx-proxy.yaml` with your ip master

```yaml
- name: Depedencies preparation on worker
  vars:
    master1: 172.18.215.11
    master2: 172.18.215.12
    master3: 172.18.215.13
```
3. Before join please mapping domain /etc/hosts on master 1 / provisioniner with your environment

4. Test connectivity
```sh
ansible -i inventory -m ping all
```

5. Running job
```sh
ansible-playbook -i inventory k8s-nginx-proxy.yaml
```
