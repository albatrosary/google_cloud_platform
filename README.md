## Google Cloud Platform

### Test

```bash
$ gcloud config set project my-projects-146905 \
  && gcloud source repos clone nodejs-mvms-quickstart \
    ~/src/my-projects-146905/nodejs_mvms_quickstart-2016-10-19-14-44  \
  && cd ~/src/my-projects-146905/nodejs_mvms_quickstart-2016-10-19-14-44/1-hello-world \
  && git checkout master
$ npm install --production
$ npm start
```

https://8080-dot-2168056-dot-devshell.appspot.com/?authuser=3

### Deploy

```bash
gcloud app deploy
```

http://my-projects-146905.appspot.com/


## 

### gcloud + git
```bash
$ git init
$ git add .
$ git commit -m "first commit"
$ git remote add google https://source.developers.google.com/p/my-projects-146905/r/default
$ git config --local credential.helper gcloud.sh
$ git push --all google
```

### deploy

```bash
$ gcloud config set project my-projects-146905 \
  && gcloud source repos clone default \
    ~/src/my-projects-146905/default  \
  && cd ~/src/my-projects-146905/default \
  && git checkout master
$ gcloud app deploy
```