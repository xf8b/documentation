---
layout: default
title: Startup Guide
permalink: /xf8bot/startup/
---

# Startup Guide
You need:  

* A bot token (See [How To Get A Token](#how-to-get-a-token))  
* Java 15 (I recommend [AdoptOpenJDK](https://adoptopenjdk.net))    
* A MongoDB Server (You can use the [cloud server they provide for free](https://www.mongodb.com/cloud/atlas/signup) or host your own)  

### Using Docker
**You must have a GitHub account and a PAT for authenticating!**
See [the GitHub docs](https://docs.github.com/en/free-pro-team@latest/packages/managing-container-images-with-github-container-registry/pushing-and-pulling-docker-images#authenticating-to-github-container-registry) if you need help.
1. Install Docker if you haven't.
2. Authenticate to the GitHub Container Registry.
3. Run `docker pull ghcr.io/xf8b/xf8bot` to pull the image.
4. Run `docker run xf8bot:TAG ARGS`, with `TAG` being the version you would like to run (latest or stable) and `ARGS` being the program arguments that you pass in. For a full list of program arguments, see [the documentation](https://xf8b.github.io/documentation/xf8bot/args/).
5. Invite the bot to your server.  
6. You're done.  
### Self Compiling
1. Download the code, and run `gradlew shadowJar` (or `./gradlew shadowJar` for Mac and Linux).    
2. The jar file will be in `build/libs`.  
3. Run that using `java -jar xf8bot-x.x.x-all.jar`. (optionally you can add program arguments so you don't have to do step 4. see [the documentation](https://xf8b.github.io/documentation/xf8bot/args/))
4. It will fail because of the invalid token.  
You must go to `config.toml` and fill out the fields that are under `required`.  
5. Invite the bot to your server.  
6. You're done.  

## Config
You must setup (if you use the config file):

* The MongoDB connection URL (See [The MongoDB Documentation](https://docs.mongodb.com/manual/reference/connection-string/))
* The MongoDB database name 
* The token (See [How To Get A Token](#how-to-get-a-token))
* The bot administrators (Copy paste your user ID into the brackets (See [Discord Support](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-)))
* The sharding strategy (I recommend to keep it at `RECOMMENDED`)

You can remove the log dump webhook field by putting a # before it.

## How To Get A Token
1. Go to the [Discord Developer Portal](https://discord.com/developers/applications).
2. Login with your Discord account if you need to.
3. Click **New Application**.
4. Type the name that you want the bot to be named.
5. Click **Bot** on the side, and then click **Add Bot**. Press **Confirm**.
6. You must go down and enable the **Server Members Intent**.
7. You now have the token. Do not share this token, as it is basically the key to the bot. If you ever accidentally leak it, press the **Regenerate** button.
## How To Get The Invite
1. Go to the [Discord Developer Portal](https://discord.com/developers/applications).
2. Login with your Discord account if you need to.
3. Click the application that you created in the [How To Get A Token](#how-to-get-a-token) section.
4. Copy the **Client ID**.
5. The template for the invite link is `https://discordapp.com/oauth2/authorize?client_id=CLIENT_ID&permissions=8&scope=bot`. Replace `CLIENT_ID` with the client id.
6. You now have the invite. Copy paste the link into your browser and add it to your server.

<b> <a rel="cc:attributionURL" property="dct:title" href="https://xf8b.github.io/documentation/xf8bot/">xf8bot Documentation</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/xf8b/">xf8b</a> is licensed under <a rel="license" href="https://creativecommons.org/licenses/by-sa/4.0">CC BY-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" /><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" /><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" /></a> </b> 
