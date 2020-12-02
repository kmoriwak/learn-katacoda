# Adding a new role and settings

`sed -ie 's/tlog_scope_sssd: all/tlog_scope_sssd: all\n    timesync_ntp_servers:\n      - hostname: time-d-b.nist.gov\n        iburst: yes/' soe.yml`{{execute}}

`echo "    - role: rhel-system-roles.timesync" >> soe.yml`{{execute}}

`cat soe.yml`{{execute}}

`ansible-playbook soe.yml`{{execute}}