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
- name: Tester le role ansible-role-quizlab
  hosts: all
  become: true
  roles:
    - ansible-role-quizlab
```

## Test

```bash
cd projet
ansible-playbook -i inventaire playbooks/ansible-role-quizlab.yaml
```

## Publication sur Ansible Galaxy

1. Creer le depot GitHub public du role (nom recommande: `ansible-role-quizlab`).
2. Pousser le role dans ce depot.
3. Se connecter a https://galaxy.ansible.com via compte GitHub.
4. Importer le role depuis l'interface Galaxy (My Content > Add Content > Import Role).
5. Verifier que `meta/main.yml` est present et correct (platforms, tags, license).

