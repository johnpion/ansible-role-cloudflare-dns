# cloudflare_dns

## Requirements
OS: Debian 10

## Role Variables

## Dependencies

## Example Playbook
```
- hosts: cloudflare-dns
  roles:
    - role: cloudflare-dns
      tags: cloudflare-dns
```

## Example HostVars

```
cloudflare_email: admin@example.com
cloudflare_api_token: "{{ vault_cloudflare_api_token }}"

cloudflare_proxied: true

cloudflare_zone:
- name: example.com
  record:
  - value: 1.2.3.4
    proxied: True
  - name: www
    value: 1.2.3.4
    proxied: True
  - value: ASPMX.L.GOOGLE.COM
    type: MX
  - value: ALT1.ASPMX.L.GOOGLE.COM
    type: MX
    priority: 5
  - value: ALT2.ASPMX.L.GOOGLE.COM
    type: MX
    priority: 5
  - value: ASPMX2.GOOGLEMAIL.COM
    type: MX
    priority: 10
  - value: ASPMX3.GOOGLEMAIL.COM
    type: MX
    priority: 10
```

## Author Information
skype: john.seregin
