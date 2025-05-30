# Tutorial-11

## Reflection

### Reflection on Hello Minikube

1. Initially, when the pod was just running internally, the logs would only show the startup messages indicating that the HTTP server started on port 8080 and UDP server on port 8081. However, after exposing it as a Service and accessing it through the browser, the logs will show additional entries each time I accesses the application. Every HTTP request made to the application generates new log entries showing the incoming requests.

2. The -n option specifies which Kubernetes namespace to query for resources. In the first kubectl get commands without the -n option, kubectl defaults to the "default" namespace, which is where user-created resources like the hello-node deployment and service are placed unless explicitly specified otherwise. When using -n kube-system, the command specifically targets the "kube-system" namespace, which is a special namespace reserved for Kubernetes system components and infrastructure pods. This is why the output doesn't show the hello-node pod and service that were explicitly create. They exist in the default namespace, not in kube-system.
