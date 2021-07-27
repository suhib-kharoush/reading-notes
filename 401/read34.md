# Configuring Django Settings

#### Managing Django Settings: Issues
- Different environments. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. 

- Sensitive data. You have `SECRET_KEY` in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.

- Sharing settings between team members. we need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings.

- Django settings are a Python code. This is a curse and a blessing at the same time.

#### Setting Configuration: Different Approaches
- There is no built-in universal way to configure Django settings without hardcoding them. But books, open-source and work projects provide a lot of recommendations and approaches on how to do it best. Let’s take a brief look at the most popular ones to examine their weaknesses and strengths.

#### settings_local.py
- This is the oldest method. I used it when I was configuring a Django project on a production server for the first time. I saw a lot of people use it back in the day, and I still see it now.

#### Separate settings file for each environment
- This is an extension of the previous approach. It allows us to keep all configurations in VCS and to share default settings between developers.

- In this case, we make a settings package with the following file structure:

```
settings/
   ├── __init__.py
   ├── base.py
   ├── ci.py
   ├── local.py
   ├── staging.py
   ├── production.py
   └── qa.py
```


#### Setting Structure
- Instead of splitting settings by environments, you can split them by the source: Django, third- party apps (Celery, DRF, etc.), and your custom settings.

- File structure:
```
project/
├── apps/
├── settings/
│   ├── __init__.py
│   ├── djano.py
│   ├── project.py
│   └── third_party.py
└── manage.py
```
#### Django Settings:
- - Keep settings in environment variables.
- - Write default values for production configuration (excluding secret keys and tokens).
- - Don’t hardcode sensitive settings, and don’t put them in VCS.
- - Split settings into groups: Django, third-party, project.
- - Follow naming conventions for custom (project) settings.


#### How Does SSH Work?

![](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/ssh-tutorial-how-does-ssh-work-768x478.jpg)

#### What is SSH?
- SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.

#### How Does SSH Work?
- For Mac and Linux users, head over to your terminal program and then follow the procedure below:

- The SSH command consists of 3 distinct parts:
````
ssh {user}@{host}
````

#### Understanding Different Encryption Techniques:
- The significant advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client. Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host. There are three different encryption technologies used by SSH:
- - Symmetrical encryption
- - Asymmetrical encryption
- - Hashing.

#### Symmetric Encryption
- Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the client and the host. Effectively, any one possessing the key can decrypt the message being transferred.

![](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/symmetric-encryption-ssh-tutorial.jpg)

#### Asymmetric Encryption
- Unlike symmetrical encryption, asymmetrical encryption uses two separate keys for encryption and decryption. These two keys are known as the public key and the private key. Together, both these keys form a public-private key pair.

![](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/asymmetric-encryption.jpg)

#### Hashing
- One-way hashing is another form of cryptography used in Secure Shell Connections. One-way-hash functions differ from the above two forms of encryption in the sense that they are never meant to be decrypted. They generate a unique value of a fixed length for each input that shows no clear trend which can exploited. This makes them practically impossible to reverse.

![](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/ssh-tutorial-hash.jpg)