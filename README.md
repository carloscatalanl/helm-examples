# Helm Examples

> Helm examples

## Prerequisites

Helm:

https://helm.sh/docs/intro/install/

## Resources

[Artifacthub](https://artifacthub.io/)

## Common commands:

Add repo:
```ssh
helm repo add <repo-name> <repo-url>
```

Check repo charts:
```ssh
helm search repo <repo-name>
```

Update my helm repos:
```ssh
helm repo update   
```

Install helm chart:
```ssh
helm install <chart-name> --generate-name --create-namespace --namespace <namespace>
```

List helm charts installed:
```ssh
helm -n <namespace> list
```

Uninstall helm chart:
```ssh
helm -n <namespace> uninstall <repo-name>
```

Show values:
```ssh
helm show values <chart-name>
```

Export values to file:
```ssh
helm show values <chart-name> > config.yaml
```

Install chart with new files from file:
```ssh
helm install -f config.yaml bitnami/wordpress --generate-name --create-namespace --namespace <namespace>
```

Set custom value to a new chart:
```ssh
helm install <chart-name> --generate-name --set <var>=<value> --create-namespace --namespace <namespace>
```

Upgrade a helm chart:
```ssh
helm -n <namespace> upgrade -f config.yaml <actual-chart-name> <from-chart-name>
```

Rollback a helm chart:
```ssh
helm -n <namespace> rollback <chart-name> <number-of-version-back>
```

Show chart history:
```ssh
helm -n <namespace>  history <chart-name>
```
