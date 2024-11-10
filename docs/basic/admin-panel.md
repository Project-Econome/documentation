---
sidebar_position: 3
---

# Using the admin panel

## Accessing the admin panel
Once you have installed and turned on your bot, got Ddevs Portal and Locate your bot and goto Oauth2 and click `add redirect`

![redirects](./img/redirects.png)

once you have clicked that you should see a text box and you should type in `http://localhost:3000/auth/discord/callback` and once you have done that hit save.

![Save](./img/save.png)

now click reset secret not far from add redirect and put your secret into your env file with the rest of your bots information and should look something like this

```bash
DISCORD_CLIENT_ID=1299424625444519946
DISCORD_CLIENT_SECRET=VZhOOt_BE0XY1TnpcIa9GLUs6O9aA-cV
CALLBACK_URL=http://localhost:3000/auth/discord/callback
SESSION_SECRET=MySecretName
TOKEN=MTI5OTQyNDYyNTQ0NDUxOTk0Ng.GRAZlL.yg6uf-JlDuyYdd__Q9iy719R4T9deIZzjYLD6E
```

> at the time of this the example above will not connect you to a legitamate bot as all the info was reset

once you have completed this restart your bot and you should be able to access the panel through http://localhost:3000