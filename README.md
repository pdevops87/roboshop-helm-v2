# roboshop-helm-v2
helm install demo ./mychart
helm install demo ./mychart --set cfg.enabled=true

to trim the space in between use {{- if }} and {{- end}}