# C++

Gitpod supports C++ right out of the box, but there are still ways to optimize your Go experience within Gitpod.

## Examples
But before we begin here are some examples of already gitpodified repositories running in Gitpod

| Name | Open In Gitpod |
|------|----------------|
|Component Editor | [![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/Circuito-io/ComponentEditor) |
| eosio-web-ide | [![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/EOSIO/eosio-web-ide)
| tinyraycaster | [![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/ssloy/tinyraycaster)

<br>

## Workspace Configuration

### C/C++ VSCode Extensions
The C/C++ VSCode extension gives intellisense support for C++! To install it to your repository add the following to your [`.gitpod.yml`](https://www.gitpod.io/docs/config-gitpod-file/):
```yaml
vscode:
  extensions:
    - ms-vscode.cpptools@0.26.2:Pq/tmf2WN3SanVzB4xZc1g==
```

