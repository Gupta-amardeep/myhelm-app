curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3

chmod 755 get_helm.sh

./get_helm.sh

helm version

which helm

Create chart:-
helm create <chart>
tree <chart>

helm lint <chart> :-check issues in chart

helm install springboot --debug --dry-run springboot

hel template <chart> :- check values in templates

helm install <appname> <chart>

helm upgrade <appname> <chart>

stable rep add:-
helm repo add stable https://charts.helm.sh/stable

helm search repo stable

helm install stable/mysql