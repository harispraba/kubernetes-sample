# Step to test HPA

- Setup both apache and its HPA from yaml
- Run load generation pod
- Watch the HPA working

## Load generation pod

`kubectl run -i --tty load-generator --rm --image=busybox:1.28 --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"`
