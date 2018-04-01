# DevOps Machine (Docker)

## 1. Installing the tools

##### 1.1 - first you need to install Homebrew and Cask, you can do so by running following commands in sequence 

```
xcode-select --install
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew doctor //this is just to make sure Homebrew installed successfully
 
brew tap caskroom/cask
brew install cask
```
##### 1.2 - then you need to install virtualbox, since our docker's setup relies on a virtual machine that is powered
 by 
virtualbox,

if you have it installed you can skip this step otherwise open up your terminal and run this command:

```
brew cask install virtualbox
```

##### 1.3 then install docker and its tools

if you have it installed you can skip this step otherwise  run this command:

```
brew install docker docker-compose docker-machine
```

##### 1.4 then install docker credentials helper 
if you have it installed you can skip this step otherwise run this command:

```
brew install docker-credential-helper
```

## 2- Prepare the workspace:

##### 2.1 - to create the workspace directory run the following command

```
mkdir ~/Workspace
```
now lets cd in
```
cd ~/Workspace
```
now lets clone the devops-machine repository.
```
git clone https://github.com/anmolnagpal/devops-machine
```
cd to it 
```
cd devops-machine
```
Make sure that you are at master branch & have updated code 
```
git checkout master && git pull origin master
```
## 3- Creating the virtual machine:

##### 3.1 - to create the virtual machine with the name dev using the following command

```
make create-vbox 
```

##### 3.2 Now lets make sure that the machine is running

```
make start
```

## ☑ TODO

- [] Add proper readbme  
- [] Add other devops tools



## 👬 Contribution

- Open pull request with improvements
- Discuss ideas in issues
- Spread the word
- Reach out with any feedback [![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/anmol_nagpal.svg?style=social&label=Follow%20anmolnagpal)](https://twitter.com/anmol_nagpal)
