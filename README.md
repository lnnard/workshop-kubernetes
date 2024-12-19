# Kubernetes Workshop

This repository contains Kubernetes configuration files for a workshop.

## Files

- `hello-world.yaml`: Defines a Pod named `hello-world` in the `workshop-kubernetes` namespace.
- `namespace-workshop-kubernetes.yaml`: Defines the `workshop-kubernetes` namespace.

## Usage

1. Create the namespace:

    ```sh
    kubectl apply -f namespace-workshop-kubernetes.yaml
    ```

2. Deploy the `hello-world` Pod:

    ```sh
    kubectl apply -f hello-world.yaml
    ```

3. Verify the Pod is running:

    ```sh
    kubectl get pods -n workshop-kubernetes
    ```

## File Contents

### [namespace-workshop-kubernetes.yaml](namespace-workshop-kubernetes.yaml)

```yaml
apiVersion: v1
kind: Namespace
metadata:
  name: workshop-kubernetes