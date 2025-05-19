## Instalacja Klastra 

### Control-plane nodes

1. Włączenie modułów (`overlay` i `br_netfilter`)
2. Konfiguracja kernala (ip_forward / nf-call )
3. Wyłączenie SWAPa ( + /etc/fstab)
4. Instalacja container runtime (containerd / cri-io / cri-dockerd)
5. Instalacja pakietów pomocniczych (curl, http-transport)
6. Dodanie repozytorium K8s (+ refresh)
7. Inicjalizacja klastra (`kubeadm init`)
8. Kopiowanie configu
9. Instalacja network pluginu

## Worker nodes

1. Włączenie modułów (`overlay` i `br_netfilter`)
2. Konfiguracja kernala (ip_forward / nf-call )
3. Wyłączenie SWAPa ( + /etc/fstab)
4. Instalacja container runtime (containerd / cri-io / cri-dockerd)
5. Instalacja pakietów pomocniczych (curl, http-transport)
6. Dodanie repozytorium K8s (+ refresh)
7. Join do control-plane (jako root `kubeadm join`)

> Note: Punkty 1-6 pokrywa skyprt `deploy-k8s-<os>.sh`.
