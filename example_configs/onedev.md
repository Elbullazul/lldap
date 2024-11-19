# Configuration for Onedev
In Onedev, go to `Administration > Authentication Sources` and click `External Authentication`
Select `Generic LDAP`

* LDAP URL: Your lldap server's ip/hostname
* Authentication Required: On
* Manager DN: `uid=admin,ou=people,dc=example,dc=com`
* Manager Password: Your bind user's password
* User Search Base: `ou=people,dc=example,dc=com`
* User Full Name Attribute: `displayName`
* Email Attribute: mail
* User SSH Key Attribute: (Leave Blank)
* Group Retrieval: "Search Groups Using Filter"
* Group Search Base: `ou=groups,dc=example,dc=com`
* Group Search Filter" `(&(uniqueMember={0})(objectclass=groupOfUniqueNames))`
* Group Name Attribute: cn
* Create User As Guest: Off
* Default Group: "No Default Group"
* Timeout: 300

Replace every instance of `dc=example,dc=com` with your configured domain.

After applying the above settings, users should be able to log in with their user name.