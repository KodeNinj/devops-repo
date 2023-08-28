# GIT & GITHUB
In this section I learnt about how code collaborations takes place and how these codes are managed from a single source called repository

## LEARNING STEPS

### Getting Started:
To get started, the git client must first be installed on the user's device. For this training, I installed it directly from my Ubuntu CLI using 
```apt install git```

Also, create a new repo on Github (which is exactly this repo you are curently). I have an account on Github before. If you don't, create an account before you will be able to create a repo.

### Setting up the global username and Email
You might need to set your footprint so that git can keep track of your changes by knowing who made a partiular changes. To set the email and phone

- To set your email: ```git config user.email "<Your email>"``` The email is in a quote
- To set your username: ```git config user.name "<Your username>"``` The username is in a quote

### Setting Up an SSH key
You want to be able to use SSH to bind your local, physical computer This means, the registry save on your system will  be able to recognize that of the public key saved on your Github account
- in your terminal, enter the code ```ssh-keygen``` This will generate an RSA keys (private and public key)
- Once the generation is done, ```ls```, ```cat <filename that have pub in it>```. Copy the public key strings
- Navigate to your Github account, go to setting via the profile section. Look for SSH and GPG keys
- Click NEW SSH KEY and in the title, put the name you want to use for your key. Then paste the strings you copy in the key box. The key usually start from ssh-rsa.
- To save, click ADD SSH KEY
- And that's all.


### Cloning Repo locally on your system
This just means, in layman terms, you want to download the repository onto your system so that you can work with the file. But in this type of download, the downloaded files is still partially linked to the repository on your Github.
To clone repo:
-  on the repo dashboard, click the code button and navigate HTTPS Panel and copy the code
- go to the CLI and type the following code, while still in the same directory you have your ssh-rsa key,
```git clone <the code you copied>```