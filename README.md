# Ansible role **minikube**

Configure minikube cluster

## Requirements

* Ansible >= 2.9 (Earlier versions may work, but I haven't tested)
* Python 3 installed
* This is tested only in Ubuntu, but should work in other Linux based systems

## Role Variables

All variables in [default/main.yml](defaults/main.yml) can be overridden

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
|`minikube_driver`| docker | minikube [driver options](https://minikube.sigs.k8s.io/docs/drivers/)|
|`kubectl_install`|false| Flag to specify kubectl installation|
|`kubectl_version`| latest | kubectl version to install|

## Dependencies

## Example Playbook

This role is not released in galaxy yet to utilze this role, you can add this repo as a git submodule

```bash
git submodule add -b main https://github.com/slashpai/ansible-minikube.git roles/minikube
```

```yaml
- hosts: all
  roles:
    - minikube
```

Example [playbook](https://github.com/slashpai/ansible_playbooks/tree/main/minikube)

To get role updates

```bash
git submodule update --remote
```

## Contributing

## License

[MIT](LICENSE)
