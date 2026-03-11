# roboshop-helm-v2
helm install demo ./mychart
helm install demo ./mychart --set cfg.enabled=true

to trim the space in between use {{- if }} and {{- end}}


helm template roboshop . --show-only templates/cfgMap2.yaml , to show only single yaml file

helm upgrade -i roboshop . , to run all *.yaml files

hel upgrade -i roboshop . --dry-run --debug , to manifest all yaml files with templating values