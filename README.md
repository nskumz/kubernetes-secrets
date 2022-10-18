KUBERNETES-SECRETS

A Kubernetes secret is an object storing sensitive pieces of data such as usernames, passwords, tokens, and keys. Secrets are created by the system during an app installation or by users whenever they need to store sensitive information and make it available to a pod.

KUBERNETES SECRET TYPES

Kubernetes features two categories of secrets

1. The system’s service accounts automatically create built-in secrets and associate them with containers together with API credentials.
2. You can also create customized secrets for credentials you need to make available to pods.


Create Kubernetes Secrets
To create a Kubernetes secret, apply one of the following methods:

---> Use kubectl for a command-line based approach.

---> Create a configuration file for the secret.

---> Use a generator, such as Kustomize to generate the secret.

1. To start creating a secret with kubectl, first create the files to store the sensitive information:

```shell
echo -n 'user' > ./username.key
echo -n '54f41d12e8fa' > ./password.txt
```

2.now use kubectl to create the secrets
```shell
kubectl create secret generic fb-credentials
--from-file=username.key\
--from-file=password.txt
```

3. To provide keys for values stored in the secret, use the following syntax:

```shell
kubectl create secret generic [secret-name] \
--from-file=[key1]=[file1] \
--from-file=[key2]=[file2]
```
4. Check that the secret has been successfully created by typing:

```shell
kubectl get secrets
```



