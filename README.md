# homelab-ops-mini

Mini-project voor Ansible-beheer van één Ubuntu VM met Suricata.

Bewust minimaal: één host, één playbook, geen vault, geen Signal, geen roles.

## Structuur

```text
homelab-ops-mini/
├── inventory/
│   └── hosts.yml
├── playbooks/
│   └── vm-setup.yml
└── docs/
    └── flow.md
```

## Gebruik

```bash
uvx --from ansible-core ansible-playbook -i inventory/hosts.yml playbooks/vm-setup.yml -K --check --diff
uvx --from ansible-core ansible-playbook -i inventory/hosts.yml playbooks/vm-setup.yml -K
```

Per stap draai je `--tags check`, `--tags update` of `--tags suricata`.

Zie `docs/flow.md` voor het stroomdiagram.
