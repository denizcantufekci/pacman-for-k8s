# Running Pac-Man on Kubernetes

Pac-Man the classic arcade game - deployment files for v1.29 k8s

<img src="https://veducate.co.uk/wp-content/uploads/2021/09/Pac-Man-UI.jpg" width=45% height=45%>

### Using a Script for installation
Clone repo and run ```chmod +X pacman-install.sh``` and then run file ```./pacman-install.sh```

#### Uninstall using a Script
Run file `./pacman-uninstall.sh`. This will delete all objects created by `./pacman-install.sh`

### Upgrade

Added portworx storage class
Added stork scheculer
Added PodSecurityAdmission label to namespace manifest
Removed PSP manifest
Change clusterRole resources
Change pacman service type to NodePort

## Source

These are modified files from the below github repo for the node.js version, which contain the necessary changes to run in VMware Tanzu Kubernetes Grid (TKG) such as updated api values and pod security policies (psp) with associated service accounts and RBAC.

> <https://github.com/font/k8s-example-apps/tree/master/pacman-nodejs-app>

Security changes to the deployment such as setting up mongodb auth were thanks to [Dav1x](https://github.com/dav1x/) you can find his [Pac-Man deployment for OpenShift here](https://github.com/dav1x/pacman-ocp).
