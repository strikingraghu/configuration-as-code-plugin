# configure gitlab plugin

## sample configuration

```yaml
jenkins:
  [...]
credentials:
  system:
    domainCredentials:
      - credentials:
          - gitLabApiTokenImpl:
              scope: SYSTEM
              id: gitlab_token
              apiToken: "qwertyuiopasdfghjklzxcvbnm"
              description: "Gitlab Token"
unclassified:
  gitlabconnectionconfig:
    connections:
    - apiTokenId: gitlab_token
      clientBuilderId: "autodetect"
      connectionTimeout: 20
      ignoreCertificateErrors: true
      name: "my_gitlab_server"
      readTimeout: 10
      url: "https://gitlab.com/"
```
