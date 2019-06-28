# kubectl

+ [Available Commands](#available-commands)
    + [Basic Commands (Beginner)](#basic-commands-beginner)
    + [Basic Commands (Intermediate)](#basic-commands-intermediate)
    + [Deploy Commands](#deploy-commands)
    + [Cluster Management Commands](#cluster-management-commands)
    + [Troubleshooting and Debugging Commands](#troubleshooting-and-debugging-commands)
    + [Advanced Commands](#advanced-commands)
    + [Settings Commands](#settings-commands)
    + [Other Commands](#other-commands)

## Available Commands

+ [kubectl](kubectl.md)
+ [kubectl options](kubectl-options.md)

### Basic Commands (Beginner)

+ [kubectl create](kubectl-create.md) kubectl create --help
+ [kubectl create clusterrole](kubectl-create-clusterrole.md) kubectl create clusterrole --help
+ [kubectl create clusterrolebinding](kubectl-create-clusterrolebinding.md) kubectl create clusterrolebinding --help
+ [kubectl create configmap](kubectl-create-configmap.md) kubectl create configmap --help
+ [kubectl create deployment](kubectl-create-deployment.md) kubectl create deployment --help
+ [kubectl create job](kubectl-create-job.md) kubectl create job --help
+ [kubectl create namespace](kubectl-create-namespace.md) kubectl create namespace --help
+ [kubectl create poddisruptionbudget](kubectl-create-poddisruptionbudget.md) kubectl create poddisruptionbudget --help
+ [kubectl create priorityclass](kubectl-create-priorityclass.md) kubectl create priorityclass --help
+ [kubectl create quota](kubectl-create-quota.md) kubectl create quota --help
+ [kubectl create role](kubectl-create-role.md) kubectl create role --help
+ [kubectl create rolebinding](kubectl-create-rolebinding.md) kubectl create rolebinding --help

+ [kubectl create secret](kubectl-create-secret.md) kubectl create secret --help
+ [kubectl create secret docker-registry](kubectl-create-secret-docker-registry.md) kubectl create secret docker-registry --help
+ [kubectl create secret generic](kubectl-create-secret-generic.md) kubectl create secret generic --help
+ [kubectl create secret tls](kubectl-create-secret-tls.md) kubectl create secret tls --help

+ [kubectl create service](kubectl-create-service.md) kubectl create service --help
+ [kubectl create service clusterip](kubectl-create-service-clusterip.md) kubectl create service clusterip --help
+ [kubectl create service externalname](kubectl-create-service-externalname.md) kubectl create service externalname --help
+ [kubectl create service loadbalancer](kubectl-create-service-loadbalancer.md) kubectl create service loadbalancer --help
+ [kubectl create service nodeport](kubectl-create-service-nodeport.md) kubectl create service nodeport --help

+ [kubectl create serviceaccount](kubectl-create-serviceaccount.md) kubectl create serviceaccount --help

+ [kubectl expose](kubectl-expose.md) kubectl expose --help
+ [kubectl run](kubectl-run.md) kubectl run --help

+ [kubectl set](kubectl-set.md) kubectl set --help
+ [kubectl set env](kubectl-set-env.md) kubectl set env --help
+ [kubectl set image](kubectl-set-image.md) kubectl set image --help
+ [kubectl set resources](kubectl-set-resources.md) kubectl set resources --help
+ [kubectl set selector](kubectl-set-selector.md) kubectl set selector --help
+ [kubectl set serviceaccount](kubectl-set-serviceaccount.md) kubectl set serviceaccount --help
+ [kubectl set subject](kubectl-set-subject.md) kubectl set subject --help

### Basic Commands (Intermediate)

+ [kubectl explain](kubectl-explain.md) kubectl explain --help
+ [kubectl get](kubectl-get.md) kubectl get --help
+ [kubectl edit](kubectl-edit.md) kubectl edit --help
+ [kubectl delete](kubectl-delete.md) kubectl delete --help

### Deploy Commands

+ [kubectl rollout](kubectl-rollout.md) kubectl rollout --help
+ [kubectl rollout history](kubectl-rollout-history.md) kubectl rollout history --help
+ [kubectl rollout pause](kubectl-rollout-pause.md) kubectl rollout pause --help
+ [kubectl rollout resume](kubectl-rollout-resume.md) kubectl rollout resume --help
+ [kubectl rollout status](kubectl-rollout-status.md) kubectl rollout status --help
+ [kubectl rollout undo](kubectl-rollout-undo.md) kubectl rollout undo --help

+ [kubectl scale](kubectl-scale.md) kubectl scale --help
+ [kubectl autoscale](kubectl-autoscale.md) kubectl autoscale --help

### Cluster Management Commands

+ [kubectl certificate](kubectl-certificate.md) kubectl certificate --help
+ [kubectl certificate approve](kubectl-certificate-approve.md) kubectl certificate approve --help
+ [kubectl certificate deny](kubectl-certificate-deny.md) kubectl certificate deny --help

+ [kubectl cluster-info](kubectl-cluster-info.md) kubectl cluster-info --help
+ [kubectl cluster-info dump](kubectl-cluster-info-dump.md) kubectl cluster-info dump --help

+ [kubectl top](kubectl-top.md) kubectl top --help
+ [kubectl top node](kubectl-top-node.md) kubectl top node --help
+ [kubectl top pod](kubectl-top-pod.md) kubectl top pod --help

+ [kubectl cordon](kubectl-cordon.md) kubectl cordon --help
+ [kubectl uncordon](kubectl-uncordon.md) kubectl uncordon --help
+ [kubectl drain](kubectl-drain.md) kubectl drain --help
+ [kubectl taint](kubectl-taint.md) kubectl taint --help

### Troubleshooting and Debugging Commands

+ [kubectl describe](kubectl-describe.md) kubectl describe --help
+ [kubectl logs](kubectl-logs.md) kubectl logs --help
+ [kubectl attach](kubectl-attach.md) kubectl attach --help
+ [kubectl exec](kubectl-exec.md) kubectl exec --help
+ [kubectl port-forward](kubectl-port-forward.md) kubectl port-forward --help
+ [kubectl proxy](kubectl-proxy.md) kubectl proxy --help
+ [kubectl cp](kubectl-cp.md) kubectl cp --help

+ [kubectl auth](kubectl-auth.md) kubectl auth --help
+ [kubectl auth can-i](kubectl-auth-can-i.md) kubectl auth can-i --help
+ [kubectl auth reconcile](kubectl-auth-reconcile.md) kubectl auth reconcile --help

### Advanced Commands

+ [kubectl diff](kubectl-diff.md) kubectl diff --help

+ [kubectl apply](kubectl-apply.md) kubectl apply --help
+ [kubectl apply edit-last-applied](kubectl-apply-edit-last-applied.md) kubectl apply edit-last-applied --help
+ [kubectl apply set-last-applied](kubectl-apply-set-last-applied.md) kubectl apply set-last-applied --help
+ [kubectl apply view-last-applied](kubectl-apply-view-last-applied.md) kubectl apply view-last-applied --help

+ [kubectl patch](kubectl-patch.md) kubectl patch --help
+ [kubectl replace](kubectl-replace.md) kubectl replace --help
+ [kubectl wait](kubectl-wait.md) kubectl wait --help
+ [kubectl convert](kubectl-convert.md) kubectl convert --help

### Settings Commands

+ [kubectl label](kubectl-label.md) kubectl label --help
+ [kubectl annotate](kubectl-annotate.md) kubectl annotate --help
+ [kubectl completion](kubectl-completion.md) kubectl completion --help

### Other Commands

+ [kubectl api-resources](kubectl-api-resources.md) kubectl api-resources --help
+ [kubectl api-versions](kubectl-api-versions.md) kubectl api-versions --help

+ [kubectl config](kubectl-config.md) kubectl config --help
+ [kubectl config current-context](kubectl-config-current-context.md) kubectl config current-context --help
+ [kubectl config delete-cluster](kubectl-config-delete-cluster.md) kubectl config delete-cluster --help
+ [kubectl config delete-context](kubectl-config-delete-context.md) kubectl config delete-context --help
+ [kubectl config get-clusters](kubectl-config-get-clusters.md) kubectl config get-clusters --help
+ [kubectl config get-contexts](kubectl-config-get-contexts.md) kubectl config get-contexts --help
+ [kubectl config rename-context](kubectl-config-rename-context.md) kubectl config rename-context --help
+ [kubectl config set](kubectl-config-set.md) kubectl config set --help
+ [kubectl config set-cluster](kubectl-config-set-cluster.md) kubectl config set-cluster --help
+ [kubectl config set-context](kubectl-config-set-context.md) kubectl config set-context --help
+ [kubectl config set-credentials](kubectl-config-set-credentials.md) kubectl config set-credentials --help
+ [kubectl config unset](kubectl-config-unset.md) kubectl config unset --help
+ [kubectl config use-context](kubectl-config-use-context.md) kubectl config use-context --help
+ [kubectl config view](kubectl-config-view.md) kubectl config view --help

+ [kubectl plugin](kubectl-plugin.md)
+ [kubectl plugin list](kubectl-plugin-list.md)

+ [kubectl version](kubectl-version.md)


