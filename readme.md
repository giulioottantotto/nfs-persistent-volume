```
oc project
oc create -f nfs-pv.yml 
oc describe pv volume-persistente
oc create -f nfs-claim.yml 
oc describe pvc volume-persistente
oc get dc
oc set volume dc/test-scc --add --name=volume-claim-persistente --type=persistentVolumeClaim -claim-name=volume-persistente --mount-path=/giulio
oc get pod
oc rsh test-scc-15-6qqz8
```