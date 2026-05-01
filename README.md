``` sudo vim /etc/hosts
add entries for all nodes
```



###### 1. Navigate to the directory AppBuildDesign/TestFiles/app. Inspect the Dockerfile. Build the container image from the Dockerfile with the tag ckad-app:1.0.0. Run a container with the container image. Make the application available on port 1025. Execute a curl or wget command against the application’s endpoint.
<details>
<summary> Solution</summary>

```ls```

```
Dockerfile  package.json  spec  src
podman build -t ckad-app:1.0.0 .
podman image ls
podman run -d -p 1025:3000 7c01bebf22d2(imageID)
podman container ls
wget -O- localhost:1025
podman logs ac8fec488aba(conatinerID)
```
</details>

###### 2. Modify the Dockerfile from the previous exercise. Change the base image to the tag node:current-alpine3.20. Build the container image from the Dockerfile with the tag ckad-app:1.0.1. Ensure that container image has been created by listing it.
<details>


Practice exercises

1. Increase your efficiency when running kubectl commands by shortening kubectl and creating a shell alias to k.
2. Using the kubectl CLI tool, get the output of the pods running in the kube-system namespace, and show the pod IP addresses. Save the output of the command to a file named pod-ip-output.txt.
3. Upgrade the control plane components using kubeadm. When completed, check that everything, including kubelet and kubectl, is upgraded to version 1.32.1 (or the latest distribution of Kubernetes when you are reading this).

