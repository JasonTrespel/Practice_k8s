## Simple Practice: Create K8s Objects

1. Create a Pod manifest from scratch using a text editor. Have the name of the Pod be `simplepod` using an `nginx:1.27.3` image. Have the container name be `simple-container` with a port number of `8080`.

<details>
<summary>Answer</summary>

```yaml
---
apiVersion: v1
kind: Pod
metadata:
  name: simplepod
spec:
  containers:
  - name: simple-container
    image: nginx:1.27.3
    ports:
    - containerPort: 8080
```
</details>



2. Create `newpod` with image `hello-world` using one command. For funnsies run the command `watch "kubectl get pods"` and look at the output for a minute or so.

<details>
<summary>
Answer</summary>
kubectl run newpod --image=hello-world
</details>
