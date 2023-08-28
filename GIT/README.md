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
- on the repo dashboard, click the code button and navigate SSH Panel and copy the code
- go to the CLI and type the following code, while still in the same directory you have your ssh-rsa key,
```git clone <the code you copied>```
- This will clone the repository locally unto your computer

### Working with the Cloned Repo: Adding to the Imaginary Box
So, now you have the files locally on your device. Let's assume you've done some things on the repo. E.g. Create new file, deleted something, edit some file, etc. These changes needs to be bundled inside the git box. 

Don't mind me, that's how I was able to learn it. Let me explain it to you this way. As a developer, you get a file that others are working with. All the changes you made have to be packaged into a box of change as you make all your changes. Finally, when you are done with tthe work, you will have to send this box back to the GitHub where the comparison and merging of other boxes can be done into one huge box of project. Is that clear?

Now, let's continue from where I stopped ---------> "Let's assume you've done some things on the repo. E.g. Create new file, deleted something, edit some file, etc. These changes needs to be bundled inside the git box." 

Now, have made some changes to the file you cloned. You will need to add these changes inside the git box. Your own little box. To do this, enter the code below.

```git add <name of the file>``` --------------------------> This will add that particular file into the imaginary box.

what happen if you made changes to numerous files, don't tell me you will write that multiple times for all the files. Nah! Your blood might dry. 
To do this for numerous files, enter the line of code below

```git add .``` ------------> The dot after the "add" means you are adding all files to the imaginary box.

### Seal the damn Box
So, after all the changes, you decide that it's time to save your changes globally on the GitHub repo. This means you want to add your own box to other boxes on github to be merged into the giant box of project. Before you can move the box online, you will need to first seal the box. There are some rules that is need while sealing the box.
- The box must be given a special title: as a dev, you will be working with a lot of boxes (box = change). And after you are done with each boxes, you will need to submit it to the box manager (Git - version control handled by GitHub here). To avoid confusion of "who have what", proper labelling of the box is needed.. This is called COMMIT MESSAGE.

```git commit -m "COMMIT MESSAGE"``` --------------> The -m is a flag that signifies that the next string is a message. Ensure to use intuitive label for your box. 

### Box sealed? Now Push that Thing to space
Like I said earlier, after you are done with your changes, you will need to send it globally where it will be compared and merged with the giant box (main code). So how do you send your box to this merging room?

```git push``` -------------> This line of code will send the sealed box into space. Note: there are times you will need to add other things to this code. ut for now, let's stick to this simple line of code.