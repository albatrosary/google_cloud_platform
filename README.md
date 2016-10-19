## Google Cloud Console

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