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

once you have completed this restart your bot and you should be able to access the panel through http://localhost:3000! 

> Note if your hosting provider doesnt support the panel there is a command that you can add to the bot visit [MyCountryBalls Optional Assets](https://example.com)

## Creating your first user
1. Go to `config.json` to add your first user, 

2. Locate `owners`

3. add your owners id's to the array.
```bash
{
  "Name": "CountryBall",
  "Report": "Report Forum Channel ID(must be forum atm)",
  "Log": "Catch Log Channel ID",
  "Artwork": "Artwork Log Forum Channel ID(must be forum atm)",
  "Version": "1.1.0",
  "Caught": "Caught",
  "owners": ["838105973985771520","id2"],
  "mongo": "mongodb+srv://username:pass@cluster0.clusterid.mongodb.net/bot"
}
```
4. goto your panel click login authorise your bot accessing your account and you will all be set.

> You will be disconnected after some time for security reasons. When this happens, you'll be redirected to the home page and need to relog in.

## Creating balls

To create your first CountryBall locate the form that should be at the top of the page.

Then Fill out the form.

    - `Country` is the name of your countryball

    - `Short name` can be used when the base name is too long for displaying in the card, providing a shorter alternative

    - `Catch names` is for providing alternative catch names for your countryball, may it be for translation or other purposes. You can input your different names separated by commas (,). **Don't put spaces between commas**

            > Your catch names may all be lowercased after saving, this is normal.

    - `Health` is the base health stat. This stat will vary from -20% to +20% when caught, defined randomly

    - `Attack` is the base attack stat. This stat will vary from -20% to +20% when caught, defined randomly

    - `Rarity` defines how rare is this countryball in the spawn algorithm. A value closer to 0 means more rare. A rarity equal to 0 means it cannot spawn.

            > While not required, it's a good practice to only set rarities between 0 and 10, 10 being the most common and 0 the most rare.

    - `Emoji ID` is for the custom emoji placed next to the ball when displayed. Obtaining an emoji ID is tricky:

            i. Type an emoji in the chat bar

            ![emoji](./img/emoji1.png)

            ii. Add an antislash \ character before your emoji. The image should disappear and show the text name of the emoji instead.

            ![emoji](./img/emoji2.png)

            iii. Send the message. The ID is a number between 17 and 19 characters as highlighted.

            ![emoji](./img/emoji3.png)

            iv. Copy and paste that number in the form

            ![emoji](./img/emoji4.png)


    - `Image credits` is a little sentence added for crediting the author of the artwords in the corner of the card

    - `type` is the image used inside the collection cards (/balls list or /balls info)

    - `Image` is the image used when a countryball spawns in the wild

Now click `save`, you just added your first countryball!


## How to share access to the dashboard
### If you're hosting this on your personal computer : its highly not recommended.

Opening your local traffic to the internet is incredibly risky, opening you to all kinds of security breaches. Not just you, but your entire family. If you don't have a domain name, you'll also be forced to openly share your IP address. And if you don't configure secure networking, that's opening your PC to even more potential viruses and security breaches.

### HOWEVER
if you are using visual code and know what you are doing forward a port to your panel however this means you will need to keep your pc on at all times

But if you dont know what you are doing DONT ATTEMPT THIS!

###Server Hosting
if you are hosting this on a server you may see something like `my.server.xyz:3000` on pterodactyl servers if your service provides an SSH connection then the panel should be accessible if not then you are out of luck. but if it does support this then add the user to your config.json and they should be able to access the panel when you are sending them the link!