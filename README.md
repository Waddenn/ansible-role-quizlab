# ansible-role-quizlab

Role Ansible portable pour deployer l'application Node.js `quiz-ansible` depuis GitLab sur Debian/Ubuntu et RedHat/Rocky Linux (conteneurs).

## Variables

- `quiz_repo_url` (defaut: `https://gitlab.com/ftutorials-labs/quiz-ansible.git`)
- `quiz_repo_version` (defaut: `HEAD`)
- `quiz_app_dir` (defaut: `/opt/quiz-ansible`)
- `quiz_port` (defaut: `3000`)
- `quiz_log_file` (defaut: `/tmp/quiz-ansible-role.log`)

## Exemple de playbook

```yaml
---
- name: Tester le role Waddenn.quizlab
  hosts: all
  become: true
  roles:
    - Waddenn.quizlab
```

## Test

```bash
cd projet
ansible-playbook -i inventaire playbooks/ansible-role-quizlab.yaml
```
