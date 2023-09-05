# What are Containers

- Kubernetes is also known as K8s
- What are containers
    - Completetly isolated enviornments, each with their own processes, services, networking or mounts just like a VM
    - Containers have been around for about 10 years
    - Docker isn't meant to virtualize and run operating systems
    - Dockers uses LXC containers to containerize applications
    - Containers all share the same operating system kernal
    - Docker can run any flavor of OS on top of it as long as it's based on the same kernal
        - Linux containers
        - Windows containers

    - Containers vs VMs
        - **Containers**
            - Hardware Infrastructure
                - Operating System
                    - Docker
                        - Container 1
                            - Application
                            - Libraries
                            - Dependancies
                        - Container 2
                            - Application
                            - Libraries
                            - Dependancies

        - **Virtual Machines**
            - Hardware Infrastructure
                - Operating System
                    - Hypervisor
                        - Virtual Machine 1
                            - Application
                            - Libraries
                            - Dependancies
                            - Operating System
                        - Virtual Machine 1
                            - Application
                            - Libraries
                            - Dependancies
                            - Operating System

    - Virtual machines have a higher utilization
    - Docker containers boot faster
    - You can find images of the most common operting systems, databases, services, and tools
    - Use `docker run _________________` to start application
        - `docker run mongodb`
    - Add as many instances as you want, then configure a load balancer




    - Containerize applications
    - Run each service with it's own dependancies in seperate containers
