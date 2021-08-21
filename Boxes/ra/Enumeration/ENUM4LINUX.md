## Enum4linux Output
```
target:
  host: 10.10.209.35
  workgroup: ''
credentials:
  user: ''
  password: ''
  random_user: nhbfbkvy
services:
  LDAP:
    port: 389
    accessible: true
  LDAPS:
    port: 636
    accessible: true
  SMB:
    port: 445
    accessible: true
  SMB over NetBIOS:
    port: 139
    accessible: true
is_parent_dc: true
is_child_dc: false
long_domain: windcorp.thm
workgroup: WINDCORP
nmblookup: null
smb1_only: false
sessions_possible: true
null_session_possible: true
user_session_possible: false
random_user_session_possible: false
domain_sid: S-1-5-21-555431066-3599073733-176599750
member_of: domain
os_info: null
users: null
groups: null
shares: {}
policy: null
printers: null
errors:
  nmblookup:
    enum_netbios:
    - 'Could not get NetBIOS names information via ''nmblookup'': timed out'
  workgroup:
    enum_netbios:
    - 'Could not get NetBIOS names information via ''nmblookup'': timed out'
  random_user_session_possible:
    enum_sessions:
    - 'Could not establish random user session: STATUS_LOGON_FAILURE'
  os_info:
    enum_os_info:
    - 'Could not get OS info via ''srvinfo'': STATUS_ACCESS_DENIED'
  users:
    enum_users_rpc:
    - 'Could not find users via ''querydispinfo'': STATUS_ACCESS_DENIED'
    - 'Could not find users via ''enumdomusers'': STATUS_ACCESS_DENIED'
  groups:
    enum_groups_rpc:
    - 'Could not get groups via ''enumalsgroups domain'': STATUS_ACCESS_DENIED'
    - 'Could not get groups via ''enumalsgroups builtin'': STATUS_ACCESS_DENIED'
    - 'Could not get groups via ''enumdomgroups'': STATUS_ACCESS_DENIED'
  policy:
    enum_policy:
    - 'SamrConnect2 call failed on port 445/tcp: STATUS_ACCESS_DENIED'
    - DCE/SAMR named pipe connect failed on port 139/tcp
  printers:
    enum_printers:
    - 'Could not get printer info via ''enumprinters'': STATUS_ACCESS_DENIED'
```