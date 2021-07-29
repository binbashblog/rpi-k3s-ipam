# Set secure passwords for IPAM via secretkey

```shell
$ read -s IPAM_DB_PASSWD
$ kubectl -n ipam create secret generic phpipam-passwd-root --from-literal=secretkey="$(pwgen -cns1 20)"
$ kubectl -n ipam create secret generic phpipam-passwd-ipam --from-literal=secretkey="$IPAM_DB_PASSWD"
```

