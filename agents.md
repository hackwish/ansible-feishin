# Agent Configuration for ansible-feishin

## Role Management Agents

### Role Developer Agent
- Responsibility: maintain install logic, defaults, and templates
- Triggers: changes in tasks/, templates/, defaults/, vars/
- Tools: ansible-lint, ansible-playbook

### Test Agent
- Responsibility: validate syntax and role behavior
- Triggers: pull requests and local changes
- Tools: ansible-playbook, yamllint
