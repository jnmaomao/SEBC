```
[root@cmnode krb5kdc]# cat /etc/krb5.conf 
[libdefaults]
default_realm = JNMAOMAO.CN
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = arcfour-hmac
default_tkt_enctypes = arcfour-hmac
permitted_enctypes = arcfour-hmac
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
JNMAOMAO.CN = {
kdc = cmnode.com
admin_server = cmnode.com
}
```