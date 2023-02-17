More information can be found on https://liamhardman.cloud/automation/monitoring ! 

To apply these configs, simply clone this repo and run kubectl apply -f ./ .
While these configs aren't production ready, I have used persistent volumes where possible, so you won't lose a bunch of monitoring data as soon as you kill a deployment off!

Just one thing to note, this does assume that you have an nginx ingress if you're wanting to access grafana over the internet. If you're not, you can instead run a kubectl port-forward svc/grafana-svc -n monitoring 3000:3000
