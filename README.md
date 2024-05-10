## Enverment variable setup

```
env:
  MONGODB_DB_NAME: gha-demo
jobs:
  test:
    env:
      MONGODB_CLUSTER_ADDRESS: cluster0.vvdui8d.mongodb.net
      MONGODB_USERNAME: dhruvin
      MONGODB_PASSWORD: 820Dhruvpani
      PORT: 8080
```

In this Example clearly see that setting up `env:` on main level, jobs level or steps level, if you setup on jobs level you can not access it on main level

### Github Secrets

```
  MONGODB_USERNAME: ${{ secrets.MONGODB_USERNAME }}
  MONGODB_PASSWORD: ${{ secrets.MONGODB_PASSWORD }}
```

bad practice to add our credentials direct into workflow file, so that time github secrets help to store and access out credentials