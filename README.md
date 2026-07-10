# ansible-feishin

This role installs Feishin on Linux and macOS using the official GitHub release binaries.

## Supported platforms

- Debian/Ubuntu/Mint using the official DEB package
- Fedora/RHEL/CentOS and other non-Debian Linux distributions using the official AppImage
- macOS using the official DMG release asset

## Variables

- `feishin_version`: release tag to install (`latest` by default)
- `feishin_install_dir`: installation directory (`/opt/feishin`)
- `feishin_bin_path`: launcher path (`/usr/local/bin/feishin`)
- `feishin_create_desktop_entry`: create a desktop entry on Linux (`true`)

## Example playbook

```yaml
- hosts: all
  become: true
  roles:
    - role: ansible-feishin
      vars:
        feishin_version: latest
```

## Testing

```bash
ansible-playbook tests/test.yml -i tests/inventory --syntax-check
```

## License

MIT
