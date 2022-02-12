# Ansible role: `system_dns`

Ansible role to manage DNS configuration.

⚠️ **This role has been moved into the collection [jpclipffel.system](https://github.com/jpclipffel/ansible_collection.system):**
* GitHub: https://github.com/jpclipffel/ansible_collection.system
* Ansible Galaxy: https://galaxy.ansible.com/jpclipffel/system

---

## Tags

| Tag     | Description             |
|---------|-------------------------|
| `setup` | Setup DNS configuration |

## Variables

| Variable              | Type                 | Required | Defaut               | Description                                                |
|-----------------------|----------------------|----------|----------------------|------------------------------------------------------------|
| `system_dns_resolver` | `string`             | No       | `resolv.conf`        | Ansible user account (`systemd-resolved` or `resolv.conf`) |
| `system_dns_servers`  | `list` of `IP`       | No       | `[ '172.29.245.1' ]` | List of DNS servers                                        |
| `system_dns_options`  | `list` of `string`   | No       | `[ 'edns0' ]`        | List of DNS options to use with `resolv.conf`              |
| `system_dns_search`   | `list` of `hostname` | No       | `[ 'dt.ept.lu' ]`    | List of search domains                                     |

## Templates

| Template         | Description            |
|------------------|------------------------|
| `resolv.conf.j2` | `resolv.conf` template |
