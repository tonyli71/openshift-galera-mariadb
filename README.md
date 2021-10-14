# openshift-galera-mariadb

How to use:

oc new-project my-mariadb-galera-app
oc new-app -f  mariadb-galera-persistent-template.yml
oc apply -f  galera-stateful2.yml 
