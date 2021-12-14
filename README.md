## interactsh-web

[Interactsh-web](https://github.com/projectdiscovery/interactsh-web) is a free and open-source web client that displays [Interactsh](https://github.com/projectdiscovery/interactsh) interactions in a well-managed dashboard in your browser. It uses the **browser's local storage** to store and display interactions. By default, the web client is configured to use - **interachsh.com**, a cloud-hosted interactsh server, and supports other self-hosted public/authencaited interactsh servers as well.

A hosted instance of **interactsh-web** client is available at https://app.interactsh.com

<img width="2032" alt="interactsh-web" src="https://user-images.githubusercontent.com/8293321/135175927-07580994-32eb-4c06-8ca6-7ac9ea84776b.png">

## Installation on Ubuntu

### Install nodejs (tested on 17.2.0)

```sh
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
apt-get install -y nodejs
apt-get install gcc g++ make
``` 

### Clone Repo
```sh
git clone https://github.com/mishoops/interactsh-web.git
``` 

### Edit files

Edit URL values in following files
```console
   CNAME
   src/components/customHost/index.tsx
   src/lib/localStorage/index.ts
   src/pages/homePage/index.tsx
```

### Install app
```sh
npm install  --legacy-peer-deps
``` 

Upgrade npm to 8.3.0 if needed
```sh
npm install -g npm@8.3.0
``` 



### Running app

Export env variable
```sh
export NODE_OPTIONS=--openssl-legacy-provider
``` 

Change inotify value
```sh
 echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
```


Run app
```sh
npm start
```


