#  Kustomization chart example
A very simnple example of a Kustomization chart that contains only a Deployment resource with NginX as an image.
## Components
There are two main components within the repository as follow:
### Base Resource
In this example, there is 1 simple base resource, which is a deployment that uses `nginx:1.17` image in a container.
### Kustomization overlay
The base directory contains the original Deployment definition.
The overlay directory is where you create the Kustomization overlay.
The resources field references the base directory.
The patches field defines a patch that targets the Deployment named my-app. It replaces the number of replicas from 1 to 3.

## Apply the Kustomization chart
Go to `/overlay` and use the following command to apply the chart
```bash
kubectl apply -k .
```
