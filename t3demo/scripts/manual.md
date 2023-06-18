## Description
Plugin can be used to retrieve resource utilization of pods or nodes in your Kubernetes cluster. Resource utilization is an important thing to monitor for Kubernetes cluster owners. In order to monitor resource utilization, you can keep track of things like CPU, Memory.

### Installation steps 
 Dowload file - *kubeplugin*

To use a plugin, make the plugin executable: 
    ```
    sudo chmod +x ./kubectl-foo
    ```
Place it anywhere in your PATH:
    ```
    sudo mv ./kubectl-foo /usr/local/bin
    ```

### How to use plugin 

You may now invoke your plugin as a kubectl command:

    ```
    kubectl kubeplugin <resourcetype> <namespace>
    ```
where:
resourcetype - node or pod
namespece -one of list : kubectl get namespacess

Output must be list of 
"Resource, Namespace, Name, CPU, Memory"



```
~ kubectl kubeplugin pod demo 
Resource: pod, Namespace: demo, Name: ambassador-844d658479-4l2kr, CPU: 79m, Memory: 266Mi
Resource: pod, Namespace: demo, Name: cache-8687c99dc4-p5qbz, CPU: 5m, Memory: 2Mi
Resource: pod, Namespace: demo, Name: db-648fd5f6cc-v2bvg, CPU: 20m, Memory: 370Mi
Resource: pod, Namespace: demo, Name: demo-api-7b997b4465-8h78p, CPU: 11m, Memory: 22Mi
Resource: pod, Namespace: demo, Name: demo-ascii-8bb5db8f7-6kdrt, CPU: 8m, Memory: 23Mi
Resource: pod, Namespace: demo, Name: demo-data-866b75478-b22qr, CPU: 7m, Memory: 23Mi
Resource: pod, Namespace: demo, Name: demo-front-df4dfc9cf-22d7h, CPU: 5m, Memory: 21Mi
Resource: pod, Namespace: demo, Name: demo-img-66b64c59d8-4dnkm, CPU: 7m, Memory: 25Mi
Resource: pod, Namespace: demo, Name: demo-nats-0, CPU: 3m, Memory: 26Mi
Resource: pod, Namespace: demo, Name: demo-nats-box-fc77b65ff-rfpqm, CPU: 1m, Memory: 0Mi
```
