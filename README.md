# Ansible Role: Vyos Router Management


## Role Variables
Available variables are listed below, along with default values (see `defaults/main.yml`):

Set the path for the config backup. Path starts from / on ansible host.

    vyos_backup_path: 'backup'

Set the options for vyos_cmd variable in order for role to execute specific action.

    vyos_cmd: backup, addip2fw, delip2fw, addport2fw, delport2fw, addnewport2fw, addnewaddress2fw, addnewrule2fw

Set the description you wish to add to the interface.

    vyos_interface_description: 'interface description'

Set the interface name in the vyos router for which description need to be configured.

    vyos_interface: 'eth0'

Set variable to the ip address (single IP Address or with subnet like 0.0.0.0/0).

    vyos_fw_ipaddress: 

Set variable to predefined vyos firewall address group.

    vyos_fw_address_group: 

Set variable to port in vyos firewall port group.

vyos_fw_port:

Set variable to predefined vyos firewall port group.

    vyos_fw_port_group:

Set variable to predefined vyos firewall name.

    vyos_fw_name:

Set variable to rule number in vyos firewall.

    vyos_fw_rule_number:

Set variable to protocol (tcp, udp, tcp_udp, icmp etc).

    vyos_fw_protocol: 

Set variable to host (ip address or fqdn) for ping test.

    vyos_host: 

## Dependencies

None.

## Example Playbook

     - name: "playing vyos playbook"
       become: true
       hosts: all
       gather_facts: no
       roles:
        - bwdxbfzco.vyos