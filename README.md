# Teamcity Helm Chart
This chart deploy:
- A teamcity server
- Several teamcity agent
- Several teamcityagent with high memory
You can choose what to deploy by setting:
```yaml
agent:
  enabled: true
highmemagent:
  enabled: true
deployServer: true
```
## Upload a new version
```shell
helm repo add iprova https://chartmuseum.eiprova.com
helm plugin install https://github.com/chartmuseum/helm-push.git
helm push . iprova
```

## Installation
```shell
helm repo add iprova https://chartmuseum.eiprova.com
helm repo update
# Install the latest version of the Helm chart
helm install postgresql iprova/teamcity
```