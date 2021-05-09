# openshift-hello-php
This is a sample php application for OpenShift.

To deploy the application, run `oc new-app` command like this:
```
oc new-project demo
oc new-app https://github.com/orimanabu/openshift-hello-php --name hello
```

After a while, you will see a pod and a service.
```
oc get po
oc get svc
```

To access the pod from outside of the cluster, create route for the svc.
```
oc expose svc/hello
oc get route
```
