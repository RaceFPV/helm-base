# Release Log

## 0.0.1

See the values-example.yaml for all of the ways this chart can be used. You can use one, or all of the options available. You can also run multiple of each option and helm will iterate over the values, for example:
```
deployments:
    deployment1:
        containers:
        - name: container1
            image:
            repository: example.com/docker/test1
    deployment2:
        containers:
        - name: container1
            image:
            repository: example.com/docker/test2
```

# Base helm chart template
Used as a base for all helm based k8s deployments

'helm install my-app . -f values.yaml --namespace mynamespace --create-namespace'

'helm upgrade my-app . -f values.yaml --namespace mynamespace'

'helm uninstall my-app --namespace mynamespace'

## Creating a new chart version

'helm package ./base-chart'

'mv ./base-chart/<PATH_TO_FILE> ./base-chart/charts/'

*push or upload your newly generated packaged file to your helm repo of choice*