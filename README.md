# roboshop-helm-v2
helm install demo ./mychart
helm install demo ./mychart --set cfg.enabled=true

to trim the space in between use {{- if }} and {{- end}}


helm template roboshop . --show-only templates/cfgMap2.yaml , to show only single yaml file

helm upgrade -i roboshop . , to run all *.yaml files

hel upgrade -i roboshop . --dry-run --debug , to manifest all yaml files with templating values


to install a chart:
====================
helm install full-coral ./mychart
 to retrieve the yaml file(manifest file) with release name:
helm get manifest full-coral

not install a chart but rendered template output:
=================================================
helm install --debug --dry-run goodly-guppy ./mychart

to override default values(values.yaml):
=======================================
helm install solid-vulture ./mychart --dry-run=client --debug --set favoriteDrink=slurm
or 
helm install demo . -f  pass-args/cart.yaml

shows a summary (table view) of the Pod
========================================
kubectl get pod mypod -n mynamespace

