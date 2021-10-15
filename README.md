# openshift-galera-mariadb

This mariadb DB on Galera for Tow Site Active-Active Model DataBase Cluster <br>
It can be use on Openshift 4.8.11 and Submariner

How to use:

oc new-project my-mariadb-galera-app 

oc new-app -f  mariadb-galera-persistent-template.yml

OR

oc apply -f  galera-stateful.yml 

subctl export service --namespace my-mariadb-galera-app galera-stateful

find peer site DNS ip :
oc describe dns.operator/default | grep "Cluster IP" | awk -F ':' '{print $2}' | awk '{print $1}'
