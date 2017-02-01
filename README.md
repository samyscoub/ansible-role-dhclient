# ansible-role-dhclient
An ansible role for configuring dhclient.
# Requirements
None.
# Role Variables
| Variable | Description | Default |
|----------|-------------|---------|
| dhclient\_host\_name | system hostname | somehost |
| dhclient\_domain\_name | system domain suffix | somedomain.com |
| dhclient\_domain\_search | default domain search suffix | {{ dhclient\_domain\_name }} |
| dhclient\_domain\_name\_servers | array of DNS server IP addresses | [] |
# Dependencies
None
# Example Playbook
```yaml 
- hosts: localhost
  vars:
    dhclient_host_name: myhost
    dhclient_domain_name: mydomain.com
    dhclient_domain_name_servers:
      - 8.8.8.8
      - 8.8.4.4
    dhclient_config:
  roles:
    - ansible-role-dhclient
```
