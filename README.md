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
