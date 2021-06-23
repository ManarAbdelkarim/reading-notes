# API Deployment

# Configuring Django Settings: Best Practices

## Managing Django Settings: Issues

1- `Sensitive data`. You have SECRET_KEY in each Django project. This data cannot be stored in VCS.

2- S`haring settings between team members`. You need a general approach to eliminate human error when working with the settings.

4- `Django settings are a Python code`. This is a curse and a blessing at the same time. 



## Separate settings file for each environment

## 12 Factors
12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud.

- Codebase
- Dependencies
- Config
- Backing services
- Build, release, run
- Processes
- Port binding
- Concurrency
- Disposability
- Dev/prod parity
- Logs
- Admin processes


## Django Settings: Best practices
- Keep settings in environment variables.

- Write default values for production configuration (excluding secret keys and tokens).

- Don’t hardcode sensitive settings, and don’t put them in VCS.

- Split settings into groups: Django, third-party, project.

- Follow naming conventions for custom (project) settings.

# How Does SSH Work

## What is SSH
SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet.

## Understanding Different Encryption Techniques

![](https://miro.medium.com/max/640/1*23RpkZuWAeSP7x0YdMtsdQ.png)

- Symmetrical Encryption

Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the client and the host. Effectively, 

- Asymmetrical encryption

Unlike symmetrical encryption, asymmetrical encryption uses two separate keys for encryption and decryption. These two keys are known as the public key and the private key. 


- Hashing.

hashing is another form of cryptography used in Secure Shell Connections.