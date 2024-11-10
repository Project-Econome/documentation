---
sidebar_position: 1
---

# Installing MyCountryBalls!

## 1. Install requirements (optional)
You need to install Docker and git on your computer.

When installing git, be sure to choose the option that says "Git from the command line and also for 3rd-party software". Leave the other options to their default values.

> Dont Panic! If you cannot install Docker, skip this step and read further on.

## 2. Create a Discord bot account
You must first setup a Discord bot account. You can follow discord.js's tutorial to create and invite your bot.

For now, don't copy your token, but keep the page open.

Once this is configured, you also need to enable message content intent. Go to the "Bot" tab of your application, scroll down to "Privileged intents" and tick "Message content".

> Tip: You can fill the description of your application, it will appear under the "About me" section.

## 3. Download the bot
### Windows
1. Right-click in the place where you want to install the bot, for instance your desktop, and select "Git bash here".

2. Paste the following command:

```bash 
git clone https://github.com/try-econome/MyCountryBalls.git
```
A folder named try-econome/MyCountryBalls should have appeared. If not, right-click and hit "Refresh".

### macOS/Linux
1. Open the terminal app and navigate to the folder where you want to install the bot using the cd command. For instance, if you want to install the bot in your desktop, type `cd` Desktop.

2. Paste the following command:

```bash 
git clone https://github.com/try-econome/MyCountryBalls.git
```
A folder named try-econome/MyCountryBalls should have appeared.

## 4. Installing the bot
### With Docker 
1. Open a command prompt and navigate to the bot's folder
   - **Windows**: Open the folder, then in the explorer's navigation bar, write "powershell"
   - **macOS/Linux**: Open the terminal and use cd ```<folder>``` to navigate (for instance ```cd Desktop/try-econome/MyCountryBalls```)
2. Make sure the bot is running by entering the `docker ps` command. If there is an error such as "Cannot connect to the Docker daemon", start Docker.
3. Run `docker compose build`. This will download a lot of components and may take some time, wait until it is done.

### Without Docker (recommended)
1. Install Node.js v18 at least.
2. Open a command prompt and navigate to the bot's folder
    - Windows: Open the folder, then in the explorer's navigation bar, write "powershell"
    - macOS/Linux: Open the terminal and use cd ```<folder>``` to navigate (for instance ```cd Desktop/try-econome/MyCountryBalls```)
3. Run `npm install` to download all the dependencies
