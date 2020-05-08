# polkadot

This project will help you to deploy a Polkadot (https://github.com/paritytech/polkadot) network via ansible.

Steps:

1. Edit hosts file:
```
$ vi ansible/inventory/hosts
[nodes]
192.168.x.x ansible_connection=ssh  ansible_user=root
```
2. Run polkadot playbook:
```
$ ansible-playbook ansible/plays/main.yml -k -u root
```
Above playbook will help you to deploy a polkadot nodes. Also, it will deploy monitoring stack including prometheus. an exporter for monitoring polkadot nodes [https://github.com/mixbytes/polkadot-prometheus-exporter] and grafana for visulaisation.

3. Acessing dashboards:
```
Prometheus: http://<IP>:9090/
Grafana: http://<IP>:3000/
Exporter: http://<IP>:9091/
```
