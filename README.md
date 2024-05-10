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