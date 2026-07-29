# AGENTS.md - ansible-feishin

## Testing

```bash
ansible-playbook tests/test.yml -i tests/inventory --syntax-check
```

## CI/CD

- Semantic-release runs on push to `master` or `main` branches
- Uses Conventional Commits format for release automation

## Structure

- Standard Ansible role layout: `tasks/`, `handlers/`, `templates/`, `defaults/`, `vars/`
- Platform-specific tasks: `install_linux.yml`, `install_macos.yml`, `verify.yml`
- Role tests run against `localhost` with `become: true`

## Key Files

- `defaults/main.yml` - default variables (version, install paths)
- `tasks/main.yml` - entry point that dispatches to platform-specific tasks
- `ansible.cfg` - sets `roles_path=../` for testing from parent directory
