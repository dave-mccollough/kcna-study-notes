# Runtime - CRI

- Container Runtime Enviornment (CRI) lets any container vendor work as a container runtime for Kubernetes

  - Rkt
  - containerd

- Kubernetes can support different runtime enviornments without having to modify Kubernetes code
- CRI defines the gRPC protocol that Kubernetes Kubelet uses to interact with container runtimes
